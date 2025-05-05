---
title: Bestellung nach SKU
description: Erfahren Sie, wie Sie Ihren Shop so konfigurieren, dass er die Bestellung nach SKU unterstützt, um es Ihren Kunden zu erleichtern.
exl-id: cb39554f-ab76-46d5-8217-e43bc8f9f88d
feature: Orders, Storefront, Configuration
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '586'
ht-degree: 0%

---

# Bestellung nach SKU

{{ee-feature}}

Eine „SKU“ ist eine „Stock Keeping Unit“. SKUs helfen Online-Verkäufern in der Regel dabei, die wichtigsten Produktmerkmale zu identifizieren, z. B.: Größe, Farbe, Preis und Material. Produkt-IDs unterscheiden sich von SKUs:

- Die `Product ID` ist eine sequenzielle Zahlenreihe, die intern zur Identifizierung von Produkten verwendet wird und nicht für Kunden verfügbar ist.
- Die `SKU` wird vom Verkäufer generiert, normalerweise basierend auf dem Produktnamen und den Attributen für Marketing oder internes Tracking. Zum Beispiel: Ein blaues Baumwoll-T-Shirt, Größe mittel: T-COT-MED-BL. Die SKU kann vom Verkäufer bei Bedarf geändert werden.

Normalerweise enthält eine SKU eine Reihe von Abkürzungen, die die unterschiedlichen Merkmale des Produkts angeben. Die maximale SKU-Länge beträgt 64 Zeichen. SKUs sind wichtig, um Inventar effektiv zu verfolgen und zu verwalten. Daher ist ihre korrekte Einrichtung für E-Commerce entscheidend.

_Order by SKU_ ist ein [Widget](../content-design/widgets.md) das im Store als Komfort für alle Käufer angezeigt oder nur für Käufer in bestimmten Kundengruppen verfügbar gemacht werden kann. Käufer können entweder die SKU- und Mengeninformationen direkt in den Block „Bestellung nach SKU“ eingeben oder eine CSV-Datei von ihrem Kundenkonto hochladen. Unabhängig von der Konfiguration ist „Bestellung nach SKU“ für Speicheradministratoren immer verfügbar.

![Bestellung nach SKU in der Storefront](./assets/storefront-order-by-sku.png){width="700" zoomable="yes"}

## Bestellung nach SKU konfigurieren

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich den Abschnitt **[!UICONTROL Sales]** und wählen Sie darunter **[!UICONTROL Sales]**.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Order by SKU Settings]** .

1. Legen Sie **[!UICONTROL Enable Order by SKU on my Account in Storefront]** auf eine der folgenden Einstellungen fest:

   - `Yes, for Everyone` - Der Block „Bestellung nach SKU“ ist im Shop für jeden Käufer verfügbar.
   - `Yes, for Specified Customer Groups` - Bestellung nach SKU ist nur für Mitglieder einer bestimmten Kundengruppe verfügbar, z. B. `Wholesale`.
   - `No` - Der Block „Bestellung nach SKU“ wird nicht in der Storefront angezeigt und die Seite „Bestellung nach SKU“ ist nicht im Kundenkonto verfügbar.

   ![Sortieren nach SKU-Einstellungen](../configuration-reference/sales/assets/sales-order-by-sku-settings.png){width="600" zoomable="yes"}

1. Klicken Sie auf **[!UICONTROL Save Config]**.

![Adobe Commerce B2B](../assets/b2b.svg) (nur Adobe Commerce B2B) _&#x200B;**Um die Funktion „Bestellung nach SKU“ zu aktivieren, deaktivieren Sie die Funktion „Schnellbestellung“:**&#x200B;_

1. Navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Wählen Sie im linken Bedienfeld unter _[!UICONTROL General]_&#x200B;die Option **[!UICONTROL B2B Features]**

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL B2B Features]** .

1. Legen Sie **[!UICONTROL Enable Quick Order]** auf `No` fest.

   Mit [ Funktion „Schnellbestellung](../b2b/quick-order.md) können Kunden und Gäste schnell Bestellungen basierend auf der SKU oder dem Produktnamen aufgeben.

## Storefront-Erlebnis

Wenn die Funktion für den Store konfiguriert ist, können Kunden von jeder Seite, die das Widget &quot;_nach SKU“_, oder von ihrem Konto-Dashboard aus eine Bestellung nach SKU aufgeben.

### Bestellung nach SKU aus dem Seitenblock

1. Im _„Bestellung nach SKU_ gibt der Kunde die **[!UICONTROL SKU]** und **[!UICONTROL Qty]** des zu bestellenden Artikels ein.

1. Um ein weiteres Element hinzuzufügen, klicken Sie auf **[!UICONTROL Add Row]** und wiederholen Sie den Vorgang.

1. Klicks **[!UICONTROL Add to Cart]**.

### Bestellung nach SKU über ein Kundenkonto

1. In der Storefront meldet sich der Kunde bei seinem Konto an.

1. Wählen Sie im Bedienfeld links **[!UICONTROL Order by SKU]** aus.

1. Fügt einzelne Elemente entsprechend den Voreinstellungen hinzu:

   _&#x200B;**Fügt jedes Element nach SKU hinzu:**&#x200B;_

   - Gibt den **[!UICONTROL SKU]** und die **[!UICONTROL Qty]** des zu bestellenden Artikels ein.

   - Um ggf. weitere Elemente hinzuzufügen, klicken Sie auf _Zeile hinzufügen_ ![Plus-](../assets/button-add-item.png) und wiederholt dies für beliebig viele Elemente.

   - Klicks **[!UICONTROL Add to Cart]**.

   _&#x200B;**Lädt eine CSV-Datei mit mehreren Elementen hoch:**&#x200B;_

   - Bereitet eine [CSV-Datei (](../systems/data-csv.md)) mit Spalten für `SKU` und `Qty` vor.

   ![SKUs zum Importieren](./assets/account-dashboard-order-by-sku-import.png){width="500" zoomable="yes"}

   - Um die CSV-Datei hochzuladen, klicken Sie auf **[!UICONTROL Choose File]** und wählen Sie die hochzuladende Datei aus.

   - Klicks **[!UICONTROL Add to Cart]**.

   Wenn eines der Produkte zusätzliche Optionen bietet, wird der Kunde vom Warenkorb aufgefordert, das Produkt zu bearbeiten.

   ![Produkt erfordert Aufmerksamkeit](./assets/account-dashboard-order-by-sku-cart-product-requires-attention.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >Wenn doppelte SKUs vorhanden sind, werden die Mengen zu einem einzigen Zeileneintrag im Warenkorb zusammengefasst. Der Kunde kann die Menge jedes Artikels ändern und auf **[!UICONTROL Update Shopping Cart]** klicken, um die Gesamtwerte neu zu berechnen.

