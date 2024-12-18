---
title: Kategorien - Designeinstellungen
description: Erfahren Sie mehr über die Verwendung der [!UICONTROL Design]-Einstellungen zum Definieren des Aussehens einer Kategorie, aller zugehörigen Produktseiten und des Seiten-Layouts.
exl-id: 6dc216ac-1c52-4196-9c93-e5cad19901b5
feature: Catalog Management, Categories, Page Content
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '372'
ht-degree: 0%

---

# Kategorien - Designeinstellungen

Im _[!UICONTROL Design]_Abschnitt erhalten Sie Kontrolle über das Erscheinungsbild einer Kategorie, alle zugehörigen Produktseiten und das Seitenlayout. Sie können eine Kategorieseite und die zugehörigen Produkte für eine Promotion anpassen oder die Kategorie unterscheiden. Sie können beispielsweise ein unverwechselbares Design für eine Marke oder eine spezielle Produktlinie entwickeln oder ein Update für einen bestimmten Zeitraum anwenden.

![Design-Einstellungen für eine Kategorie](./assets/category-design.png){width="600" zoomable="yes"}

>[!NOTE]
>
>Wenn dasselbe Produkt mehreren Kategorien mit unterschiedlichen Designeinstellungen für jede Kategorie zugewiesen wird, wird empfohlen, in den Konfigurationsoptionen für die Suchmaschinenoptimierung **Kategoriepfad für Produkt** = `Yes` [ ](../configuration-reference/catalog/catalog.md#search-engine-optimization). Um auf diese Einstellung zuzugreifen, gehen Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**, erweitern Sie **[!UICONTROL Catalog]**und wählen Sie **Katalog**unten im linken Bereich aus und erweitern Sie dann den Abschnitt **Suchmaschinenoptimierung**auf der Seite.

| Feld | Beschreibung |
|--- |--- |
| [!UICONTROL Use Parent Category Settings] | Ermöglicht der aktuellen Kategorie, die Design-Einstellungen von der übergeordneten Kategorie zu übernehmen. Wenn diese Option verwendet wird, sind alle anderen Felder im Abschnitt Design nicht mehr verfügbar. Optionen: `Yes` / ` No` |
| [!UICONTROL Theme] | Wendet ein benutzerdefiniertes Design auf die Kategorie an. |
| [!UICONTROL Layout] | Wendet ein anderes Layout auf die Kategorieseite an. Optionen: <br/>**[!UICONTROL No layout updates]**- Standardmäßig sind Layout-Aktualisierungen für Kategorieseiten nicht verfügbar.<br/>**[!UICONTROL Empty]** : Hiermit können Sie Ihr eigenes Seiten-Layout definieren. (XML muss verstanden werden.) <br/>**[!UICONTROL 1 column]**- Wendet ein einspaltiges Layout auf die Kategorieseite an.<br/>**[!UICONTROL 2 columns with left bar]** - Wendet ein zweispaltiges Layout mit einer linken Seitenleiste auf die Kategorieseite an. <br/>**[!UICONTROL 2 columns with right bar]**- Wendet ein zweispaltiges Layout mit einer rechten Seitenleiste auf die Kategorieseite an.<br/>**[!UICONTROL 3 columns]** - Wendet ein dreispaltiges Layout auf die Kategorieseite an.<br/>**[!UICONTROL Page -- Full Width]**- (erfordert [Page Builder](../page-builder/introduction.md)) Wendet das Layout mit voller Breite für CMS-Seiten auf die Kategorieseite an.<br/>**[!UICONTROL Category -- Full Width]** - (Seiten-Builder erforderlich) Wendet das Layout mit voller Breite für Kategorieseiten auf die Kategorieseite an. <br/>**[!UICONTROL Product -- Full Width]**- (Seiten-Builder erforderlich) Wendet das Layout mit voller Breite für Produktseiten auf die Kategorieseite an. |
| [!UICONTROL Custom Layout Update] | Listet die verfügbaren benutzerdefinierten Layout-Aktualisierungsdateien auf dem Server auf. Wählen Sie die benutzerdefinierte Layout-Aktualisierung aus, die Sie auf die Kategorie anwenden möchten. |
| [!UICONTROL Apply Design to Products] | Wenn diese Option aktiviert ist, werden die benutzerdefinierten Einstellungen auf alle Produkte in der Kategorie angewendet. |

{style="table-layout:auto"}

## [!UICONTROL Scheduled Design Update]

{{ce-feature}}

Im Abschnitt _[!UICONTROL Scheduled Design Update]_wird der Datumsbereich festgelegt, in dem ein benutzerdefinierter Entwurf auf Kategorieseiten angewendet wird.

| Feld | Beschreibung |
|--- |--- |
| [!UICONTROL Schedule Update From/To] | Bestimmt den Datumsbereich, in dem ein benutzerdefiniertes Layout auf die Kategorie angewendet wird. |

![Geplante Design-Aktualisierung](./assets/category-scheduled-design-update.png){width="600" zoomable="yes"}
