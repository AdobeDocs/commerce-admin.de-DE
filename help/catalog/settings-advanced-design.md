---
title: Produkteinstellungen - [!UICONTROL Design]
description: Mit den [!UICONTROL Design] können Sie für ein Produkt ein anderes Design auf eine Produktseite anwenden und das Layout ändern.
exl-id: 8606ddc7-ca81-4503-94e5-a8276506c0a1
feature: Catalog Management, Products, Page Content
TQID: 'https://experienceleague.adobe.com/u6VzZ9TiovuSopBcBjmpQTKl3pzh3DoXXzpr8akWp-8'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: c18ed297-2187-4aec-affb-9d9654eca6fc
    internal-label: Catalog management
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
  - id: 4067ab89-2e97-5de1-8d98-de8318461a8d
    internal-label: Products
  - id: 17d326fa-534a-55a5-b46f-8ae1de1e2f75
    internal-label: Page Content
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
    internal-label: Leader
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: acc7571574eb9c7e96911266897350a77913488e
workflow-type: tm+mt
source-wordcount: '284'
ht-degree: 0%
---
# Produkteinstellungen - [!UICONTROL Design]

Mit den _[!UICONTROL Design]_&#x200B;können Sie ein anderes Design auf die Produktseite anwenden, das Spalten-Layout ändern, festlegen, wo die Produktoptionen angezeigt werden, und benutzerdefinierten XML-Code eingeben.

![Design](./assets/product-design-ee.png){width="600" zoomable="yes"}

>[!NOTE]
>
>Wenn dasselbe Produkt mehreren Kategorien mit unterschiedlichen Designeinstellungen für jede Kategorie zugewiesen wird, wird empfohlen, in den Konfigurationsoptionen für die Suchmaschinenoptimierung **[!UICONTROL Use Categories Path for Product URLs]** = `Yes` [&#x200B; festlegen](../configuration-reference/catalog/catalog.md#search-engine-optimization). Um auf diese Einstellung zuzugreifen, gehen Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**, erweitern Sie **[!UICONTROL Catalog]**&#x200B;und wählen Sie im linken Bereich unten **[!UICONTROL Catalog]**&#x200B;aus und erweitern Sie dann den **[!UICONTROL Search Engine Optimization]**&#x200B;auf der Seite.

| Feld | [Umfang](../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|---|---|----|
| [!UICONTROL Theme] | Shop-Ansicht | ![Adobe Commerce](../assets/adobe-logo.svg) (nur Adobe Commerce) Ermöglicht das Anwenden eines anderen Designs auf das Produkt. Optionen: (Alle verfügbaren Designs) |
| [!UICONTROL Layout] | Shop-Ansicht | Ermöglicht die Anwendung eines anderen [Layouts](../content-design/page-layout.md) auf die Produktseite. Optionen: <br/>**[!UICONTROL No layout updates]**- Standardmäßig sind Layout-Aktualisierungen für die Produktseite nicht verfügbar.<br/>**[!UICONTROL Empty]** - Ermöglicht die Definition eines eigenen Layouts, z. B. einer 4-spaltigen Seite. (XML ist ein Verständnis erforderlich.) <br/>**[!UICONTROL 1 column]**- Wendet ein einspaltiges Layout auf die Produktseite an.<br/>**[!UICONTROL 2 columns with left bar]** - Wendet ein zweispaltiges Layout mit einer linken Seitenleiste auf die Produktseite an. <br/>**[!UICONTROL 2 columns with right bar]**- Wendet ein zweispaltiges Layout mit einer rechten Seitenleiste auf die Produktseite an.<br/>**[!UICONTROL 3 columns]** - Wendet ein dreispaltiges Layout auf die Produktseite an. <br/>**[!UICONTROL Page -- Full Width]**- ([[!DNL Page Builder]](../page-builder/introduction.md) erforderlich) Wendet das Layout „Vollbreite“ für CMS-Seiten auf die Produktseite an.<br/>**[!UICONTROL Category -- Full Width]** - ([!DNL Page Builder] erforderlich) Wendet das Layout mit der gesamten Breite für Kategorieseiten auf die Produktseite an. <br/>**[!UICONTROL Product -- Full Width]**- ([!UICONTROL Page Builder] erforderlich) Wendet das Layout mit der gesamten Breite für Produktseiten auf die Produktseite an. |
| [!UICONTROL Display Product Options In] | Shop-Ansicht | Legt fest, wo die Produktoptionen auf der Produktseite angezeigt werden. Optionen: `Product Info Column` / `Block after Info Column` |
| [!UICONTROL Custom Layout Update] | Shop-Ansicht | Wird verwendet, um auf Optionen zuzugreifen, um ein benutzerdefiniertes Layout auf der Produktseite zu aktualisieren. |

{style="table-layout:auto"}

