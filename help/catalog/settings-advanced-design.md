---
title: Produkteinstellungen - [!UICONTROL Design]
description: Mit den Einstellungen für [!UICONTROL Design] können Sie für ein Produkt ein anderes Design auf eine Produktseite anwenden und das Layout ändern.
exl-id: 8606ddc7-ca81-4503-94e5-a8276506c0a1
feature: Catalog Management, Products, Page Content
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '276'
ht-degree: 0%

---

# Produkteinstellungen - [!UICONTROL Design]

Mit den Einstellungen für _[!UICONTROL Design]_können Sie ein anderes Design auf die Produktseite anwenden, das Spaltenlayout ändern, festlegen, wo Produktoptionen angezeigt werden, und benutzerdefinierten XML-Code eingeben.

![Design](./assets/product-design-ee.png){width="600" zoomable="yes"}

>[!NOTE]
>
>Wenn dasselbe Produkt mehreren Kategorien mit unterschiedlichen Design-Einstellungen für jede Kategorie zugewiesen wird, wird empfohlen, **[!UICONTROL Use Categories Path for Product URLs]** = `Yes` in den Konfigurationsoptionen für die Suchmaschinenoptimierung [3} festzulegen. ](../configuration-reference/catalog/catalog.md#search-engine-optimization) Um auf diese Einstellung zuzugreifen, gehen Sie zu &quot;**[!UICONTROL Stores]**&quot;> &quot;_[!UICONTROL Settings]_&quot;> &quot;**[!UICONTROL Configuration]**&quot;, erweitern Sie &quot;**[!UICONTROL Catalog]**&quot;, wählen Sie &quot;**[!UICONTROL Catalog]**&quot;im linken Bereich und erweitern Sie dann den Abschnitt &quot;**[!UICONTROL Search Engine Optimization]**&quot;auf der Seite.

| Feld | [Umfang](../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|---|---|----|
| [!UICONTROL Theme] | Store-Ansicht | ![Adobe Commerce](../assets/adobe-logo.svg) (nur Adobe Commerce) Ermöglicht Ihnen die Anwendung eines anderen Designs auf das Produkt. Optionen: (Alle verfügbaren Designs) |
| [!UICONTROL Layout] | Store-Ansicht | Bietet Ihnen die Möglichkeit, ein anderes [layout](../content-design/page-layout.md) auf die Produktseite anzuwenden. Optionen: <br/>**[!UICONTROL No layout updates]**- Standardmäßig sind keine Layoutaktualisierungen für die Produktseite verfügbar.<br/>**[!UICONTROL Empty]** - Ermöglicht Ihnen die Definition Ihres eigenen Layouts, z. B. einer vierspaltigen Seite. (Erfordert ein Verständnis von XML.) <br/>**[!UICONTROL 1 column]**- Wendet ein einspaltiges Layout auf die Produktseite an.<br/>**[!UICONTROL 2 columns with left bar]** - Wendet ein zweispaltiges Layout mit einer linken Seitenleiste auf die Produktseite an. <br/>**[!UICONTROL 2 columns with right bar]**- Wendet ein zweispaltiges Layout mit einer rechten Seitenleiste auf die Produktseite an.<br/>**[!UICONTROL 3 columns]** - Wendet ein dreiseitiges Layout auf die Produktseite an. <br/>**[!UICONTROL Page -- Full Width]**- (Erfordert [[!DNL Page Builder]](../page-builder/introduction.md)) Wendet das Layout mit voller Breite für CMS-Seiten auf die Produktseite an.<br/>**[!UICONTROL Category -- Full Width]** - (Erfordert [!DNL Page Builder]) Wendet das Layout mit voller Breite für Kategorieseiten auf die Produktseite an. <br/>**[!UICONTROL Product -- Full Width]**- (Erfordert [!UICONTROL Page Builder]) Wendet das Layout mit voller Breite für Produktseiten auf die Produktseite an. |
| [!UICONTROL Display Product Options In] | Store-Ansicht | Legt fest, wo die Produktoptionen auf der Produktseite angezeigt werden. Optionen: `Product Info Column` / `Block after Info Column` |
| [!UICONTROL Custom Layout Update] | Store-Ansicht | Wird verwendet, um auf Optionen zuzugreifen, um ein benutzerdefiniertes Layout auf der Produktseite zu aktualisieren. |

{style="table-layout:auto"}
