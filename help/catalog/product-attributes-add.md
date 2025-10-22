---
title: Hinzufügen von Attributen zu einem Produkt
description: Erfahren Sie, wie Sie Attribute zu Produkten in Ihrem Katalog hinzufügen.
exl-id: 1f92807a-2362-48a2-8d3a-4aef90a5671f
feature: Catalog Management, Products
source-git-commit: 45d69ccc1a5a6a7b8d072465c19829a76dde826d
workflow-type: tm+mt
source-wordcount: '847'
ht-degree: 0%

---

# Hinzufügen von Attributen zu einem Produkt

Obwohl Attribute hauptsächlich über das Menü [Stores](../stores-purchase/stores-menu.md) verwaltet werden, können Sie bei der _an einem Produkt auch_ hinzufügen. Sie können aus der Liste der vorhandenen Attribute auswählen oder ein Attribut erstellen. Das neue Attribut wird zu dem [Attributsatz“ hinzugefügt](../catalog/attribute-sets.md) auf dem das Produkt basiert.

## Schritt 1: Attribut hinzufügen

1. Öffnen Sie das Produkt im Bearbeitungsmodus.

1. Klicken Sie oben rechts auf **[!UICONTROL Add Attribute]**.

   ![Neues Produkt mit festgelegtem Standardattribut](./assets/product-attribute-add.png){width="600" zoomable="yes"}

1. Um dem Produkt ein vorhandenes Attribut hinzuzufügen, verwenden Sie die [Filtersteuerelemente](../getting-started/admin-grid-controls.md), um das Attribut im Raster zu finden, und führen Sie folgende Schritte aus:

   - Aktivieren Sie das Kontrollkästchen in der ersten Spalte jedes hinzuzufügenden Attributs.

   - Klicken Sie auf **[!UICONTROL Add Selected]**.

   ![Attribut auswählen](./assets/product-attribute-add-select.png){width="600" zoomable="yes"}

1. Um ein neues Attribut zu definieren, klicken Sie auf **[!UICONTROL Create New Attribute]** und füllen Sie die Elemente in Schritt 2 aus.

## Schritt 2: Grundlegende Attributeigenschaften beschreiben

![Attributeigenschaften](./assets/product-attribute-add-new.png){width="600" zoomable="yes"}

1. Geben Sie unter _[!UICONTROL Attribute Properties]_&#x200B;ein **[!UICONTROL Attribute Label]**&#x200B;ein, um das Attribut zu identifizieren.

1. Legen Sie **[!UICONTROL Catalog Input Type for Store Owner]** auf den Typ des [Eingabedialogs](attributes-input-types.md) fest, der für die Dateneingabe verwendet werden soll.

   Wenn das Attribut für ein (konfigurierbares [) verwendet wird](product-create-configurable.md) wählen Sie `Dropdown`. Legen Sie dann **[!UICONTROL Required]** auf `Yes` fest.

1. Gehen Sie für die Eingabetypen `Dropdown` und `Multiple Select` wie folgt vor:

   - Klicken Sie unter **[!UICONTROL Values]** auf **[!UICONTROL Add Value]**.

   - Geben Sie den ersten Wert ein, der in der Liste angezeigt werden soll.

     Sie können einen Wert für den Administrator und eine Übersetzung des Werts für jede Shop-Ansicht eingeben. Wenn Sie nur eine Store-Ansicht haben, können Sie nur den Admin-Wert eingeben, der auch für die Storefront verwendet wird.

   - Klicken Sie auf **[!UICONTROL Add Value]** und wiederholen Sie den vorherigen Schritt für jede Option, die Sie in die Liste aufnehmen möchten.

   - Wählen Sie **[!UICONTROL Is Default]** aus, um die Option als Standardwert zu verwenden.

   ![Werte](./assets/product-attribute-add-values-colors.png){width="600" zoomable="yes"}

1. Wenn Sie möchten, dass der Kunde eine Option auswählt, bevor das Produkt gekauft werden kann, setzen Sie **[!UICONTROL Required]** auf `Yes`.

## Schritt 3: Erweiterte Eigenschaften beschreiben (optional)

![Erweiterte Attributeigenschaften](./assets/product-attribute-advanced-attribute-properties.png){width="600" zoomable="yes"}

1. Geben Sie einen eindeutigen **[!UICONTROL Attribute Code]** in Kleinbuchstaben und ohne Leerzeichen ein.

1. Legen Sie **[!UICONTROL Scope]** fest, um anzugeben, wo in der Store-Hierarchie das Attribut verwendet werden kann.

   Wenn das Attribut für ein (konfigurierbares [) verwendet wird](product-create-configurable.md) wählen Sie `Global`.

1. Wenn dieses Attribut nur für dieses Produkt gilt, setzen Sie **[!UICONTROL Unique Value]** auf `Yes`.

1. Legen Sie **[!UICONTROL Input Validation for Store Owner]** auf den Typ der Daten, die das Feld enthalten soll, fest, um die Gültigkeit aller in ein Textfeld eingegebenen Daten zu testen.

   Dieses Feld ist nicht für Eingabetypen mit ausgewählten Werten verfügbar. Die Eingabevalidierung kann für eine der folgenden Aktionen verwendet werden:

   - `Decimal Number`
   - `Integer Number`
   - `Email`
   - `URL`
   - `Letters`
   - `Letters (a-z, A-Z) or Numbers (0-9)`

   ![Eingabevalidierung](./assets/product-attribute-input-validation.png){width="500"}

1. Wenn Sie das Attribut als Spalte in das Produktraster einbeziehen möchten, setzen Sie **[!UICONTROL Add to Column Options]** auf `Yes`.

1. Wenn Sie das _[!UICONTROL Products]_&#x200B;nach dieser Spalte filtern können möchten, setzen Sie **[!UICONTROL Use in Filter Options]**&#x200B;auf `Yes`.

## Schritt 4: Feldbezeichnung eingeben

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Manage titles]** .

1. Geben Sie einen **[!UICONTROL Title]** ein, der als Titel für das Feld verwendet werden soll.

   Wenn Ihr Store in verschiedenen Sprachen verfügbar ist, können Sie für jede Ansicht einen übersetzten Titel eingeben.

   ![Titel verwalten](./assets/product-attribute-add-manage-titles.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   > Wenn Sie beabsichtigen, dieses Attribut als Facette in der Live-Suche zu verwenden, müssen Sie eine Store-spezifische Beschriftung angeben. Andernfalls wird der Attributname möglicherweise nicht korrekt auf der Seite zur Facettenkonfiguration angezeigt. Um die Konfiguration zu aktualisieren, bearbeiten Sie den Titel manuell mit der Option [Bearbeiten“ in der Facette Live Search](https://experienceleague.adobe.com/en/docs/commerce/live-search/live-search-admin/facets/facets-add#step-2-edit-facet-properties-optional) im _Live Search-Handbuch_.

## Schritt 5: Eigenschaften der Storefront beschreiben

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Storefront Properties]** .

   ![Storefront-Eigenschaften](./assets/product-attribute-add-storefront-properties.png){width="600" zoomable="yes"}

1. Um das Attribut für die Suche verfügbar zu machen, setzen Sie **[!UICONTROL Use in Search]** auf `Yes`.

1. Um das Attribut in den Produktvergleich aufzunehmen, setzen Sie **[!UICONTROL Comparable on Storefront]** auf `Yes`.

1. Um Dropdown-, Multiple-Select- oder Preis-Attribute in die mehrschichtige Navigation einzuschließen, legen Sie **[!UICONTROL Use in Search Results Layered Navigation]** auf eine der folgenden Einstellungen fest:

   - `Filterable (with results)` - Die mehrschichtige Navigation umfasst nur die Filter, für die passende Produkte gefunden werden können. Attributwerte, die bereits für alle in der Liste aufgeführten Produkte gelten, werden nicht als verfügbare Filter angezeigt. Attributwerte mit einer Anzahl von null (0) Produktübereinstimmungen werden auch in der Liste der verfügbaren Filter weggelassen.<br/><br/>Die gefilterte Liste von Produkten enthält nur die Produkte, die dem Filter entsprechen. Die Produktliste wird nur aktualisiert, wenn die ausgewählten Filter das Gezeigte ändern.

   - `Filterable (no results)` - Die mehrschichtige Navigation umfasst Filter für alle verfügbaren Attributwerte und ihre Produktanzahl, einschließlich der Produkte mit null (0) Produktübereinstimmungen. Wenn der Attributwert ein Farbfeld ist, wird der Wert als Filter angezeigt, aber durchgestrichen.

   >[!NOTE]
   >
   >Wenn die _[!UICONTROL Use in Search]_&#x200B;auf `No` festgelegt ist, wird die&#x200B;_[!UICONTROL Use in Search Results Layered Navigation]_ nicht angezeigt und das Produktattribut wird bei der Suche mit keinem [!UICONTROL Use in Layered Navigation] Einstellwert verwendet.

1. Um das -Attribut in der mehrschichtigen Navigation auf Suchergebnisseiten zu verwenden, setzen Sie **[!UICONTROL Use in Search Results Layered Navigation]** auf `Yes` und geben Sie eine Zahl in das Feld **[!UICONTROL Position]** ein.

   Die Positionsnummer gibt die relative Position des Attributs innerhalb des mehrschichtigen Navigationsblocks an.

   >[!NOTE]
   >
   >Das Feld _[!UICONTROL Position]_&#x200B;ist standardmäßig abgeblendet und Sie müssen das Attribut speichern, bevor Sie diese Einstellung ändern können.

1. Um das Attribut in Preisregeln zu verwenden, setzen Sie **[!UICONTROL Use for Promo Rule Conditions]** auf `Yes`.

1. Damit der Text mit HTML formatiert werden kann, legen Sie **[!UICONTROL Allow HTML Tags on Storefront]** auf `Yes` fest.

   Durch diese Einstellung wird der WYSIWYG-Editor beim Bearbeiten des Felds verfügbar.

1. Um das Attribut in die Produktseite aufzunehmen, setzen Sie **[!UICONTROL Visible on Catalog Pages on Storefront]** auf `Yes`.

1. Füllen Sie die folgenden Einstellungen wie vom Design unterstützt aus:

   - Um das Attribut in Produktlisten aufzunehmen, setzen Sie **[!UICONTROL Used in Product Listing]** auf `Yes`.

   - Um das -Attribut als Sortierparameter für Produktlisten zu verwenden, setzen Sie **[!UICONTROL Used for Sorting in Product Listing]** auf `Yes`.

1. Klicken Sie abschließend auf **[!UICONTROL Save Attribute]**.
