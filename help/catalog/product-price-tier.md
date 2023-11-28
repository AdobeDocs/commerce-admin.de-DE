---
title: Kategoriekosten
description: Erfahren Sie, wie Sie mit den Stufenpreisen über eine Produktliste oder Produktseite einen Mengenrabatt anbieten können.
exl-id: b5810899-31a6-4288-9acc-09f7f4dfbd43
feature: Catalog Management, Products
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '459'
ht-degree: 0%

---

# Kategoriekosten

Mit den Stufenpreisen können Sie einen Mengenrabatt von einer Produktliste oder Produktseite im Storefront anbieten. Der Rabatt kann auf eine bestimmte Store-Ansicht, eine Kundengruppe oder einen freigegebenen Katalog angewendet werden.

Wenn Sie viele Produkte aktualisieren müssen, ist es am effizientesten, die Änderungen am Tier-Preis zu importieren, anstatt sie einzeln einzugeben. Weitere Informationen finden Sie unter [Einfuhrstufungspreise](../systems/data-import-price-tier.md).

![Tier-Preis auf einer Storefront-Produktseite](./assets/product-price-tier-storefront.png){width="700" zoomable="yes"}

Auf der Produktseite wird der Mengenrabatt berechnet und eine Meldung wie die folgende angezeigt:

`Buy 6 for $5.95 each and save 15%`

Die Preise in der Storefront haben Vorrang von der höchsten bis zur niedrigsten Menge. Wenn Sie einen Partnerpreis für die Menge haben `5` und eines für `10`und ein Kunde fünf, sechs, sieben, acht oder neun Artikel zum Warenkorb hinzufügt, erhält der Kunde den ermäßigten Preis für die Menge `5` Ebene. Wenn der Kunde den zehnten Artikel hinzufügt, der für die Menge angegebene ermäßigte Preis `10` Ebene ersetzt die Ebene für eine Menge von `5`und des ermäßigten Preises für `10` gilt.

## Hinzufügen einer Preisstufe für ein Produkt

1. Öffnen Sie das Produkt im Bearbeitungsmodus.

1. Unter dem _[!UICONTROL Price]_Feld, klicken Sie auf **[!UICONTROL Advanced Pricing]**.

1. Im _[!UICONTROL Tier Price]_Abschnitt, klicken Sie auf **[!UICONTROL Add]**.

   Wenn Sie eine Stufe mit mehreren Preisen erstellen, klicken Sie auf **[!UICONTROL Add]** für jede zusätzliche Ebene, sodass Sie alle Ebenen gleichzeitig bearbeiten können. Jede Ebene in der Gruppe hat dieselbe Website- und Kundengruppe oder gemeinsame Katalogzuweisung, aber eine andere Menge und einen anderen Preis.

## Konfigurieren der Preisstufe

1. Wenn Ihr Store mehrere Websites hat, wählen Sie die **[!UICONTROL Website]** für die die Tier-Preise gelten.

1. Falls nötig, begrenzen Sie die Verfügbarkeit der Preisklasse durch Auswahl der **[!UICONTROL Customer Group]** oder **[!UICONTROL Shared Catalog]** (![B2B für Adobe Commerce](../assets/b2b.svg) Verfügbar mit [B2B für Adobe Commerce](./b2b/../introduction.md) nur).

1. Für **[!UICONTROL Qty]**, geben Sie die Menge ein, die bestellt werden muss, um den Rabatt zu erhalten.

   - **Methode 1:** Geben Sie den Preis als festen Betrag ein.

     Satz **[!UICONTROL Price]** nach `Fixed` und geben Sie den angepassten Preis für eine Einheit auf dieser Ebene an.

     ![Statuspreis als fester Betrag](./assets/product-price-tier-fixed.png){width="600" zoomable="yes"}

   - **Methode 2:** Preis in Prozent eingeben

     Satz **[!UICONTROL Price]** nach `Discount` und geben Sie den ermäßigten Preis als Prozentsatz des Basispreises des Produkts an.

     Geben Sie beispielsweise für einen 15-Prozent-Rabatt die Zahl ein. `15`. (Der Preis wird mit zwei Dezimalstellen gespeichert, z. B. `15.00`.

     >[!NOTE]
     >
     >Um den diskontierten Preis zu erhalten, wird der definierte Prozentsatz anhand des in der Variablen _[!UICONTROL Price]_ nicht das _[!UICONTROL Special Price]_ -Feld.

     ![Tier-Preis in Prozent](./assets/product-price-tier-discount.png){width="600" zoomable="yes"}

## Preiskonfiguration abschließen

1. Wiederholen Sie die vorherigen Schritte, um einen weiteren Satz von Stufenpreisen für eine andere Website oder Kundengruppe hinzuzufügen.

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Done]** und dann **[!UICONTROL Save]**.

>[!NOTE]
>
>Die **_final_** Der Produktpreis wird als **_Minimum_** relevanter Preis nach folgender Formel: <br/>`Final Price=Min(Regular(Base) Price, Group(Tier) Price, Special Price, Catalog Price Rule) + Sum(Min Price per each required custom option)`

>[!NOTE]
>
>**_Festpreis_** Anpassbare Produktoptionen sind _not_ beeinflusst von den Regeln für Gruppenpreis, Tier-Preis, Sonderpreis oder Katalogpreis.
