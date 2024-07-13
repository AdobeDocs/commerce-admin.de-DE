---
title: Festlegen der gemeinsamen Preise und Struktur von Katalogen
description: Erfahren Sie mit Adobe Commerce B2B, wie Sie die Preise und die Struktur eines freigegebenen Katalogs einrichten.
exl-id: 67caf56f-1b31-44bb-98dc-ea6ea7d8a4d5
feature: B2B, Companies, Catalog Management
role: Admin
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '1305'
ht-degree: 0%

---

# Festlegen der gemeinsamen Preise und Struktur von Katalogen

Die Einrichtung der Preise und der Struktur eines freigegebenen Katalogs ist ein zweistufiger Prozess. Ihre aktuelle Position im Prozess wird durch eine Zahl in der Fortschrittsleiste am oberen Rand der Seite hervorgehoben. Sie können den anderen Schritt im Prozess jederzeit anzeigen, indem Sie auf die Fortschrittsleiste klicken. Wenn Sie z. B. an benutzerdefinierten Preisen arbeiten, sollten Sie zur Produktauswahlseite zurückkehren, um sie zu referenzieren. Klicken Sie einfach in der Fortschrittsleiste oben auf der Seite auf **[!UICONTROL Products]** und dann auf **[!UICONTROL Pricing]** , um zur benutzerspezifischen Preisseite zurückzukehren. Ihre Arbeit geht dabei nicht verloren.

![Produkte im Katalog](./assets/shared-catalog-products-workspace.png){width="700" zoomable="yes"}

In der standardmäßigen Kategorienstruktur ist die Stammkategorie der oberste Container und wird in den Beispieldaten als _Standardkategorie_ bezeichnet. Wenn freigegebene Kataloge aktiviert sind, verfügt die Kategoriestruktur jedoch über einen äußeren Container mit dem Namen _Stammkatalog_. Der Stammkatalog umfasst alle anderen Kategoriestrukturen, die im System vorhanden sind. Weitere Informationen finden Sie unter [Katalogumfang](../catalog/introduction.md#catalog-scope).

## Schritt 1: Öffnen Sie die Konfiguration der freigegebenen Katalogpreise und -struktur

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Catalog]** > **[!UICONTROL Shared Catalogs]**

1. Gehen Sie für den freigegebenen Katalog im Raster zur Spalte _[!UICONTROL Action]_und klicken Sie auf **[!UICONTROL Set Pricing and Structure]**.

   ![Festlegen der Preise und der Struktur für den freigegebenen Katalog](./assets/shared-catalog-set-pricing-structure.png){width="700" zoomable="yes"}

1. Wenn der freigegebene Katalog zum ersten Mal konfiguriert ist, klicken Sie auf **[!UICONTROL Configure]** , um mit den folgenden Schritten fortzufahren.

## Schritt 2: Auswählen der Produkte

Der erste Schritt in diesem Prozess besteht darin, die Produkte auszuwählen, die Sie in den freigegebenen Katalog aufnehmen möchten. Die Produktauswahlseite enthält den [Kategorienbaum](../catalog/category-create.md) auf der linken Seite und ein synchronisiertes Produktraster auf der rechten Seite. Wenn Sie auf eine Kategorie im Baum klicken, werden die Produkte in der Kategorie im Raster angezeigt.

Nur Kategorien mit ausgewählten Produkten werden in der [oberen Navigation](../catalog/navigation-top.md) angezeigt, wenn der freigegebene Katalog von der Storefront aus angezeigt wird. Standardmäßig sind nur die ersten drei Kategoriestufen in der Storefront-Navigation enthalten, nicht jedoch die Root-Kategorie.

1. Verwenden Sie die Auswahl **Store** , um den [Perimeter](../catalog/introduction.md#product-scope) der Konfiguration festzulegen.

   Der Umfang der Konfiguration kann nur festgelegt werden, bevor der freigegebene Katalog zum ersten Mal gespeichert wird. Wenn Sie die Produktauswahl später bearbeiten, ist die Store-Auswahl nicht mehr verfügbar.

   ![Store auswählen](./assets/shared-catalog-products-scope.png){width="600" zoomable="yes"}

1. Führen Sie im Kategoriebaum einen der folgenden Schritte aus:

   - Um alle Produkte einzubeziehen, klicken Sie auf **[!UICONTROL Select all]** oder aktivieren Sie das Kontrollkästchen der übergeordneten Kategorie.
   - Um bestimmte Produktkategorien einzubeziehen, aktivieren Sie das Kontrollkästchen jeder Kategorie, die Sie einbeziehen möchten.
   - Um ein einzelnes Produkt ein- oder auszuschließen, aktivieren oder deaktivieren Sie das Kontrollkästchen des Produkts.

   Die Notation unter jeder Kategorie im Baum zeigt die Anzahl der Produkte aus der Kategorie an, die derzeit im freigegebenen Katalog enthalten sind. Die Notation unter der [Stammkategorie](../catalog/category-root.md) zeigt die Gesamtanzahl der Produkte aus allen Kategorien, die derzeit für den freigegebenen Katalog ausgewählt sind.

1. Um Kategorieprodukte im Raster anzuzeigen, klicken Sie auf den Namen der Kategorie im Baum. Wenn eine Kategorie ausgewählt wird, geschieht Folgendes:

   - Der Umschalter in der ersten Spalte des Rasters ist für jedes ausgewählte Produkt auf die grüne Position _Ein_ eingestellt.
   - Wenn ein Produkt mehreren Kategorien zugewiesen ist und nicht in einer dieser Kategorien ausgewählt ist, bleibt es in den anderen Kategorien verfügbar und auch bei Verwendung der [Katalogsuche](../catalog/search.md).
   - Das System legt für die ausgewählten Produkte automatisch [Kategorieberechtigungen](../catalog/category-permissions.md) auf `Allow` fest.

1. Verwenden Sie bei Bedarf die Filter und andere Rastersteuerelemente, um die Produkte zu finden, die Sie in den freigegebenen Katalog aufnehmen möchten.

   Sie können einzelne Produkte einzeln auswählen oder auslassen, indem Sie in der ersten Spalte auf den Umschalter klicken.

   Wenn Sie eine Kategorie auswählen, die keine Produkte enthält, aber mit CMS-Inhalten oder einem externen Link verknüpft ist, wird diese in der oberen Navigation des Storefront angezeigt.

   Die Kategorieeinstellungen, die Sie vornehmen, werden erst dann dauerhaft in der Datenbank gespeichert, wenn die Konfiguration gespeichert wurde. Sie werden jedoch vorübergehend gespeichert, wenn Sie an der Struktur und den Preisen arbeiten.

1. Klicken Sie auf **[!UICONTROL Next]**.

   ![Produkte für Katalog auswählen](./assets/shared-catalog-select-products-step-1.png){width="600" zoomable="yes"}

## Schritt 3: Festlegen benutzerdefinierter Preise

Sie können die individuellen Preise für jedes Produkt festlegen oder das Steuerelement _[!UICONTROL Action]_verwenden, um benutzerdefinierte Preise als festen Betrag oder Prozentsatz für mehrere Produktdatensätze festzulegen.

- **[!UICONTROL Fixed]**: Gibt den endgültigen Produktpreis an. Wenn Sie beispielsweise einen Festpreis von 10,00 USD eingeben, liegt der Preis in der Storefront für das entsprechende Unternehmen bei 10,00 USD.

  >[!NOTE]
  >
  >Der Mindestwert zwischen dem Basispreis und dem eingegebenen Festwert wird als Endproduktpreis verwendet.

  >[!NOTE]
  >
  >**_Der feste Preis_** Die anpassbaren Optionen für das Produkt sind _nicht_ von den Regeln für Gruppenpreis, Tier-Preis, Sonderpreis oder Katalogpreis betroffen.

- **[!UICONTROL Percentage]**: Bestimmt den benutzerspezifischen Preis basierend auf dem Rabattprozentsatz. Um beispielsweise einen 10-Prozent-Rabatt anzubieten, setzen Sie den benutzerdefinierten Preistyp auf `Percentage` und geben Sie `10` ein. Der ermäßigte benutzerdefinierte Preis beträgt 90 Prozent des ursprünglichen Produktpreises.

Verwenden Sie die Spalte _[!UICONTROL Custom Price]_im Raster, um den Rabatt auf einen festen Betrag oder einen Prozentsatz für die folgenden Produktarten festzulegen:

- [Einfach](../catalog/product-create-simple.md) (einschließlich konfigurierbarer Produktvarianten)
- [Paket](../catalog/product-create-bundle.md)
- [herunterladbar](../catalog/product-create-downloadable.md)
- [Virtual](../catalog/product-create-virtual.md)

Die Spalte &quot;Benutzerdefinierter Preis&quot;ist für die Produkttypen [konfigurierbar](../catalog/product-create-configurable.md) und [gruppiert](../catalog/product-create-grouped.md) sowie für [Geschenkkarten](../catalog/product-gift-card-create.md) leer.

Die Auswahl der Produkte im Raster kann nicht von der Seite _Benutzerspezifische Preise_ geändert werden. Sie können jedoch die Fortschrittsanzeige oben auf der Seite verwenden, um zum vorherigen Schritt zurückzukehren und die Auswahl der Produkte zu ändern.

![Produkte für Katalog auswählen](./assets/shared-catalog-custome-prices-step-3.png){width="600" zoomable="yes"}

### Anwenden eines benutzerspezifischen Preises

1. Legen Sie bei einer Installation mit mehreren Sites **[!UICONTROL Website]** auf die Website fest, auf der die benutzerdefinierten Preise gelten.

   ![Website auswählen](./assets/shared-catalog-scope-pricing.png){width="600" zoomable="yes"}

1. Verwenden Sie eine der folgenden Methoden, um die Produkte auszuwählen, für die die benutzerdefinierten Preise gelten sollen.

   - Verwenden Sie den Kategoriebaum, um alle Produkte einer bestimmten Kategorie auszuwählen.
   - Setzen Sie das Steuerelement _[!UICONTROL Mass Actions]_in der Kopfzeile auf `Select All`.
   - Aktivieren Sie das Kontrollkästchen einzelner Produkte.

   Das Raster zeigt die Produkte in den aktuell ausgewählten Kategorien an und Sie können die Standardsteuerelemente verwenden, um Produkte zu finden und die Liste zu filtern.

   ![Alle auswählen](./assets/shared-catalog-custom-pricing-mass-actions.png){width="600" zoomable="yes"}

1. Setzen Sie **[!UICONTROL Actions]** auf einen der folgenden Werte:

   - `Set Discount` - Wendet einen Rabattprozentsatz auf alle ausgewählten Produkte an. Jeder betroffene Produktpreis wird als **_ermäßigter_** Preis angezeigt.
   - `Adjust Fixed Price` - Wendet einen festen Rabattprozentsatz auf alle ausgewählten Produkte an. Jeder betroffene Produktpreis wird als **_angepasster Festpreis_** angezeigt.

   ![Aktionssteuerung - Rabatt festlegen](./assets/shared-catalog-set-custom-prices-discount-action.png){width="600" zoomable="yes"}

1. Geben Sie bei Aufforderung den Rabatt oder die Preisanpassung ein und klicken Sie auf **[!UICONTROL Apply]**.

   ![Rabatt festlegen](./assets/shared-catalog-set-custom-prices-discount.png){width="400"}<br/>

   ![Festen Preis anpassen](./assets/shared-catalog-set-custom-fixed-prices.png){width="400"}

   Der Rabatt wird auf alle ausgewählten Produkte angewendet, und die Spalte _Benutzerdefinierter Preis_ gibt den angewendeten Rabatttyp und Betrag an.

   ![Spalte &quot;Benutzerspezifischer Preis&quot;mit Rabatt](./assets/shared-catalog-set-custom-prices-discount-applied.png){width="600" zoomable="yes"}

### Anwenden eines Ebenenpreises

[Mit dem Tier-Preis](../catalog/product-price-tier.md) können Sie einen Mengenrabatt für Produkte im freigegebenen Katalog anbieten. Die Spalte _Tierpreis_ des Rasters enthält einen Link zu den Optionen _Erweiterte Preise_ , die speziell für den freigegebenen Katalog gelten. Wenn das Produkt bereits Stufenpreise enthält, wird die Anzahl der vorhandenen Ebenen in Klammern nach dem Link angezeigt.

Die folgenden Anweisungen zeigen, wie Sie die Stufenpreise auf ein einzelnes Produkt anwenden. Informationen zum Anwenden von Tierpreisen auf mehrere Produkte finden Sie unter [Preise der Importstufe](../systems/data-import-price-tier.md).

1. Markieren Sie für das Produkt im Raster die Spalte _Tier Price_ und klicken Sie auf **[!UICONTROL Configure]**.

   ![Konfigurieren des Statuspreises](./assets/shared-catalog-tier-price-configure.png){width="600" zoomable="yes"}

1. Klicken Sie auf der Seite _Erweiterte Preise_ auf **[!UICONTROL Add Price]** und führen Sie folgende Schritte aus:

   ![Katalog- und Statuspreis](./assets/shared-catalog-tier-price-configure-add-price.png){width="600" zoomable="yes"}

   - Setzen Sie **[!UICONTROL Website]** auf die Website, auf der der Tier-Preis gilt.
   - Geben Sie die Menge des Produkts ein, das gekauft werden muss, um den Rabatt zu erhalten.
   - Setzen Sie **[!UICONTROL Price]** auf einen der folgenden Rabatttypen:
      - `Fixed`
      - `Discount`
   - Geben Sie den Rabattbetrag ein.
   - Um eine andere Ebene zu erfassen, klicken Sie auf **Preis hinzufügen** und wiederholen Sie den Prozess, um die nächste Ebene zu definieren.

   ![Mehrstufige Preise](./assets/shared-catalog-tier-price-configure-multiple-tiers.png){width="600" zoomable="yes"}

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Done]**.

   Im Raster wird die Anzahl der Ebenen in Klammern der Spalte _[!UICONTROL Tier Price]_angezeigt.

   ![Mehrere Ebenen](./assets/shared-catalog-tier-price-configure-parentheses.png){width="600" zoomable="yes"}

## Speichern Sie Struktur und Preise

Wenn die benutzerspezifische Preisgestaltung abgeschlossen ist, klicken Sie auf **[!UICONTROL Generate Catalog]** und dann auf **[!UICONTROL Save]**.

Der freigegebene Katalog wird jetzt in der Datenbank gespeichert. Sein Name erscheint in der Spalte _[!UICONTROL Shared Catalog]_des Rasters_[!UICONTROL Products]_ . Der nächste Schritt besteht darin, [den freigegebenen Katalog einem Unternehmen zuzuweisen](./catalog-shared-assign-companies.md).
