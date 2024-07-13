---
title: Was ist die Storefront?
description: Erfahren Sie mehr über die Seiten und funktionalen Elemente, die Ihr Store bereitstellen kann, um das Einkaufserlebnis für Ihre Kunden zu unterstützen.
exl-id: 1c64888f-2bc0-4e2e-b7da-0e7182ea67e0
feature: Storefront
source-git-commit: 3b359ed43e81a2771a372c8e3c7557853b3eecad
workflow-type: tm+mt
source-wordcount: '816'
ht-degree: 0%

---

# Was ist die Storefront?

Innerhalb Ihrer Adobe Commerce- oder Magento Open Source-Implementierung ist die Storefront der externe, öffentlich zugängliche Bereich Ihres Stores. Es stellt die Inhalte und funktionalen Komponenten bereit, die Ihre Kunden zum Einkaufen und Einkaufen verwenden.

Der Pfad, den Kunden zu einem Kauf nehmen, wird manchmal als _Pfad zum Kauf_ bezeichnet und Ihre Storefront enthält die Komponenten, damit Kunden diesen Pfad ausführen können. Die folgenden Abschnitte bieten einen Überblick über die grundlegenden Seitentypen, die einen strategischen Wert bieten - die Orte, die Kunden normalerweise besuchen, während sie in Ihrem Geschäft einkaufen. Berücksichtigen Sie bei der Überprüfung verschiedene Store-Funktionen, die in jeder Phase der Journey verwendet werden können.

## Startseite

Wusstest du, dass die meisten Leute nur ein paar Sekunden auf einer Seite verbringen, bevor sie sich entscheiden zu bleiben oder woanders zu gehen? Es ist nicht mehr lange, einen Eindruck zu machen. Studien zeigen, dass Menschen auch Fotos lieben, besonders von anderen Menschen. Welches Design Sie auch wählen, alles auf Ihrer Homepage sollte Besucher zum nächsten Schritt im Verkaufsprozess führen. Die Idee ist, ihre Aufmerksamkeit in einem zusammenhängenden Fluss von einem Zielpunkt zum nächsten zu lenken.

![Beispiel einer Storefront-Startseite ](./assets/storefront-homepage-full.png){width="700"}

## Katalogseite

Katalogseitenauflistungen haben in der Regel kleine Produktbilder und kurze Beschreibungen und können als Liste oder Raster formatiert werden. Sie können Bausteine, Videos und schlüsselwortreiche Beschreibungen hinzufügen und auch spezielle Entwürfe für eine Promotion oder Saison erstellen. Sie können eine spezielle Kategorie erstellen, um einen Lebensstil oder eine Marke zu kennzeichnen, bei dem es sich um eine kuratierte Sammlung von Produkten aus verschiedenen Kategorien handelt.

Die ursprüngliche Produktbeschreibung gibt den Käufern in der Regel genügend Informationen, um sie genauer anzusehen. Personen, die wissen, was sie wollen, können das Produkt zu ihrem Warenkorb hinzufügen und gehen. Kunden, die bei ihrem Konto einkaufen, genießen ein personalisiertes Einkaufserlebnis.

![Sammlungsseite auf der Storefront](./assets/storefront-collection-page.png){width="700"}

## Suchergebnisse

Wussten Sie, dass Personen, die die Suche verwenden, mit fast doppelt so hoher Wahrscheinlichkeit einen Kauf tätigen wie Personen, die sich allein auf die Navigation verlassen? Sie können diese Käufer als _vorqualifiziert_ betrachten.

### [!DNL Live Search]

Mit [[!DNL Live Search]](https://experienceleague.adobe.com/docs/commerce-merchant-services/live-search/overview.html) für Adobe Commerce bietet Ihr Store ein schnelles, superrelevantes und intuitives Sucherlebnis und steht Adobe Commerce ohne zusätzliche Kosten zur Verfügung.

![Beispiel für Live-Suche - Suche nach Eingabe von ](./assets/storefront-search-as-you-type.png){width="700"}

### Standardkatalogsuche

Bei der Standardkatalogsuche [ enthält Ihr Store ein Suchfeld in der oberen rechten Ecke und einen Link zur erweiterten Suche in der Fußzeile. ](../catalog/search.md) Alle Suchbegriffe, die von Käufern eingesendet werden, werden gespeichert, sodass Sie genau sehen können, wonach sie suchen. Sie können Vorschläge unterbreiten und Synonyme und gängige Rechtschreibfehler eingeben. Zeigen Sie dann eine bestimmte Seite an, wenn ein Suchbegriff eingegeben wird.

![Beispiel für standardmäßige Katalogsuchergebnisse](./assets/storefront-search-results-page-full.png){width="700"}

## Produktseite

Die Produktseite hat viel zu tun! Das erste, was Sie auf der Produktseite sehen, ist das Hauptbild mit einer hochauflösenden Zoom- und Miniaturgalerie. Neben dem Preis und der Verfügbarkeit gibt es einen Tab-Bereich mit weiteren Informationen und einer Liste verwandter Produkte.

![Beispiel für eine Storefront-Produktseite](./assets/storefront-product-page-full-m.png){width="700"}

## Warenkorb

Der Warenkorb ist der Ort, an dem die Gesamtbestellungen ermittelt werden können, zusammen mit Rabattgutscheinen und geschätzten Versand- und Steuervorgängen sowie einem idealen Ort, um Ihre Vertrauensabzeichen und Siegel anzuzeigen. Es ist auch eine ideale Gelegenheit, einen letzten Artikel anzubieten. Als Crosssell können Sie bestimmte Artikel auswählen, die als Impulskauf angeboten werden sollen, sobald ein bestimmter Artikel im Warenkorb erscheint.

![Beispiel für eine Storefront-Einkaufswagenseite ](./assets/storefront-cart-full.png){width="700"}

## Checkout-Seite

Der Checkout-Prozess besteht aus zwei Schritten:

1. Versandinformationen

   Der erste Schritt des Checkout-Prozesses besteht darin, dass der Kunde die Versandadressen-Informationen ausfüllt und die Versandmethode auswählt. Wenn der Kunde über ein Konto verfügt, wird die Lieferadresse automatisch angegeben, kann aber bei Bedarf geändert werden.
Wenn ein Gastkunde eine E-Mail-Adresse eingibt, die als zuvor registriert wurde, wird die Anmeldeaufforderung angezeigt, wenn das Feld [!UICONTROL Enable Guest Checkout Login] in der Speicherkonfiguration auf `Yes` eingestellt ist (siehe [[!UICONTROL Checkout Options]](../configuration-reference/sales/checkout.md#checkout-options) im _Konfigurationshandbuch_). Diese Einstellung kann jedoch Kundeninformationen für nicht authentifizierte Benutzer verfügbar machen.

   ![Beispiel für eine Storefront-Checkout-Seite](./assets/storefront-checkout-shipping-full.png){width="700"}

1. Überprüfen und Zahlungsinformationen

   Der zweite Schritt des Checkout-Prozesses besteht darin, dass der Kunde die Zahlungsmethode auswählt und optional einen Rabattcode anwendet.

   >[!NOTE]
   >
   >Obwohl [!DNL Commerce] die Konfiguration mehrerer Couponcodes ermöglicht, darf ein Kunde nur einen Couponcode auf den Warenkorb anwenden. (Weitere Informationen finden Sie unter [Couponcodes](../merchandising-promotions/price-rules-cart-coupon.md#coupon-codes) .)

   ![Beispiel für eine Storefront-Checkout-Seite](./assets/storefront-checkout-payment-full.png){width="700"}

Die Fortschrittsleiste am oberen Seitenrand folgt jedem Schritt des Checkout-Prozesses, und die _Bestellzusammenfassung_ zeigt die Informationen an, die bis zu diesem Zeitpunkt eingegeben wurden.

>[!NOTE]
>
>Die Ausnahme für einen zweistufigen Checkout gilt für virtuelle und/oder herunterladbare Produkte. Wenn sich nur diese Arten von Produkten im Warenkorb befinden, wird der Checkout automatisch in eine einstufige Prozedur umgewandelt, da keine Versandinformationen erforderlich sind.
