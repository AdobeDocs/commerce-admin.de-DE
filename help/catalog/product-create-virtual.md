---
title: Virtuelles Produkt
description: Erfahren Sie, wie Sie ein virtuelles Produkt erstellen, das ein nicht greifbares Element darstellt, z. B. eine Mitgliedschaft, einen Service, eine Garantie oder ein Abonnement.
exl-id: 8788ba04-e911-429e-9e48-ce589f0c9fa1
feature: Catalog Management, Products
TQID: https://experienceleague.adobe.com/L981f0c-abmRqbEf3A-8CxTgVyzAuN-u1WDuMZAKSP4
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c18ed297-2187-4aec-affb-9d9654eca6fc
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 653
ht-degree: 0%

---

# Virtuelles Produkt

Virtuelle Produkte oder digitale Güter stellen immaterielle Gegenstände dar, wie Mitgliedschaften, Dienstleistungen, Gewährleistungen oder Abonnements und digitale Downloads von Büchern, Musik, Videos oder anderen Produkten. Virtuelle Produkte können einzeln verkauft oder als Teil der Produkttypen [Gruppiertes Produkt](product-create-grouped.md), [Konfigurierbares Produkt](product-create-configurable.md) oder [Bundle-](product-create-bundle.md) enthalten werden.

Abgesehen davon, dass das Feld _[!UICONTROL Weight]_&#x200B;nicht vorhanden ist, ist der Prozess der Erstellung eines virtuellen Produkts und eines einfachen Produkts identisch. Die folgenden Anweisungen zeigen den Prozess der Erstellung eines virtuellen Produkts mithilfe einer [Produktvorlage](attribute-sets.md), erforderlichen Feldern und grundlegenden Einstellungen. Wenn Sie die Grundlagen fertig gestellt haben, können Sie die anderen Produkteinstellungen nach Bedarf abschließen.

>[!NOTE]
>
>PayPal unterstützt den Verkauf digitaler Waren über den PayPal Express Checkout nicht mehr. Es wird empfohlen, entweder [PayPal Payments Standard](../stores-purchase/paypal-payments-standard.md) oder ein anderes PayPal-Zahlungs-Gateway zur Verarbeitung von Bestellungen zu verwenden, die virtuelle Produkte enthalten.

![Virtuelles Produkt](./assets/product-virtual-membership.png){width="700" zoomable="yes"}

## Schritt 1: Produkttyp auswählen

1. Navigieren Sie in der _Admin_-Seitenleiste zu **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Wählen Sie im Menü _[!UICONTROL Add Product]_![Menüpfeil](../assets/icon-menu-down-arrow-red.png){width="25"} oben rechts **[!UICONTROL Virtual Product]**&#x200B;aus.

   ![Virtuelles Produkt hinzufügen](./assets/product-add-virtual.png){width="700" zoomable="yes"}

## Schritt 2: Attributsatz auswählen

Um den [Attributsatz](attribute-sets.md) auszuwählen, der als Vorlage für das Produkt verwendet wird, führen Sie einen der folgenden Schritte aus:

- Klicken Sie in das Feld **[!UICONTROL Attribute Set]** und geben Sie den vollständigen Namen des Attributsatzes oder einen Teil davon ein.

- Wählen Sie in der angezeigten Liste das Attributset aus, das Sie verwenden möchten.

Das Formular wird mit der Änderung aktualisiert.

![Attributsatz auswählen](./assets/product-create-choose-attribute-set.png){width="600" zoomable="yes"}

## Schritt 3: Erforderliche Einstellungen vornehmen

1. Geben Sie die **[!UICONTROL Product Name]** ein.

1. Akzeptieren Sie die **[!UICONTROL SKU]**, die auf dem Produktnamen basiert, oder geben Sie einen anderen ein.

1. Geben Sie die **[!UICONTROL Price]** ein.

1. Da das Produkt noch nicht zur Veröffentlichung bereit ist, setzen Sie **[!UICONTROL Enable Product]** auf `No`.

1. Klicken Sie auf **[!UICONTROL Save]** und fahren Sie fort.

   Wenn das Produkt gespeichert wird, wird [&#x200B; Auswahl „Store](introduction.md#product-scope)Ansicht“ in der oberen linken Ecke angezeigt.

1. Wählen Sie die **[!UICONTROL Store View]** aus, in der das Produkt verfügbar sein soll.

   ![Store-Ansicht auswählen](./assets/product-create-store-view-choose.png){width="600" zoomable="yes"}

## Schritt 4: Vervollständigen Sie die Grundeinstellungen

1. Legen Sie **[!UICONTROL Tax Class]** auf eine der folgenden Einstellungen fest:

   - `None`
   - `Taxable Goods`

1. Geben Sie die **[!UICONTROL Quantity]** des Produkts ein, das auf Lager ist, und führen Sie folgende Schritte aus:

   - Akzeptieren Sie die **[!UICONTROL Stock Status]** Standardeinstellung von `In Stock`.

     Da ein virtuelles Produkt nicht bereitgestellt wird, wird das Feld **[!UICONTROL Weight]** nicht verwendet.

   - Akzeptieren Sie die **[!UICONTROL Visibility]** Standardeinstellung von `Catalog, Search`.

   >[!NOTE]
   >
   >Wenn Sie [Inventory management](../inventory-management/introduction.md) aktivieren, legen Händler mit einer Bezugsquelle die Menge in diesem Abschnitt fest. Händler mit mehreren Quellen fügen im Abschnitt Quellen Quellen Quellen Quellen und Mengen hinzu. Siehe folgenden Abschnitt _Zuweisen von Quellen und Mengen (Inventory management_.

1. Um dem Produkt **[!UICONTROL Categories]** zuzuweisen, klicken Sie auf das **[!UICONTROL Select…]** und führen Sie einen der folgenden Schritte aus:

   **Vorhandene Kategorie auswählen**:

   - Beginnen Sie mit der Eingabe in das Feld, bis Sie eine Übereinstimmung finden.

   - Aktivieren Sie das Kontrollkästchen der Kategorie, die zugewiesen werden soll.

   **Erstellen einer Kategorie**:

   - Klicken Sie auf **[!UICONTROL New Category]**.

   - Geben Sie die **[!UICONTROL Category Name]** ein und wählen Sie die **[!UICONTROL Parent Category]** aus, die ihre Position in der Menüstruktur bestimmt.

   - Klicken Sie auf **[!UICONTROL Create Category]**.

   Möglicherweise gibt es zusätzliche individuelle Attribute, die das Produkt beschreiben. Die Auswahl variiert je nach Attributsatz, und Sie können sie später abschließen.

### Zuweisen von Quellen und Mengen ([!DNL Inventory Management])

{{$include /help/_includes/inventory-assign-sources.md}}

## Schritt 5: Füllen Sie die Produktinformationen aus

Füllen Sie die Informationen in den folgenden Abschnitten nach Bedarf aus:

- [Inhalt](product-content.md)
- [Bilder und Videos](product-images-and-video.md)
- [Suchmaschinenoptimierung](product-search-engine-optimization.md)
- [Ähnliche Produkte, Upsell und Crosssell](related-products-up-sells-cross-sells.md)
- [Anpassbare Optionen](settings-advanced-custom-options.md)
- [Produkte in Websites](settings-basic-websites.md)
- [Design](settings-advanced-design.md)
- [Geschenkoptionen](product-gift-options.md)

>[!NOTE]
>
>Die Option _[!UICONTROL Is this downloadable product?]_&#x200B;ist standardmäßig deaktiviert. Durch Aktivierung dieser Funktion für ein virtuelles Produkt wird das Produkt [herunterladbar](product-create-downloadable.md#downloadable-product).

## Schritt 6: Produkt veröffentlichen

1. Wenn Sie bereit sind, das Produkt im Katalog zu veröffentlichen, legen Sie **[!UICONTROL Enable Product]** auf `Yes` fest.

1. Führen Sie einen der folgenden Schritte aus:

   - **Methode 1: Speichern** Vorschau

      - Klicken Sie oben rechts auf **[!UICONTROL Save]**.

      - Um das Produkt in Ihrem Geschäft anzuzeigen, wählen Sie **[!UICONTROL Customer View]** im Menü _Admin_ ( ![Menüpfeil](../assets/icon-menu-down-arrow-black.png) ).

     Der Store wird in einer neuen Browser-Registerkarte geöffnet.

     ![Kundenansicht](./assets/product-admin-customer-view.png){width="600" zoomable="yes"}

   - **Methode 2:** Speichern und schließen

     Wählen Sie im Menü _[!UICONTROL Save]_(![Menüpfeil](../assets/icon-menu-down-arrow-red.png){width="25"} ) die Option **[!UICONTROL Save & Close]**.

## Zu beachtende Dinge

- Virtuelle Produkte werden für nicht materielle Produkte wie Services, Abonnements und Gewährleistungen verwendet.

- Virtuelle Produkte sind ähnlich wie einfache Produkte, aber ohne Gewicht.

- Versandoptionen werden beim Checkout nur angezeigt, wenn sich ein greifbares Produkt im Warenkorb befindet.

<!-- Last updated from includes: 2023-05-19 17:14:58 -->
