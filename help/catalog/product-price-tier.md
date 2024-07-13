---
title: Kategoriekosten
description: Erfahren Sie, wie Sie mit den Stufenpreisen über eine Produktliste oder Produktseite einen Mengenrabatt anbieten können.
exl-id: b5810899-31a6-4288-9acc-09f7f4dfbd43
feature: Catalog Management, Products
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '458'
ht-degree: 0%

---

# Kategoriekosten

Mit den Stufenpreisen können Sie einen Mengenrabatt von einer Produktliste oder Produktseite im Storefront anbieten. Der Rabatt kann auf eine bestimmte Store-Ansicht, eine Kundengruppe oder einen freigegebenen Katalog angewendet werden.

Wenn Sie viele Produkte aktualisieren müssen, ist es am effizientesten, die Änderungen am Tier-Preis zu importieren, anstatt sie einzeln einzugeben. Weitere Informationen finden Sie unter [Preise der Importstufe](../systems/data-import-price-tier.md).

![Tier-Preis auf einer Storefront-Produktseite](./assets/product-price-tier-storefront.png){width="700" zoomable="yes"}

Auf der Produktseite wird der Mengenrabatt berechnet und eine Meldung wie die folgende angezeigt:

`Buy 6 for $5.95 each and save 15%`

Die Preise in der Storefront haben Vorrang von der höchsten bis zur niedrigsten Menge. Wenn Sie einen Stufenpreis für die Menge `5` und einen für `10` haben und ein Kunde fünf, sechs, sieben, acht oder neun Artikel zum Warenkorb hinzufügt, erhält der Kunde den abgezinsten Preis für die Menge `5`. Wenn der Kunde das zehnte Element hinzufügt, ersetzt der für die Menge `10` angegebene diskontierte Preis die Ebene für eine Menge von `5`, und der abgezinste Preis für `10` gilt.

## Hinzufügen einer Preisstufe für ein Produkt

1. Öffnen Sie das Produkt im Bearbeitungsmodus.

1. Klicken Sie unter dem Feld _[!UICONTROL Price]_auf **[!UICONTROL Advanced Pricing]**.

1. Klicken Sie im Abschnitt _[!UICONTROL Tier Price]_auf **[!UICONTROL Add]**.

   Wenn Sie eine Ebene mit mehreren Preisen erstellen, klicken Sie für jede zusätzliche Ebene auf **[!UICONTROL Add]** , damit Sie alle Ebenen gleichzeitig arbeiten können. Jede Ebene in der Gruppe hat dieselbe Website- und Kundengruppe oder gemeinsame Katalogzuweisung, aber eine andere Menge und einen anderen Preis.

## Konfigurieren der Preisstufe

1. Wenn Ihr Store über mehrere Websites verfügt, wählen Sie die **[!UICONTROL Website]** aus, für die der Stufenpreis gilt.

1. Beschränken Sie bei Bedarf die Verfügbarkeit der Preisebene, indem Sie die Option **[!UICONTROL Customer Group]** oder **[!UICONTROL Shared Catalog]** (![Adobe Commerce B2B](../assets/b2b.svg) Verfügbar nur mit [Adobe Commerce B2B](./b2b/../introduction.md)) auswählen.

1. Geben Sie für **[!UICONTROL Qty]** die Menge ein, die bestellt werden muss, um den Rabatt zu erhalten.

   - **Methode 1:** Geben Sie den Preis als festen Betrag ein

     Setzen Sie **[!UICONTROL Price]** auf `Fixed` und geben Sie den angepassten Preis für eine Einheit auf dieser Ebene ein.

     ![Statuspreis als fester Betrag](./assets/product-price-tier-fixed.png){width="600" zoomable="yes"}

   - **Methode 2:** Preis in Prozent eingeben

     Setzen Sie **[!UICONTROL Price]** auf `Discount` und geben Sie den ermäßigten Preis als Prozentsatz des Basispreises des Produkts ein.

     Geben Sie beispielsweise für einen 15-Prozent-Rabatt die Zahl `15` ein. (Der Preis wird mit zwei Dezimalstellen wie `15.00` gespeichert.)

     >[!NOTE]
     >
     >Um den ermäßigten Preis zu erhalten, wird der definierte Prozentsatz anhand des im Feld _[!UICONTROL Price]_definierten Werts und nicht anhand des Felds_[!UICONTROL Special Price]_ berechnet.

     ![Tier Price as a Percentage](./assets/product-price-tier-discount.png){width="600" zoomable="yes"}

## Preiskonfiguration abschließen

1. Wiederholen Sie die vorherigen Schritte, um einen weiteren Satz von Stufenpreisen für eine andere Website oder Kundengruppe hinzuzufügen.

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Done]** und dann auf **[!UICONTROL Save]**.

>[!NOTE]
>
>Der Produktpreis **_final_** wird als relevanter Preis für **_Minimum_** anhand der folgenden Formel berechnet: <br/>`Final Price=Min(Regular(Base) Price, Group(Tier) Price, Special Price, Catalog Price Rule) + Sum(Min Price per each required custom option)`

>[!NOTE]
>
>**_Der feste Preis_** Die anpassbaren Optionen für das Produkt sind _nicht_ von den Regeln für Gruppenpreis, Tier-Preis, Sonderpreis oder Katalogpreis betroffen.
