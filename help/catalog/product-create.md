---
title: Produkt erstellen
description: Erfahren Sie mehr über die Arten von Produkten, die Sie für Ihren Katalog erstellen können.
exl-id: ff90bf8a-a64d-403f-bd09-5c8167a36f0b
feature: Catalog Management, Products
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '689'
ht-degree: 0%

---

# Produkt erstellen

Die Auswahl eines Produkttyps ist eines der ersten Dinge, die Sie tun müssen, um ein Produkt zu erstellen. Wenn Sie gerade erst mit der Erstellung Ihres Produktkatalogs beginnen, können Sie einige Beispielprodukte erstellen, um mit jedem Produkttyp zu experimentieren. Neben den grundlegenden Produktarten wird manchmal der Begriff _komplexes Produkt_ verwendet, um Produkte mit mehreren Optionen zu referenzieren, z. B. ein konfigurierbares Produkt, das in verschiedenen Farben und Größen verfügbar ist.

>[!NOTE]
>
>Weitere Informationen finden Sie unter Katalog [Navigation](navigation.md), Einrichten von [Kategorien](categories.md) und [Attributen](product-attributes.md) sowie verfügbare Katalog-[URL-Optionen](catalog-urls.md). Nachdem Sie diese Konzepte verstanden haben, ist die effizienteste Möglichkeit, viele Produkte zum Katalog hinzuzufügen, den [Import](../systems/data-import.md) dieser Produkte aus einer CSV-Datei.

![Produktseite auf der Storefront](./assets/storefront-product-page.png){width="700" zoomable="yes"}

## Produkttypen

**[Einfaches Produkt](product-create-simple.md)** - Ein einfaches Produkt ist ein physisches Element mit einer einzelnen SKU. Einfache Produkte verfügen über unterschiedliche Preise und Kontrollen der Vorleistungen, die den Verkauf von Produktvarianten ermöglichen. Einfache Produkte können zusammen mit gruppierten, gebündelten und konfigurierbaren Produkten verwendet werden.

**[Konfigurierbares Produkt](product-create-configurable.md)** - Ein konfigurierbares Produkt scheint ein einzelnes Produkt mit Optionslisten für jede Variante zu sein. Jede Option stellt jedoch ein separates, einfaches Produkt mit einer eigenen SKU dar, die es ermöglicht, den Bestand für jede Variante zu verfolgen.

**[Gruppiertes Produkt](product-create-grouped.md)** - Ein gruppiertes Produkt präsentiert mehrere eigenständige Produkte als Gruppe. Sie können Varianten eines einzelnen Produkts anbieten oder sie für eine Promotion gruppieren. Die Produkte können separat oder als Gruppe erworben werden.

**[Virtuelle Produkte](product-create-virtual.md)** - Ein virtuelles Produkt ist kein greifbares Produkt und wird normalerweise für Produkte wie Dienste, Mitgliedschaften, Garantien und Abonnements verwendet. Virtual Produkte können zusammen mit gruppierten und gebündelten Produkten verwendet werden.

**[Bundle-Produkt](product-create-bundle.md)** - Ein Bundle-Produkt ermöglicht Kunden, aus einer Reihe von Optionen &quot;eigene Produkte zu erstellen&quot;. Das Bundle kann ein Geschenkkorb, ein Computer oder alles andere sein, das angepasst werden kann. Jedes Element im Bundle ist ein separates, eigenständiges Produkt.

**[Herunterladbares Produkt](product-create-downloadable.md)** - Ein digital herunterladbares Produkt besteht aus einer oder mehreren heruntergeladenen Dateien. Die Dateien können sich auf Ihrem Server befinden oder als URLs für einen anderen Server bereitgestellt werden.

**[Geschenkkarte](product-gift-card-create.md)** - ([Nur Adobe Commerce](../landing/home.md#product-editions)) Es gibt drei Arten von Geschenkkarten. _Virtual_ Geschenkkarten werden per E-Mail versendet. _Physikalische_ Geschenkkarten werden an den Empfänger gesendet. _Kombinierte_ Geschenkkarten, die eine Kombination aus virtuellem und physischem Material sind. Jeder hat einen eindeutigen Code, der beim Checkout eingelöst wird. Geschenkkarten können auch in einem gruppierten Produkt enthalten sein.

## Produkteinstellungen

Die am häufigsten verwendeten Produkteinstellungen und Attribute werden oben auf der Seite angezeigt, gefolgt von benutzerdefinierten Attributen. Alle anderen Produkteinstellungen befinden sich in erweiterbaren Abschnitten am unteren Rand der Seite.

![Produkteinstellungen](./assets/product-settings.png){width="600" zoomable="yes"}

| Einstellung | Beschreibung |
|--- |--- |
| [[!UICONTROL Sources]](../inventory-management/sources-assign-per-product.md) | (Wenn [[!DNL Inventory Management]](../inventory-management/introduction.md) aktiviert ist) Listet die Quellen auf, aus denen das Produkt verteilt werden kann. |
| [[!UICONTROL Content]](product-content.md) | Wird verwendet, um die Hauptproduktbeschreibung einzugeben und zu bearbeiten, die auf der Produktseite der Storefront angezeigt wird. |
| [[!UICONTROL Configurations]](product-configurations.md) | Listet alle vorhandenen Varianten des Produkts auf und kann verwendet werden, um Varianten für die Verwendung mit dem konfigurierbaren Produkttyp zu generieren. |
| [[!UICONTROL Product Reviews]](settings-advanced-product-reviews.md) | Listet alle Bewertungen auf, die Kunden für das Produkt eingereicht haben. |
| [[!UICONTROL Search Engine Optimization]](product-search-engine-optimization.md) | Gibt den URL-Schlüssel und die Metadatenfelder an, die von Suchmaschinen zum Indizieren des Produkts verwendet werden. |
| [[!UICONTROL Related Products, Up-Sells, and Cross-Sells]](related-products-up-sells-cross-sells.md) | Wird verwendet, um einfache Werbeblöcke auf der Storefront einzurichten, die eine Auswahl zusätzlicher Produkte darstellen, die für den Kunden von Interesse sein könnten. |
| [[!UICONTROL Customizable Options]](settings-advanced-custom-options.md) | Fügt anpassbare Optionen zu einem Produkt hinzu. |
| [[!UICONTROL Product in Websites]](settings-basic-websites.md) | Identifiziert jede Website, auf der das Produkt verfügbar ist, gemäß der Store-Hierarchie. |
| [[!UICONTROL Design]](settings-advanced-design.md) | Wird verwendet, um ein anderes Design auf die Produktseite anzuwenden, das Spaltenlayout zu ändern, festzulegen, wo Produktoptionen angezeigt werden, und geben Sie benutzerdefinierten XML-Code ein. |
| [[!UICONTROL Gift options]](product-gift-options.md) | Wird zum Aktivieren oder Deaktivieren einer Option für eine Geschenknachricht beim Checkout auf Produktebene verwendet. |
| [[!UICONTROL Product In Shared Catalogs]](../b2b/catalog-shared.md) | ![Adobe Commerce B2B](../assets/b2b.svg) (Nur verfügbar mit [Adobe Commerce B2B](../b2b/introduction.md)) Ermöglicht die Pflege freigegebener Kataloge mit benutzerdefinierten Preisen für verschiedene Unternehmen. |
| [[!UICONTROL Downloadable Information]](product-create-downloadable.md#step-5-complete-the-downloadable-information) | Wird zum Definieren der Parameter für den Produktdownload verwendet. |

{style="table-layout:auto"}

## Erweiterte Preise und Inventar

Klicken Sie auf den Link unterhalb von **[!UICONTROL Price]** und **[!UICONTROL Quantity]**, um auf die erweiterten Preis- und Lagerbestandseinstellungen zuzugreifen. Weitere Informationen finden Sie unter [Verwalten von Preisen](pricing-advanced.md) und [Inventory management](../inventory-management/introduction.md).
