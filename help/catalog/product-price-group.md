---
title: Gruppenpreise
description: Erfahren Sie, wie Sie mithilfe von Gruppenpreisen die Preise für vergünstigte Artikel basierend auf Kundengruppen in Ihrem Geschäft festlegen können.
exl-id: bc5be23f-64eb-47c3-beda-01168abfbf96
feature: Catalog Management, Products, Customers
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '332'
ht-degree: 0%

---

# Gruppenpreise

Sie können die Produktkonfigurationseinstellungen in der Admin-Konsole verwenden, um Preise für ermäßigte Artikel auf der Grundlage von Kundengruppen in Ihrem Geschäft festzulegen. Dieses strategische Preismodell heißt _Gruppenpreise_.

Der ermäßigte Preis eines Produkts kann Mitgliedern einer bestimmten Kundengruppe angeboten werden, wenn der Käufer bei seinem Konto angemeldet ist. Der Kundengruppenpreis wird zusammen mit dem regulären Preis auf der Produktseite angezeigt, sodass ein Käufer die Preise einfach vergleichen und entsprechend handeln kann. Nachdem der Kunde das Produkt zum Warenkorb hinzugefügt hat, wird der reguläre Preis durch den auf seiner Kundengruppe basierenden Gruppenpreis ersetzt.

Die Preise für Kundengruppen sind Bestandteil der [gestaffelten Preise](product-price-tier.md) und werden auf ähnliche Weise festgelegt. Der einzige Unterschied besteht darin, dass die Preise der Kundengruppen eine Menge von 1 aufweisen.

![Kundengruppenrabatt](./assets/storefront-price-group.png){width="600" zoomable="yes"}

## Vorteile der Verwendung von Gruppenpreisen

- Geeignet für Großkäufer

- Anreize für Kunden, ihre Kundengruppe zu aktualisieren, um von Rabatten zu profitieren

- Zielgerichtete Marketing-Kampagnen

- Vertrauen und Glaubwürdigkeit schaffen durch Belohnung treuer Kunden

## Einrichten eines Gruppenpreises

1. Öffnen Sie das Produkt im Bearbeitungsmodus.

1. Klicken Sie unter dem Feld _[!UICONTROL Price]_auf **[!UICONTROL Advanced Pricing]**.

1. Klicken Sie im Abschnitt _[!UICONTROL Customer Group Price]_auf **[!UICONTROL Add]**.

   Wenn Ihr Store [Adobe Commerce B2B](../b2b/introduction.md) enthält und [freigegebene Kataloge](../b2b/catalog-shared.md) aktiviert ist, wird dieser Abschnitt mit _[!UICONTROL Catalog and Tier Price]_beschriftet.

   ![Erweiterte Preise](./assets/product-price-group.png){width="600" zoomable="yes"}

1. Konfigurieren Sie den Gruppenpreis:

   - Wählen Sie für eine Installation mit mehreren Sites den Wert &quot;**[!UICONTROL Website]**&quot;, für den der Gruppenpreis gilt.

   - Wählen Sie die **[!UICONTROL Customer Group]** aus, die den Rabatt erhalten soll.

   - Geben Sie den Wert **[!UICONTROL Quantity]** von `1` ein.

   - Legen Sie für **[!UICONTROL Price]** den Preistyp und den Betrag fest:

      - `Fixed` - Geben Sie den ermäßigten Produktpreis ein.

      - `Discount` - Geben Sie den ermäßigten Preis als Prozentsatz des Produktpreises ein.

     ![Preise für Kundengruppen](./assets/product-price-group-discount.png){width="600" zoomable="yes"}

1. Um einen weiteren Gruppenpreis hinzuzufügen, klicken Sie auf **[!UICONTROL Add]** und wiederholen Sie den vorherigen Schritt.

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Done]** und dann auf **[!UICONTROL Save]**.

>[!NOTE]
>
>Der Produktpreis **_final_** wird als relevanter Preis für **_Minimum_** anhand der folgenden Formel berechnet: <br/>`Final Price=Min(Regular(Base) Price, Group(Tier) Price, Special Price, Catalog Price Rule) + Sum(Min Price per each required custom option)`

>[!NOTE]
>
>**_Der feste Preis_** Die anpassbaren Optionen für das Produkt sind _nicht_ von den Regeln für Gruppenpreis, Tier-Preis, Sonderpreis oder Katalogpreis betroffen.
