---
title: Kategorien - Anzeigeeinstellungen
description: Erfahren Sie mehr über die Verwendung der [!UICONTROL Display] -Einstellungen, um festzulegen, welche Inhaltselemente auf einer Kategorieseite angezeigt werden und in welcher Reihenfolge Produkte angezeigt werden.
exl-id: bb3a1b00-ba56-4113-8208-860963612333
feature: Catalog Management, Categories, Page Content
source-git-commit: a47e744cf4cc5163ca2ba0718ccb78eb65a7d404
workflow-type: tm+mt
source-wordcount: '224'
ht-degree: 0%

---

# Kategorien - Anzeigeeinstellungen

Die Anzeigeeinstellungen bestimmen, welche Inhaltselemente auf einer Kategorieseite angezeigt werden und in welcher Reihenfolge Produkte angezeigt werden. Sie können CMS-Blöcke aktivieren, den Ankerstatus der Kategorie festlegen und Sortieroptionen über die _[!UICONTROL Display Settings]_Registerkarte. Beispiele dazu, wie Kategorien in der Storefront angezeigt werden, finden Sie unter [Katalognavigation](navigation.md).

![Anzeigeeinstellungen für Kategorien](./assets/category-display-settings.png){width="600" zoomable="yes"}

| Feld | Beschreibung |
|--- |--- |
| [!UICONTROL Display Mode] | Bestimmt die auf der Kategorieseite angezeigten Inhaltselemente. Optionen: `Products Only` / `Static Block Only` / `Static Block and Products` |
| [!UICONTROL Anchor] | Wenn festgelegt auf `Yes`zeigt Produkte aus den Unterkategorien der Kategorie an, selbst wenn sie nicht explizit zur Kategorie hinzugefügt wurden, und ermöglicht die Anzeige der Variablen _[!UICONTROL filter by attribute]_in der Navigationsleiste mit mehreren Ebenen. Optionen: `Yes` / `No` |
| [!UICONTROL Available Product Listing Sort By] | (Erforderlich) Die Standardwerte sind `Position`, `Name`, und `Price`. Um die Sortieroption anzupassen, deaktivieren Sie die Option **[!UICONTROL Use All Available Attributes]** und wählen Sie die Attribute aus, die Sie verwenden möchten. Sie können bei Bedarf Attribute definieren und hinzufügen. Diese Einstellung gilt nicht für die [!DNL Live Search] [Seiten-Widget &quot;Produktliste&quot;](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/live-search/live-search-storefront/plp-styling). |
| [!UICONTROL Default Product Listing Sort By] | (Erforderlich) So definieren Sie die Standardeinstellung _[!UICONTROL Sort By]_deaktivieren Sie die Option **[!UICONTROL Use Config Settings]**und wählen Sie ein Attribut aus. Diese Einstellung gilt nicht für die [!DNL Live Search] [Seiten-Widget &quot;Produktliste&quot;](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/live-search/live-search-storefront/plp-styling). |
| [!UICONTROL Layered Navigation Price Step] | Commerce zeigt die Preisspanne standardmäßig in Schritten von 10, 100 und 1000 an, je nach Produkten in der Liste. Heben Sie die Auswahl der Option **[!UICONTROL Use Config Settings]** aktivieren. |

{style="table-layout:auto"}
