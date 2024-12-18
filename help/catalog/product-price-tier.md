---
title: Preisstufe
description: Erfahren Sie, wie Sie mit der Preisstufe einen Mengenrabatt von einer Produktliste oder Produktseite aus anbieten können.
exl-id: b5810899-31a6-4288-9acc-09f7f4dfbd43
feature: Catalog Management, Products
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '458'
ht-degree: 0%

---

# Preisstufe

Mit Preisstufen können Sie einen Mengenrabatt von einer Produktliste oder Produktseite in der Storefront anbieten. Der Rabatt kann auf eine bestimmte Shop-Ansicht, Kundengruppe oder einen freigegebenen Katalog angewendet werden.

Wenn Sie viele Produkte aktualisieren müssen, ist es am effizientesten, die Preisänderungen der Stufe zu importieren, anstatt sie einzeln einzugeben. Weitere Informationen finden Sie unter [Preise der Importstufe](../systems/data-import-price-tier.md).

![Stufenpreis auf einer Storefront-Produktseite](./assets/product-price-tier-storefront.png){width="700" zoomable="yes"}

Die Produktseite berechnet den Mengenrabatt und zeigt eine Meldung an, z. B.:

`Buy 6 for $5.95 each and save 15%`

Die Preise in der Storefront haben Vorrang von der höchsten zur niedrigsten Menge. Wenn Sie einen Stufenpreis für die Menge `5` und einen für `10` haben und ein Kunde fünf, sechs, sieben, acht oder neun Artikel in den Warenkorb legt, erhält der Kunde den ermäßigten Preis für die Menge `5` Stufe. Wenn der Kunde den zehnten Artikel hinzufügt, ersetzt der für die Menge `10` Stufe angegebene abgezinste Preis die Stufe für eine Menge von `5`, und der abgezinste Preis für `10` gilt.

## Preisstufe für ein Produkt hinzufügen

1. Öffnen Sie das Produkt im Bearbeitungsmodus.

1. Klicken Sie unter dem Feld _[!UICONTROL Price]_auf **[!UICONTROL Advanced Pricing]**.

1. Klicken Sie im Abschnitt _[!UICONTROL Tier Price]_auf **[!UICONTROL Add]**.

   Wenn Sie eine Preisstufe mit mehreren Preisen erstellen, klicken Sie auf **[!UICONTROL Add]** für jede zusätzliche Ebene, damit Sie alle Ebenen gleichzeitig bearbeiten können. Jede Ebene in der Gruppe verfügt über dieselbe Website und Kundengruppe oder gemeinsame Katalogzuweisung, aber eine andere Menge und einen anderen Preis.

## Konfigurieren der Preisstufe

1. Wenn Ihr Store über mehrere Websites verfügt, wählen Sie die **[!UICONTROL Website]** aus, für die die Preisstufe gilt.

1. Schränken Sie bei Bedarf die Verfügbarkeit der Preisstufe ein, indem Sie die **[!UICONTROL Customer Group]** oder den **[!UICONTROL Shared Catalog]** auswählen (![Adobe Commerce B2B](../assets/b2b.svg) Nur verfügbar mit [Adobe Commerce B2B](./b2b/../introduction.md)).

1. Geben Sie **[!UICONTROL Qty]** die Menge ein, die bestellt werden muss, um den Rabatt zu erhalten.

   - **Methode 1:** Geben Sie den Preis als festen Betrag ein

     Legen Sie **[!UICONTROL Price]** auf `Fixed` fest und geben Sie den angepassten Preis für eine Einheit dieser Stufe ein.

     ![Tierpreis als fester Betrag](./assets/product-price-tier-fixed.png){width="600" zoomable="yes"}

   - **Methode 2:** Geben Sie den Preis in Prozent ein.

     Setzen Sie **[!UICONTROL Price]** auf `Discount` und geben Sie den Rabattpreis als Prozentsatz des Grundpreises des Produkts ein.

     Geben Sie beispielsweise für einen Rabatt von 15 % die Zahl `15` ein. (Der Preis wird mit zwei Dezimalstellen gespeichert, z. B. `15.00`.)

     >[!NOTE]
     >
     >Um den reduzierten Preis abzurufen, wird der definierte Prozentsatz anhand des im Feld _[!UICONTROL Price]_definierten Werts berechnet und nicht anhand des Felds_[!UICONTROL Special Price]_.

     ![Stufenpreis in Prozent](./assets/product-price-tier-discount.png){width="600" zoomable="yes"}

## Abschließen der Preiskonfiguration

1. Um einen weiteren Satz von Preisstufen für eine andere Website oder Kundengruppe hinzuzufügen, wiederholen Sie die vorherigen Schritte.

1. Klicken Sie abschließend auf **[!UICONTROL Done]** und dann auf **[!UICONTROL Save]**.

>[!NOTE]
>
>Der **_Endpreis_** der Ware wird als **_Mindestpreis_** berechnet, und zwar nach folgender Formel: <br/>`Final Price=Min(Regular(Base) Price, Group(Tier) Price, Special Price, Catalog Price Rule) + Sum(Min Price per each required custom option)`

>[!NOTE]
>
>**_Festpreis_** Anpassbare Produktoptionen werden _nicht_ durch Gruppenpreis-, Stufenpreis-, Sonderpreis- oder Katalogpreisregeln beeinflusst.
