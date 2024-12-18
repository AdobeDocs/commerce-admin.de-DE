---
title: Sonderpreise
description: Erfahren Sie, wie Sie Sonderpreise für einen bestimmten Zeitraum anbieten können.
exl-id: 4a1e2045-f0a8-4bae-a5a3-8ce8b258b217
feature: Catalog Management, Products
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '857'
ht-degree: 0%

---

# Sonderpreise

Für einen bestimmten Zeitraum kann ein Sonderpreis angeboten werden. Während des angegebenen Zeitraums wird der Sonderpreis anstelle des regulären Preises angezeigt, gefolgt von einer Notation, die den regulären Preis anzeigt.

![Sonderpreis auf einer Produktseite](./assets/storefront-price-special.png){width="700" zoomable="yes"}

## Speziellen Preis auf ein einzelnes Produkt anwenden

Sie können im Katalog einfach einen Sonderpreis für ein einzelnes Produkt festlegen.

### Geplantes Update verwenden

{{ee-feature}}

Adobe Commerce unterstützt [geplante Updates](../content-design/content-staging-scheduled-update.md). Verwenden Sie diese Werbeinstrumente, um für einen bestimmten Zeitraum einen Sonderpreis auf ein bestimmtes Produkt anzuwenden.

1. Öffnen Sie das Produkt im Bearbeitungsmodus.

1. Klicken Sie auf **[!UICONTROL Scheduled Update]**.

   ![Geplantes Update für Produkt hinzufügen](./assets/product-schedule-new-update.png){width="600" zoomable="yes"}

1. Geben **unter &quot;** aktualisieren“ einen Namen für die Sonderpreisaktion ein.

1. Geben Sie einen kurzen **[!UICONTROL Description]** ein.

1. Verwenden Sie das Symbol _Kalender_ ( ![Kalendersymbol](../assets/icon-calendar.png) ), um die **[!UICONTROL Start Date]** und **[!UICONTROL End Date]** für die Sonderpreisaktion auszuwählen.

   Mit den Schiebereglern **[!UICONTROL Hour]** und **[!UICONTROL Minute]** können Sie auch die Start- und Endzeit auswählen. Klicken Sie bei festgelegtem Start- und Endpunkt auf **[!UICONTROL Close]** .

   ![Als neues Update speichern](./assets/product-price-special-scheduled-update.png){width="600" zoomable="yes"}

1. Scrollen Sie nach unten zum Feld _Preis_, klicken Sie auf **[!UICONTROL Advanced Pricing]** und geben Sie den Betrag der **[!UICONTROL Special Price]** ein, die gemäß der geplanten Aktualisierung angewendet werden sollen.

   ![Besondere Preiseinstellungen](./assets/product-price-special.png){width="600" zoomable="yes"}

1. Klicken Sie abschließend auf **[!UICONTROL Done]** und dann auf **[!DNL Save]**.

   In der Storefront sollte der Sonderpreis sowohl in der Katalogliste als auch auf der Produktseite angezeigt werden.

   Die _[!UICONTROL Scheduled Change]_wird oben auf der Seite angezeigt.

   ![Geplante Änderung](./assets/product-price-special-scheduled-change.png){width="600" zoomable="yes"}

### Einfaches Start- und Enddatum verwenden

{{ce-feature}}

Die Magento Open Source umfasst einfache Start- und Enddatumsoptionen in den erweiterten Preisoptionen.

1. Öffnen Sie das Produkt im Bearbeitungsmodus.

1. Scrollen Sie nach unten zum Feld _[!UICONTROL Price]_, klicken Sie auf **[!UICONTROL Advanced Pricing]**und geben Sie den **[!UICONTROL Special Price]**ein.

1. Verwenden Sie das Symbol _Kalender_ ( ![Kalendersymbol](../assets/icon-calendar.png) ), um die **[!UICONTROL Start Date]** und **[!UICONTROL End Date]** für die Sonderpreisaktion auszuwählen.

   Der Sonderpreis gilt unmittelbar nach Mitternacht zu Beginn des Startdatums (00:01) und gilt bis kurz vor Mitternacht (23:59) am Tag vor dem Enddatum.

   ![Geplante Änderung](./assets/product-special-price-from-ce.png){width="600" zoomable="yes"}

1. Klicken Sie abschließend auf **[!UICONTROL Done]** und dann auf **[!UICONTROL Save]**.

   In der Storefront sollte der Sonderpreis sowohl in der Katalogliste als auch auf der Produktseite angezeigt werden.

## Auf mehrere Produkte einen Sonderpreis anwenden

Sie können auch mehreren Produkten einen Sonderpreis zuweisen, z. B. mehreren Varianten eines [konfigurierbaren Produkts](product-create-configurable.md).

### Für ausgewählte Produkte einen Sonderpreis festlegen

{{ee-feature}}

Das folgende Beispiel zeigt, wie Sie mehreren Produktvarianten eines konfigurierbaren Produkts in Adobe Commerce denselben Sonderpreis zuweisen.

1. Klicken Sie auf der Seite _[!UICONTROL Products]_auf **[!UICONTROL Filters]**und geben Sie die **[!UICONTROL Name]**des konfigurierbaren Produkts ein.

1. Legen Sie **[!UICONTROL Type]** auf `Configurable Product` fest und klicken Sie auf **[!UICONTROL Apply Filters]**.

1. Wenn Sie allen Produkten denselben Sonderpreis zuweisen möchten, setzen Sie das Steuerelement in der Kopfzeile der ersten Spalte auf `Select All`.

   Alternativ können Sie das Kontrollkästchen jedes Produkts aktivieren, das Sie einbeziehen möchten.

1. Setzen Sie das **[!UICONTROL Actions]** auf `Update attributes`.

1. Scrollen Sie nach unten zum Feld _[!UICONTROL Special Price]_und aktivieren Sie das Kontrollkästchen **[!UICONTROL Change]**unter dem Feld_[!UICONTROL Special Price]_ und geben Sie den Sonderpreis ein, den Sie anbieten möchten.

   ![Sonderpreisfelder](./assets/product-price-special-commerce.png){width="600" zoomable="yes"}

1. Klicken Sie abschließend auf **[!UICONTROL Save]**.

Der im Shop verfügbare Sonderpreis erscheint in den Katalogen und auf der Produktseite. Für ein konfigurierbares Produkt wird der reguläre Preis auch auf der Produktseite angezeigt, wenn die Optionen ausgewählt sind.

### Speziellen Preis und Datumsbereich für ausgewählte Produkte festlegen

{{ce-feature}}

Das folgende Beispiel zeigt, wie Sie in Magento Open Source mehreren Produktvarianten eines konfigurierbaren Produkts denselben Sonderpreis zuweisen.

1. Navigieren Sie in der _Admin_-Seitenleiste zu **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Klicken Sie auf **[!UICONTROL Filters]**.

1. Geben Sie den **[!UICONTROL Name]** des konfigurierbaren Produkts ein.

1. Legen Sie **[!UICONTROL Type]** auf `Simple Product` fest.

   ![Filter](./assets/product-price-special-filter.png){width="600" zoomable="yes"}

1. Klicken Sie auf **[!UICONTROL Apply Filters]**.

   Das Raster listet alle einfachen Produkte auf, die als Varianten des konfigurierbaren Produkts zugeordnet sind.

1. Wenn Sie allen Produkten denselben Sonderpreis zuweisen möchten, setzen Sie das Steuerelement in der Kopfzeile der ersten Spalte auf `Select All`.

   Alternativ können Sie das Kontrollkästchen jedes Produkts aktivieren, das Sie einbeziehen möchten.

1. Setzen Sie das **[!UICONTROL Actions]** auf `Update attributes`.

   ![Attribute aktualisieren](./assets/product-price-special-action-update-attributes-ce.png){width="600" zoomable="yes"}

1. Scrollen Sie nach unten zum Feld _[!UICONTROL Special Price]** und führen Sie folgende Schritte aus:

   - Aktivieren Sie das Kontrollkästchen **[!UICONTROL Change]** unter dem Feld _[!UICONTROL Special Price]** und geben Sie den gewünschten Sonderpreis ein.

   - Aktivieren Sie das Kontrollkästchen **[!UICONTROL Change]** unter dem Feld _Sonderpreis ab Datum_, klicken Sie auf _Kalender_ ( ![Kalendersymbol](../assets/icon-calendar.png) ) und wählen Sie das erste Datum der Sonderpreisaktion aus.

     Der Sonderpreis gilt unmittelbar nach Mitternacht zu Beginn des Startdatums (00:01) und gilt bis kurz vor Mitternacht (23:59) am Tag vor dem Enddatum.

   - Aktivieren Sie das Kontrollkästchen **[!UICONTROL Change]** unter dem Feld _Sonderpreis bis Datum_, klicken Sie auf _Kalender_ ( ![Kalendersymbol](../assets/icon-calendar.png) ) und wählen Sie das letzte Datum der Sonderpreisaktion aus.

   ![Sonderpreisfelder](./assets/product-price-special-action-update-attributes-fields-ce.png){width="600" zoomable="yes"}

1. Klicken Sie abschließend auf **[!UICONTROL Save]**.

   Eine Meldung gibt an, wie viele Datensätze mit dem Sonderpreis aktualisiert wurden.

   Der Sonderpreis ist ab dem angegebenen Datum im Shop erhältlich und wird in Katalogen und auf der Produktseite angezeigt. Für ein konfigurierbares Produkt wird der reguläre Preis auch auf der Produktseite angezeigt, wenn die Optionen ausgewählt sind.

   ![Sonderpreis für konfigurierbares Produkt](./assets/storefront-special-price-configurable-product-detail.png){width="600" zoomable="yes"}

## Test läuft

Wenn der Sonderpreis nicht korrekt in der Storefront sowohl auf der Katalogliste als auch auf den Produktseiten angezeigt wird, löschen Sie Ihren Browser-Cache:

1. Navigieren Sie in der _Admin_-Seitenleiste zu **[!UICONTROL System]** > **[!UICONTROL Cache Management]**.

1. Klicken Sie auf **[!UICONTROL Flush Magento Cache]**.

>[!NOTE]
>
>Der **_Endpreis_** der Ware wird als **_Mindestpreis_** berechnet, und zwar nach folgender Formel: <br/>`Final Price=Min(Regular(Base) Price, Group(Tier) Price, Special Price, Catalog Price Rule) + Sum(Min Price per each required custom option)`

>[!NOTE]
>
>**_Festpreis_** Anpassbare Produktoptionen werden _nicht_ durch Gruppenpreis-, Stufenpreis-, Sonderpreis- oder Katalogpreisregeln beeinflusst.
