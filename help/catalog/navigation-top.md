---
title: Navigation oben
description: Erfahren Sie, wie Sie das Hauptmenü eines Stores definieren, das wie ein Verzeichnis für die verschiedenen Abteilungen funktioniert.
exl-id: 8b71fe73-2716-4820-9e57-4cb1e6888132
feature: Catalog Management, Categories, Site Navigation
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '575'
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
| Ebene 2 | Auf einem Desktop-Display ist die obere Navigation das Hauptmenü, das oben auf der Seite angezeigt wird. Auf einem Mobilgerät wird das Hauptmenü in der Regel als Flyout-Menü mit Optionen angezeigt. Die Optionen der zweiten Ebene im Luma-Speicher sind _Neue Funktionen_, _Frauen_, _Männer_, _Zahnrad_, _Trainings_ und _Verkauf_. |
| Ebene 3 | Die dritte Ebene wird unter jeder Hauptmenüoption angezeigt. Beispielsweise sind unter _Women_ die Optionen der dritten Ebene _Tops_ und _Bottom_. |
| Ebene 4 | Die Optionen der vierten Ebene sind Unterkategorien, die von einer Option der dritten Ebene abfliegen. Beispielsweise sind unter _Tops_ die Menüoptionen der vierten Ebene _Jackets_, _Hoodies &amp; Sweatshirts_, _Tees_ und _Bras &amp; Tanks_. |

{style="table-layout:auto"}

## Festlegen der oberen Navigation

Damit eine Kategorie in der oberen Navigation eines Stores angezeigt wird, führen Sie die folgenden Schritte aus:

### Schritt 1: Erstellen einer Kategorie

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. Legen Sie einen **[!UICONTROL Store View]** fest, um zu bestimmen, wo die neue Kategorie verfügbar sein soll.

1. Wählen Sie im Kategoriebaum die übergeordnete Kategorie der neuen Kategorie aus.

   Wenn Sie von Anfang an ohne Daten beginnen, gibt es möglicherweise nur zwei Kategorien in der Liste: _Standardkategorie_, die der Stamm ist, und eine _Beispielkategorie_.

1. Klicken Sie auf **[!UICONTROL Add Subcategory]**.

1. Füllen Sie die grundlegenden Informationen mit den folgenden Einstellungen aus:

   - **[!UICONTROL Enable Category]** auf `Yes` gesetzt
   - **[!UICONTROL Include in Menu]** auf `Yes` gesetzt

1. Setzen Sie in der Anzeigeeinstellung **[!UICONTROL Anchor]** auf `Yes`.

1. Nehmen Sie alle weiteren erforderlichen [Kategorieeinstellungen](category-create.md) vor.

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save]**.

Bei einer Multistore-Installation kann für jeden [store](../stores-purchase/stores.md#add-stores) ein anderes Hauptmenü als [Stammkategorie](category-root.md) zugewiesen werden.

### Schritt 2: Festlegen der Tiefe der oberen Navigation

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bedienfeld den Wert **[!UICONTROL Catalog]** und wählen Sie unter &quot;**[!UICONTROL Catalog]**&quot;.

1. Erweitern Sie den Abschnitt **[!UICONTROL Category Top Navigation]** .

   ![Obere Navigation nach Kategorie](../configuration-reference/catalog/assets/catalog-category-top-navigation.png){width="600" zoomable="yes"}

   Da die Tiefe der oberen Navigation einen globalen [Konfigurationsbereich](../getting-started/websites-stores-views.md#scope-settings) aufweist, gilt die Einstellung für alle Websites, Stores und Store-Ansichten in der Commerce-Installation. Der Konfigurationsabschnitt _[!UICONTROL Category Top Navigation]_ist nur verfügbar, wenn_[!UICONTROL Store View]_ in der oberen linken Ecke auf `Default Config` gesetzt ist.

   Eine detaillierte Liste dieser Optionen finden Sie unter [Obere Navigation der Kategorie](../configuration-reference/catalog/catalog.md#layered-navigation) in der _Konfigurationsreferenz_.

1. Um die Anzahl der Unterkategorien zu begrenzen, die in der oberen Navigation angezeigt werden, geben Sie die Zahl für **[!UICONTROL Maximal Depth]** ein.

   Der Standardwert ist &quot;`0`&quot;, was keine Begrenzung für die Anzahl der Unterkategorie-Ebenen darstellt.

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save Config]**.
