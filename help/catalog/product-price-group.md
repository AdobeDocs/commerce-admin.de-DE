---
title: Preisgestaltung einer Gruppe
description: Erfahren Sie, wie Sie mithilfe von Gruppenpreisen Preise für ermäßigte Artikel basierend auf Kundengruppen in Ihrem Geschäft festlegen können.
exl-id: bc5be23f-64eb-47c3-beda-01168abfbf96
feature: Catalog Management, Products, Customers
TQID: 'https://experienceleague.adobe.com/OCeX5pLtUzWdwOW5W8qpI4DCeab2PTAVi5xF8HUr91A'
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
  - id: 22bad240-8308-569b-a9d5-578f1ff890ca
    internal-label: Customers
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
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: acc7571574eb9c7e96911266897350a77913488e
workflow-type: tm+mt
source-wordcount: '333'
ht-degree: 0%
---
# Preisgestaltung einer Gruppe

Sie können die Produktkonfigurationseinstellungen im Admin-Bereich verwenden, um Preise für ermäßigte Artikel basierend auf Kundengruppen in Ihrem Geschäft festzulegen. Dieses strategische Preismodell wird _Gruppenpreisfindung“_.

Der ermäßigte Preis eines Produkts kann Mitgliedern einer bestimmten Kundengruppe angeboten werden, wenn der Käufer in seinem Konto eingeloggt ist. Auf der Produktseite wird der Kundengruppenpreis zusammen mit dem regulären Preis angezeigt, sodass ein Käufer die Preise einfach vergleichen und entsprechend handeln kann. Nachdem der Kunde das Produkt zum Warenkorb hinzugefügt hat, wird der reguläre Preis durch den Gruppenpreis auf Basis der Kundengruppe ersetzt.

Die Preisgestaltung für Kundengruppen ist eine Komponente der [Preisstaffelung](product-price-tier.md) und wird auf ähnliche Weise festgelegt. Der einzige Unterschied besteht darin, dass die Preise der Kundengruppen eine Menge von 1 haben.

![Kundengruppenrabatt](./assets/storefront-price-group.png){width="600" zoomable="yes"}

## Vorteile der Verwendung von Gruppenpreisen

- Geeignet für Großabnehmer

- Anreiz für Kunden, ihre Kundengruppe zu aktualisieren, um Rabatte zu nutzen

- Gezielte Marketing-Kampagnen

- Aufbau von Vertrauen und Glaubwürdigkeit durch Belohnung treuer Kunden

## Gruppenpreis einrichten

1. Öffnen Sie das Produkt im Bearbeitungsmodus.

1. Klicken Sie unter dem Feld _[!UICONTROL Price]_auf **[!UICONTROL Advanced Pricing]**.

1. Klicken Sie im Abschnitt _[!UICONTROL Customer Group Price]_auf **[!UICONTROL Add]**.

   Wenn Ihr Store [Adobe Commerce B2B](../b2b/introduction.md) enthält und [freigegebene Kataloge](../b2b/catalog-shared.md) aktiviert hat, ist dieser Abschnitt _[!UICONTROL Catalog and Tier Price]_.

   ![Advanced Pricing](./assets/product-price-group.png){width="600" zoomable="yes"}

1. Konfigurieren Sie den Gruppenpreis:

   - Wählen Sie für eine Installation an mehreren Standorten die **[!UICONTROL Website]** aus, für die der Gruppenpreis gilt.

   - Wählen Sie die **[!UICONTROL Customer Group]** aus, die den Rabatt erhalten soll.

   - Geben Sie eine **[!UICONTROL Quantity]** von `1` ein.

   - Legen Sie **[!UICONTROL Price]** den Preistyp und den Betrag fest:

     - `Fixed` - Geben Sie den reduzierten Produktpreis ein.

     - `Discount` - Geben Sie den ermäßigten Preis als Prozentsatz des Produktpreises ein.

     ![Preise für Kundengruppen](./assets/product-price-group-discount.png){width="600" zoomable="yes"}

1. Um einen weiteren Gruppenpreis hinzuzufügen, klicken Sie auf **[!UICONTROL Add]** und wiederholen Sie den vorherigen Schritt.

1. Klicken Sie abschließend auf **[!UICONTROL Done]** und dann auf **[!UICONTROL Save]**.

>[!NOTE]
>
>Der **_Endpreis_** der Ware wird als **_Mindestpreis_** berechnet, und zwar nach folgender Formel: <br/>`Final Price=Min(Regular(Base) Price, Group(Tier) Price, Special Price, Catalog Price Rule) + Sum(Min Price per each required custom option)`

>[!NOTE]
>
>**_Festpreis_** Anpassbare Produktoptionen werden _nicht_ durch Gruppenpreis-, Stufenpreis-, Sonderpreis- oder Katalogpreisregeln beeinflusst.
