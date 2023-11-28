---
title: Sonderpreise
description: Erfahren Sie, wie Sie Sonderpreise für einen festgelegten Zeitraum anbieten können.
exl-id: 4a1e2045-f0a8-4bae-a5a3-8ce8b258b217
feature: Catalog Management, Products
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '851'
ht-degree: 0%

---

# Sonderpreise

Ein Sonderpreis kann für einen bestimmten Zeitraum angeboten werden. Während des angegebenen Zeitraums wird der Sonderpreis anstelle des regulären Preises angezeigt, gefolgt von einer Notation, die den regulären Preis anzeigt.

![Sonderpreis auf einer Produktseite](./assets/storefront-price-special.png){width="700" zoomable="yes"}

## Sonderpreis auf ein einzelnes Produkt anwenden

Sie können einfach einen Sonderpreis für ein einzelnes Produkt im Katalog festlegen.

### Geplantes Update verwenden

{{ee-feature}}

Adobe Commerce unterstützt auch [Geplante Aktualisierungen](../content-design/content-staging-scheduled-update.md). Verwenden Sie diese Werbemittel, um einen Sonderpreis auf ein bestimmtes Produkt für einen bestimmten Zeitraum anzuwenden.

1. Öffnen Sie das Produkt im Bearbeitungsmodus.

1. Klicken **[!UICONTROL Scheduled Update]**.

   ![Geplantes Update für das Produkt hinzufügen](./assets/product-schedule-new-update.png){width="600" zoomable="yes"}

1. Für **Aktualisierungsname**, geben Sie einen Namen für die Sonderaktion an.

1. Kurzbeschreibung eingeben **[!UICONTROL Description]**.

1. Verwenden Sie die _Kalender_ ( ![Kalendersymbol](../assets/icon-calendar.png) ), um das **[!UICONTROL Start Date]** und **[!UICONTROL End Date]** für die Sonderpreisförderung.

   Sie können die **[!UICONTROL Hour]** und **[!UICONTROL Minute]** auch die Start- und Endzeit wählen. Klicks **[!UICONTROL Close]** wenn Start und Ende festgelegt sind.

   ![Als neues Update speichern](./assets/product-price-special-scheduled-update.png){width="600" zoomable="yes"}

1. Scrollen Sie nach unten zum _Preis_ Feld, klicken Sie auf **[!UICONTROL Advanced Pricing]** und geben Sie den Betrag der **[!UICONTROL Special Price]** entsprechend der geplanten Aktualisierung anzuwenden.

   ![Spezielle Preiseinstellungen](./assets/product-price-special.png){width="600" zoomable="yes"}

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Done]** und dann **[!DNL Save]**.

   In der Storefront sollte der Sonderpreis sowohl in der Katalogliste als auch auf der Produktseite angezeigt werden.

   Die _[!UICONTROL Scheduled Change]_wird oben auf der Seite angezeigt.

   ![Geplante Änderung](./assets/product-price-special-scheduled-change.png){width="600" zoomable="yes"}

### Einfaches Start- und Enddatum verwenden

{{ce-feature}}

Magento Open Source umfasst einfache Start- und Enddatumsoptionen in den erweiterten Preisoptionen.

1. Öffnen Sie das Produkt im Bearbeitungsmodus.

1. Scrollen Sie nach unten zum _[!UICONTROL Price]_Feld, klicken Sie auf **[!UICONTROL Advanced Pricing]**und geben Sie die **[!UICONTROL Special Price]**Betrag.

1. Verwenden Sie die _Kalender_ ( ![Kalendersymbol](../assets/icon-calendar.png) ), um das **[!UICONTROL Start Date]** und **[!UICONTROL End Date]** für die Sonderpreisförderung.

   Der Sonderpreis tritt unmittelbar nach Mitternacht am Anfang des Startdatums (00:01) in Kraft und dauert bis kurz vor Mitternacht (23:59) am Tag vor dem Enddatum.

   ![Geplante Änderung](./assets/product-special-price-from-ce.png){width="600" zoomable="yes"}

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Done]** und dann **[!UICONTROL Save]**.

   In der Storefront sollte der Sonderpreis sowohl in der Katalogliste als auch auf der Produktseite angezeigt werden.

## Anwenden eines Sonderpreises auf mehrere Produkte

Sie können auch einen Sonderpreis für mehrere Produkte zuweisen, z. B. mehrere Varianten einer [konfigurierbares Produkt](product-create-configurable.md).

### Festlegen eines Sonderpreises für ausgewählte Produkte

{{ee-feature}}

Das folgende Beispiel zeigt, wie Sie denselben Sonderpreis mehreren Produktvarianten eines konfigurierbaren Produkts in Adobe Commerce zuweisen.

1. Im _[!UICONTROL Products]_Seite, klicken **[!UICONTROL Filters]**und geben Sie die **[!UICONTROL Name]**des konfigurierbaren Produkts.

1. Satz **[!UICONTROL Type]** nach `Configurable Product` und klicken **[!UICONTROL Apply Filters]**.

1. Wenn Sie allen Produkten denselben Sonderpreis zuweisen möchten, setzen Sie das Steuerelement in der Kopfzeile der ersten Spalte auf . `Select All`.

   Alternativ können Sie das Kontrollkästchen jedes Produkts aktivieren, das Sie einbeziehen möchten.

1. Legen Sie die **[!UICONTROL Actions]** Kontrolle an `Update attributes`.

1. Scrollen Sie nach unten zum _[!UICONTROL Special Price]_und wählen Sie die **[!UICONTROL Change]**Kontrollkästchen unterhalb der_[!UICONTROL Special Price]_ und geben Sie den gewünschten Sonderpreis an.

   ![Felder für Sonderpreise](./assets/product-price-special-commerce.png){width="600" zoomable="yes"}

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save]**.

Der im Laden verfügbare Sonderpreis erscheint in den Kataloglisten und auf der Produktseite. Bei einem konfigurierbaren Produkt wird der reguläre Preis auch auf der Produktseite angezeigt, wenn die Optionen ausgewählt werden.

### Festlegen eines Sonderpreises und eines Datumsbereichs für ausgewählte Produkte

{{ce-feature}}

Das folgende Beispiel zeigt, wie Sie denselben Sonderpreis mehreren Produktvarianten eines konfigurierbaren Produkts in Magento Open Source zuweisen.

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Klicken **[!UICONTROL Filters]**.

1. Geben Sie die **[!UICONTROL Name]** des konfigurierbaren Produkts.

1. Satz **[!UICONTROL Type]** nach `Simple Product`.

   ![Filter](./assets/product-price-special-filter.png){width="600" zoomable="yes"}

1. Klicken **[!UICONTROL Apply Filters]**.

   Das Raster listet alle einfachen Produkte auf, die als Varianten des konfigurierbaren Produkts zugeordnet sind.

1. Wenn Sie allen Produkten denselben Sonderpreis zuweisen möchten, setzen Sie das Steuerelement in der Kopfzeile der ersten Spalte auf . `Select All`.

   Alternativ können Sie das Kontrollkästchen jedes Produkts aktivieren, das Sie einbeziehen möchten.

1. Legen Sie die **[!UICONTROL Actions]** Kontrolle an `Update attributes`.

   ![Attribute aktualisieren](./assets/product-price-special-action-update-attributes-ce.png){width="600" zoomable="yes"}

1. Scrollen Sie nach unten zum _[!UICONTROL Special Price]** und führen Sie folgende Schritte aus:

   - Wählen Sie die **[!UICONTROL Change]** Kontrollkästchen unterhalb von _[!UICONTROL Special Price]** und geben Sie den Sonderpreis ein, den Sie anbieten möchten.

   - Wählen Sie die **[!UICONTROL Change]** Kontrollkästchen unterhalb der _Sonderpreis ab Datum_ und klicken Sie auf das _Kalender_ ( ![Kalendersymbol](../assets/icon-calendar.png) ), und wählen Sie das erste Datum der Sonderaktion.

     Der Sonderpreis tritt unmittelbar nach Mitternacht am Anfang des Startdatums (00:01) in Kraft und dauert bis kurz vor Mitternacht (23:59) am Tag vor dem Enddatum.

   - Wählen Sie die **[!UICONTROL Change]** Kontrollkästchen unterhalb der _Sonderpreis bis zum Datum_ und klicken Sie auf das _Kalender_ ( ![Kalendersymbol](../assets/icon-calendar.png) ), und wählen Sie das letzte Datum der Sonderaktion.

   ![Spezielle Preisfelder](./assets/product-price-special-action-update-attributes-fields-ce.png){width="600" zoomable="yes"}

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save]**.

   Eine Meldung gibt an, wie viele Datensätze mit dem Sonderpreis aktualisiert wurden.

   Der Sonderpreis wird am angegebenen Datum im Store verfügbar und wird in den Kataloglisten und auf der Produktseite angezeigt. Bei einem konfigurierbaren Produkt wird der reguläre Preis auch auf der Produktseite angezeigt, wenn die Optionen ausgewählt werden.

   ![Sonderpreis für konfigurierbares Produkt](./assets/storefront-special-price-configurable-product-detail.png){width="600" zoomable="yes"}

## Test

Wenn der Sonderpreis sowohl auf der Katalogliste als auch auf den Produktseiten im Storefront nicht richtig angezeigt wird, löschen Sie Ihren Browser-Cache:

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL System]** > **[!UICONTROL Cache Management]**.

1. Klicken **[!UICONTROL Flush Magento Cache]**.

>[!NOTE]
>
>Die **_final_** Der Produktpreis wird als **_Minimum_** relevanter Preis nach folgender Formel: <br/>`Final Price=Min(Regular(Base) Price, Group(Tier) Price, Special Price, Catalog Price Rule) + Sum(Min Price per each required custom option)`

>[!NOTE]
>
>**_Festpreis_** Anpassbare Produktoptionen sind _not_ beeinflusst von den Regeln für Gruppenpreis, Tier-Preis, Sonderpreis oder Katalogpreis.
