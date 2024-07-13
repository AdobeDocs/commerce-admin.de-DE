---
title: Kategorien - Designeinstellungen
description: Erfahren Sie mehr über die Verwendung der [!UICONTROL Design] -Einstellungen, um das Erscheinungsbild einer Kategorie, alle zugehörigen Produktseiten und das Seitenlayout zu definieren.
exl-id: 6dc216ac-1c52-4196-9c93-e5cad19901b5
feature: Catalog Management, Categories, Page Content
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '372'
ht-degree: 0%

---

# Kategorien - Designeinstellungen

Im Abschnitt &quot;_[!UICONTROL Design]_&quot; erhalten Sie Kontrolle über das Erscheinungsbild einer Kategorie, alle zugehörigen Produktseiten und das Seitenlayout. Sie können eine Kategorieseite und die zugehörigen Produkte für eine Promotion anpassen oder die Kategorie unterscheiden. Sie können beispielsweise ein charakteristisches Design für eine Marke oder eine spezielle Produktlinie entwickeln oder eine Aktualisierung für einen bestimmten Zeitraum anwenden.

![Designeinstellungen für eine Kategorie](./assets/category-design.png){width="600" zoomable="yes"}

>[!NOTE]
>
>Wenn dasselbe Produkt mehreren Kategorien mit unterschiedlichen Design-Einstellungen für jede Kategorie zugewiesen wird, wird empfohlen, den **Pfad der Kategorien für Produkt-URLs verwenden** = `Yes` in den [Konfigurationsoptionen zur Suchmaschinenoptimierung](../configuration-reference/catalog/catalog.md#search-engine-optimization) festzulegen. Um auf diese Einstellung zuzugreifen, gehen Sie zu &quot;**[!UICONTROL Stores]**&quot;> &quot;_[!UICONTROL Settings]_&quot;> &quot;**[!UICONTROL Configuration]**&quot;, erweitern Sie &quot;**[!UICONTROL Catalog]**&quot;, wählen Sie &quot;**Katalog**&quot;im linken Bereich aus und erweitern Sie dann den Abschnitt &quot;**Suchmaschinenoptimierung**&quot;auf der Seite.

| Feld | Beschreibung |
|--- |--- |
| [!UICONTROL Use Parent Category Settings] | Ermöglicht der aktuellen Kategorie, die Designeinstellungen von der übergeordneten Kategorie zu übernehmen. Bei Verwendung dieser Option sind alle anderen Felder im Abschnitt &quot;Design&quot;nicht mehr verfügbar. Optionen: `Yes` / ` No` |
| [!UICONTROL Theme] | Wendet ein benutzerdefiniertes Design auf die Kategorie an. |
| [!UICONTROL Layout] | Wendet ein anderes Layout auf die Kategorieseite an. Optionen: <br/>**[!UICONTROL No layout updates]**- Standardmäßig sind keine Layoutaktualisierungen für Kategorieseiten verfügbar.<br/>**[!UICONTROL Empty]** - Verwenden Sie , um Ihr eigenes Seitenlayout zu definieren. (Erfordert ein Verständnis von XML.) <br/>**[!UICONTROL 1 column]**- Wendet ein einspaltiges Layout auf die Kategorieseite an.<br/>**[!UICONTROL 2 columns with left bar]** - Wendet ein zweispaltiges Layout mit einer linken Seitenleiste auf die Kategorieseite an. <br/>**[!UICONTROL 2 columns with right bar]**- Wendet ein zweispaltiges Layout mit einer rechten Seitenleiste auf die Kategorieseite an.<br/>**[!UICONTROL 3 columns]** - Wendet ein dreiseitiges Layout auf die Kategorieseite an.<br/>**[!UICONTROL Page -- Full Width]**- (Erfordert [Seitenaufbau](../page-builder/introduction.md)) Wendet das Layout mit voller Breite für CMS-Seiten auf die Kategorieseite an.<br/>**[!UICONTROL Category -- Full Width]** - (Erfordert den Seitenaufbau) Wendet das Layout mit voller Breite für Kategorieseiten auf die Kategorieseite an. <br/>**[!UICONTROL Product -- Full Width]**- (Erfordert den Seitenaufbau) Wendet das Layout mit voller Breite für Produktseiten auf die Kategorieseite an. |
| [!UICONTROL Custom Layout Update] | Listet die verfügbaren benutzerdefinierten Layout-Aktualisierungsdateien auf dem Server auf. Wählen Sie das benutzerdefinierte Layout-Update aus, das Sie auf die Kategorie anwenden möchten. |
| [!UICONTROL Apply Design to Products] | Wenn diese Option aktiviert ist, werden die benutzerdefinierten Einstellungen auf alle Produkte in der Kategorie angewendet. |

{style="table-layout:auto"}

## [!UICONTROL Scheduled Design Update]

{{ce-feature}}

Der Abschnitt _[!UICONTROL Scheduled Design Update]_bestimmt den Datumsbereich, zu dem ein benutzerdefinierter Entwurf auf Kategorieseiten angewendet wird.

| Feld | Beschreibung |
|--- |--- |
| [!UICONTROL Schedule Update From/To] | Bestimmt den Datumsbereich, in dem ein benutzerdefiniertes Layout auf die Kategorie angewendet wird. |

![Geplantes Design-Update](./assets/category-scheduled-design-update.png){width="600" zoomable="yes"}
