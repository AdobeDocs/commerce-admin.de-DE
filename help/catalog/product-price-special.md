---
title: Sonderpreise
description: Erfahren Sie, wie Sie Sonderpreise für einen festgelegten Zeitraum anbieten können.
exl-id: 4a1e2045-f0a8-4bae-a5a3-8ce8b258b217
feature: Catalog Management, Products
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '857'
ht-degree: 0%

---

# Sonderpreise

Ein Sonderpreis kann für einen bestimmten Zeitraum angeboten werden. Während des angegebenen Zeitraums wird der Sonderpreis anstelle des regulären Preises angezeigt, gefolgt von einer Notation, die den regulären Preis anzeigt.

![Sonderpreis auf einer Produktseite](./assets/storefront-price-special.png){width="700" zoomable="yes"}

## Sonderpreis auf ein einzelnes Produkt anwenden

Sie können einfach einen Sonderpreis für ein einzelnes Produkt im Katalog festlegen.

### Geplantes Update verwenden

{{ee-feature}}

Adobe Commerce unterstützt [geplante Updates](../content-design/content-staging-scheduled-update.md). Verwenden Sie diese Werbemittel, um einen Sonderpreis auf ein bestimmtes Produkt für einen bestimmten Zeitraum anzuwenden.

1. Öffnen Sie das Produkt im Bearbeitungsmodus.

1. Klicken Sie auf **[!UICONTROL Scheduled Update]**.

   ![Geplantes Update für Produkt hinzufügen](./assets/product-schedule-new-update.png){width="600" zoomable="yes"}

1. Geben Sie für **Name aktualisieren** einen Namen für die Sonderpreisaktion ein.

1. Geben Sie eine kurze **[!UICONTROL Description]** ein.

1. Verwenden Sie das Symbol _Kalender_ ( ![Kalendersymbol](../assets/icon-calendar.png) ), um die **[!UICONTROL Start Date]** und die **[!UICONTROL End Date]** für die Sonderpreisaktion auszuwählen.

   Sie können die Regler **[!UICONTROL Hour]** und **[!UICONTROL Minute]** auch verwenden, um die Start- und Endzeit auszuwählen. Klicken Sie auf **[!UICONTROL Close]** , wenn Start und Ende festgelegt sind.

   ![Als neues Update speichern](./assets/product-price-special-scheduled-update.png){width="600" zoomable="yes"}

1. Scrollen Sie nach unten zum Feld _Preis_ , klicken Sie auf **[!UICONTROL Advanced Pricing]** und geben Sie den Betrag der **[!UICONTROL Special Price]** ein, der gemäß der geplanten Aktualisierung angewendet werden soll.

   ![Besondere Preiseinstellungen](./assets/product-price-special.png){width="600" zoomable="yes"}

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Done]** und dann auf **[!DNL Save]**.

   In der Storefront sollte der Sonderpreis sowohl in der Katalogliste als auch auf der Produktseite angezeigt werden.

   Die _[!UICONTROL Scheduled Change]_wird oben auf der Seite angezeigt.

   ![Geplante Änderung](./assets/product-price-special-scheduled-change.png){width="600" zoomable="yes"}

### Einfaches Start- und Enddatum verwenden

{{ce-feature}}

Magento Open Source umfasst einfache Start- und Enddatumsoptionen in den erweiterten Preisoptionen.

1. Öffnen Sie das Produkt im Bearbeitungsmodus.

1. Scrollen Sie nach unten zum Feld _[!UICONTROL Price]_, klicken Sie auf **[!UICONTROL Advanced Pricing]**und geben Sie den Betrag **[!UICONTROL Special Price]**ein.

1. Verwenden Sie das Symbol _Kalender_ ( ![Kalendersymbol](../assets/icon-calendar.png) ), um die **[!UICONTROL Start Date]** und die **[!UICONTROL End Date]** für die Sonderpreisaktion auszuwählen.

   Der Sonderpreis tritt unmittelbar nach Mitternacht am Anfang des Startdatums (00:01) in Kraft und dauert bis kurz vor Mitternacht (23:59) am Tag vor dem Enddatum.

   ![Geplante Änderung](./assets/product-special-price-from-ce.png){width="600" zoomable="yes"}

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Done]** und dann auf **[!UICONTROL Save]**.

   In der Storefront sollte der Sonderpreis sowohl in der Katalogliste als auch auf der Produktseite angezeigt werden.

## Anwenden eines Sonderpreises auf mehrere Produkte

Sie können auch einen speziellen Preis für mehrere Produkte zuweisen, z. B. mehrere Varianten eines [konfigurierbaren Produkts](product-create-configurable.md).

### Festlegen eines Sonderpreises für ausgewählte Produkte

{{ee-feature}}

Das folgende Beispiel zeigt, wie Sie denselben Sonderpreis mehreren Produktvarianten eines konfigurierbaren Produkts in Adobe Commerce zuweisen.

1. Klicken Sie auf der Seite _[!UICONTROL Products]_auf **[!UICONTROL Filters]**und geben Sie die **[!UICONTROL Name]**des konfigurierbaren Produkts ein.

1. Setzen Sie **[!UICONTROL Type]** auf `Configurable Product` und klicken Sie auf **[!UICONTROL Apply Filters]**.

1. Wenn Sie allen Produkten denselben Sonderpreis zuweisen möchten, setzen Sie das Steuerelement in der Kopfzeile der ersten Spalte auf `Select All`.

   Alternativ können Sie das Kontrollkästchen jedes Produkts aktivieren, das Sie einbeziehen möchten.

1. Setzen Sie das Steuerelement **[!UICONTROL Actions]** auf `Update attributes`.

1. Scrollen Sie nach unten zum Feld _[!UICONTROL Special Price]_, aktivieren Sie das Kontrollkästchen **[!UICONTROL Change]**unter dem Feld_[!UICONTROL Special Price]_ und geben Sie den Sonderpreis ein, den Sie anbieten möchten.

   ![Felder für Sonderpreise](./assets/product-price-special-commerce.png){width="600" zoomable="yes"}

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save]**.

Der im Laden verfügbare Sonderpreis erscheint in den Kataloglisten und auf der Produktseite. Bei einem konfigurierbaren Produkt wird der reguläre Preis auch auf der Produktseite angezeigt, wenn die Optionen ausgewählt werden.

### Festlegen eines Sonderpreises und eines Datumsbereichs für ausgewählte Produkte

{{ce-feature}}

Das folgende Beispiel zeigt, wie Sie denselben Sonderpreis mehreren Produktvarianten eines konfigurierbaren Produkts in Magento Open Source zuweisen.

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Klicken Sie auf **[!UICONTROL Filters]**.

1. Geben Sie den **[!UICONTROL Name]** des konfigurierbaren Produkts ein.

1. Setzen Sie **[!UICONTROL Type]** auf `Simple Product`.

   ![Filter](./assets/product-price-special-filter.png){width="600" zoomable="yes"}

1. Klicken Sie auf **[!UICONTROL Apply Filters]**.

   Das Raster listet alle einfachen Produkte auf, die als Varianten des konfigurierbaren Produkts zugeordnet sind.

1. Wenn Sie allen Produkten denselben Sonderpreis zuweisen möchten, setzen Sie das Steuerelement in der Kopfzeile der ersten Spalte auf `Select All`.

   Alternativ können Sie das Kontrollkästchen jedes Produkts aktivieren, das Sie einbeziehen möchten.

1. Setzen Sie das Steuerelement **[!UICONTROL Actions]** auf `Update attributes`.

   ![Attribute aktualisieren](./assets/product-price-special-action-update-attributes-ce.png){width="600" zoomable="yes"}

1. Scrollen Sie nach unten zum Feld _[!UICONTROL Special Price]** und gehen Sie wie folgt vor:

   - Aktivieren Sie das Kontrollkästchen **[!UICONTROL Change]** unter dem Feld _[!UICONTROL Special Price]** und geben Sie den Sonderpreis ein, den Sie anbieten möchten.

   - Aktivieren Sie das Kontrollkästchen **[!UICONTROL Change]** unter dem Feld _Sonderpreis ab Datum_ , klicken Sie auf den _Kalender_ ( ![Kalendersymbol](../assets/icon-calendar.png) ) und wählen Sie das erste Datum der Sonderaktion.

     Der Sonderpreis tritt unmittelbar nach Mitternacht am Anfang des Startdatums (00:01) in Kraft und dauert bis kurz vor Mitternacht (23:59) am Tag vor dem Enddatum.

   - Aktivieren Sie das Kontrollkästchen **[!UICONTROL Change]** unter dem Feld _Sonderpreis bis Datum_ , klicken Sie auf den _Kalender_ ( ![Kalendersymbol](../assets/icon-calendar.png) ) und wählen Sie das letzte Datum der Sonderaktion &quot;Preisaktion&quot;.

   ![Spezielle Preisfelder](./assets/product-price-special-action-update-attributes-fields-ce.png){width="600" zoomable="yes"}

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save]**.

   Eine Meldung gibt an, wie viele Datensätze mit dem Sonderpreis aktualisiert wurden.

   Der Sonderpreis wird am angegebenen Datum im Store verfügbar und wird in den Kataloglisten und auf der Produktseite angezeigt. Bei einem konfigurierbaren Produkt wird der reguläre Preis auch auf der Produktseite angezeigt, wenn die Optionen ausgewählt werden.

   ![Sonderpreis für konfigurierbares Produkt](./assets/storefront-special-price-configurable-product-detail.png){width="600" zoomable="yes"}

## Test

Wenn der Sonderpreis sowohl auf der Katalogliste als auch auf den Produktseiten im Storefront nicht richtig angezeigt wird, löschen Sie Ihren Browser-Cache:

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL System]** > **[!UICONTROL Cache Management]**.

1. Klicken Sie auf **[!UICONTROL Flush Magento Cache]**.

>[!NOTE]
>
>Der Produktpreis **_final_** wird als relevanter Preis für **_Minimum_** anhand der folgenden Formel berechnet: <br/>`Final Price=Min(Regular(Base) Price, Group(Tier) Price, Special Price, Catalog Price Rule) + Sum(Min Price per each required custom option)`

>[!NOTE]
>
>**_Der feste Preis_** Die anpassbaren Optionen für das Produkt sind _nicht_ von den Regeln für Gruppenpreis, Tier-Preis, Sonderpreis oder Katalogpreis betroffen.
