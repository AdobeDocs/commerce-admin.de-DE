---
title: Warenkorbkonfiguration
description: Erfahren Sie mehr über die Warenkorbfunktionen, die Sie konfigurieren können, um das Kauferlebnis in Ihrem Geschäft zu unterstützen.
exl-id: b98ec7ce-9354-4f03-b67e-dd1587f0c866
feature: Shopping Cart, Configuration
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '2449'
ht-degree: 0%

---

# Warenkorbkonfiguration

Die Warenkorbkonfiguration bestimmt, wie der Warenkorb für Ihre Store-Kunden funktioniert, einschließlich der Umleitung des Kunden zur Warenkorbseite und der Verwendung von Bildern für Produktminiaturansichten. Sie können auch verlangen, dass eine Bestellung einen Mindestbetrag erreicht, bevor der Checkout-Prozess beginnt, die Anzahl der Tage, für die die angegebenen Preise gültig bleiben, angeben und die Reihenfolge der Artikel im Abschnitt _Bestellsummen_ angeben.

[**Mini-Warenkorb**](#mini-cart) - Konfigurieren Sie diese Option, um festzustellen, ob der Warenkorb-Link/das Symbol die Anzahl der verschiedenen Produkte (oder SKUs) im Warenkorb oder die Gesamtmenge aller Artikel anzeigt.

[**Mini-Warenkorb-Link**](#configure-the-cart-link) - Konfigurieren Sie diese Option, um festzustellen, ob der Mini-Warenkorb angezeigt wird, wenn ein Kunde auf die Anzahl der Artikel im Warenkorbsymbol oben auf einer Store-Seite klickt.

[**Zu Warenkorb umleiten**](#redirect-to-cart) - Konfigurieren Sie diese Option, um festzustellen, ob die Warenkorbseite immer dann angezeigt wird, wenn ein Artikel zum Warenkorb hinzugefügt wird, oder nur, wenn ein Kunde beschließt, zur Seite zu gehen.

[**Lebensdauer eines Preises angeben**](#quote-lifetime) - Konfigurieren Sie diese Option, um festzulegen, wie lange ein Preis gültig ist.

[**Mindestbestellbetrag**](#minimum-order-amount) - Konfigurieren Sie diese Optionen, um einen Mindestbetrag festzulegen, nachdem Rabatte angewendet wurden, die Bestelluntersummen erfüllt werden müssen und die Meldungen im Warenkorb angezeigt werden.

[**Mindestbestellmenge**](#minimum-order-quantity) - Konfigurieren Sie diese Optionen, um eine Mindestanzahl von Elementen anzugeben, die für die Bestellung erforderlich sind.

[**Warenkorb-Miniaturansichten**](#cart-thumbnails) - Konfigurieren Sie die Optionen für Warenkorbminiaturansichten, um die im Warenkorb angezeigten Miniaturansichten für gruppierte oder konfigurierbare Produkte zu bestimmen.

[**Geschenkoptionen**](#gift-options) - Konfigurieren Sie Geschenkoptionen, um zu bestimmen, ob Kunden Geschenkgutschriften oder Grußkarten hinzufügen können und ob Geschenkverpackungsoptionen verfügbar sind.

>[!NOTE]
>
>Informationen zum Konfigurieren des Checkout-Prozesses finden Sie unter [Checkout-Optionen](checkout-process.md).

## Mini-Warenkorb

Der _Mini-Warenkorb_ zeigt eine Zusammenfassung der Artikel im Warenkorb an. Sie ist standardmäßig aktiviert und wird angezeigt, wenn Sie oben auf der Seite auf den Link Warenkorb klicken.
Der Link kann so konfiguriert werden, dass die Anzahl der verschiedenen Produkte (oder SKUs) im Warenkorb oder die Gesamtmenge aller Artikel angezeigt wird.

![Der Käufer zeigt die Warenkorbseitenleiste von einer Produktseite an](./assets/storefront-mini-cart-watch.png){width="700" zoomable="yes"}

>[!NOTE]
>
>Bei einem _registrierten_ -Kunden kann es vorkommen, dass der Mini-Warenkorb nicht automatisch über mehrere Geräte und Browser hinweg synchronisiert wird. Um den Mini-Warenkorb in solchen Fällen zu synchronisieren, kann der Kunde einfach die Seite [Warenkorb](cart.md) auf diesem Gerät oder Browser öffnen.

### Konfigurieren des Mini-Warenkorbs

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich den Wert **[!UICONTROL Sales]** und wählen Sie **[!UICONTROL Checkout]** aus.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) im Abschnitt _[!UICONTROL Mini Cart]_.

   ![Konfigurieren des Mini-Warenkorbs](../configuration-reference/sales/assets/checkout-mini-cart.png){width="600" zoomable="yes"}

1. Wenn die Einstellung für eine bestimmte Store-Ansicht gilt, wählen Sie [die Store-Ansicht](../configuration-reference/scope-change.md#set-the-scope), in der die Konfiguration gilt.

   Klicken Sie nach Aufforderung auf **[!UICONTROL OK]** , um fortzufahren.

1. Setzen Sie **[!UICONTROL Display Mini Cart]** auf einen der folgenden Werte:

   - `Yes` - Zeigt den Mini-Warenkorb auf Store-Seiten an. Das Erscheinungsbild der Seitenleiste hängt vom Design ab.
   - `No` - Deaktiviert die Anzeige des Mini-Warenkorbs auf Store-Seiten.

1. Wenn die Anzeige aktiviert ist, aktualisieren Sie die anderen Optionen, um die Anzeige zu konfigurieren:

   - Geben Sie für &quot;**[!UICONTROL Number of Items to Display Scrollbar]**&quot;die Anzahl der Elemente ein, die in der Seitenleiste angezeigt werden können, bevor die Bildlaufleiste ausgelöst wird.
   - Geben Sie für &quot;**[!UICONTROL Maximum Display Recently Added Item(s)]**&quot;die maximale Anzahl der kürzlich hinzugefügten Artikel ein, die im Mini-Warenkorb angezeigt werden sollen.

1. Klicken Sie auf **[!UICONTROL Save Config]**.

### Warenkorb-Link konfigurieren

1. Auf der Seitenleiste _Admin_ wurde **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**angezeigt.

1. Erweitern Sie im linken Bereich den Wert **[!UICONTROL Sales]** und wählen Sie **[!UICONTROL Checkout]** aus.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) im Abschnitt **[!UICONTROL My Cart Link]** .

1. Legen Sie **[!UICONTROL Display Cart Summary]** auf eine der folgenden Einstellungen fest:

   - `Display item quantities` - Diese Einstellung zeigt die Gesamtanzahl der Produkte im Warenkorb an und fügt die Mengen für jedes Produkt hinzu.
   - `Display number of items in cart` - Diese Einstellung zeigt die Anzahl der Artikel im Warenkorb an, unabhängig von der Menge.

   ![Konfigurationsoptionen für meinen Warenkorblink](../configuration-reference/sales/assets/checkout-my-cart-link.png){width="600" zoomable="yes"}

1. Klicken Sie auf **[!UICONTROL Save Config]**.

## Zum Warenkorb umleiten

Die Warenkorbseite kann so konfiguriert werden, dass sie immer dann angezeigt wird, wenn ein Artikel zum Warenkorb hinzugefügt wird, oder nur, wenn Kunden sich dafür entscheiden, zur Seite zu gehen. Die grundlegenden Informationen zu den aktuell im Warenkorb befindlichen Artikeln sind immer im [Mini-Warenkorb](#mini-cart) verfügbar. Die Entscheidung besteht darin, die Vorteile eines weiteren Einkaufs zwischen den Kunden und dem Vorteil einer Ermutigung der Kunden zum Checkout auszugleichen. Es könnte eine einfache Frage persönlicher Präferenz sein. Wenn Sie sie jedoch mit Zahlen sichern möchten, können Sie einen A/B-Test durchführen, um zu sehen, welcher Ansatz zu einer höheren Konversionsrate führt.

**_So konfigurieren Sie, wann der Warenkorb angezeigt wird:_**

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich den Wert **[!UICONTROL Sales]** und wählen Sie **[!UICONTROL Checkout]** aus.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) im Abschnitt **[!UICONTROL Shopping Cart]** .

   ![Die Konfigurationseinstellungen des Warenkorbs wurden auf der Seite eingeblendet](../configuration-reference/sales/assets/checkout-shopping-cart.png){width="600" zoomable="yes"}

1. Wenn die Einstellung für eine bestimmte Store-Ansicht gilt, wählen Sie [die Store-Ansicht](../configuration-reference/scope-change.md#set-the-scope), in der die Konfiguration gilt.

   Klicken Sie nach Aufforderung auf **[!UICONTROL OK]** , um fortzufahren.

1. Setzen Sie **[!UICONTROL After Adding a Product Redirect to Shopping Cart]** auf einen der folgenden Werte:

   - `Yes` - Zeigt die Warenkorbseite unmittelbar nach dem Hinzufügen eines Produkts zum Warenkorb an.
   - `No` - Deaktiviert die Umleitung zum Warenkorb nach einer Produktaktualisierung zum Warenkorb.

1. Klicken Sie auf **[!UICONTROL Save Config]**.

## Anführungslebensdauer

Mit der Installation und Aktivierung von Adobe Commerce B2B können Sie die Funktion _Anführungszeichen_ unterstützen. Diese Funktion ermöglicht es autorisierten Käufern, den Preisverhandelungsprozess einzuleiten, indem sie eine Anfrage vom Warenkorb einreichen. Das Raster _Anführungszeichen_ listet jedes erhaltene Angebot auf und pflegt einen Verlauf der Kommunikation zwischen Käufer und Verkäufer. Weitere Informationen zu den B2B-Funktionen finden Sie unter [Verhandlungsanführungszeichen](../b2b/quotes.md) im _Adobe Commerce B2B-Benutzerhandbuch_.

Sie können feststellen, wie lange ein Preis gültig ist, indem Sie die Lebensdauer des Warenkorbangebots in der Konfiguration festlegen. Wenn beispielsweise ein Käufer einen Warenkorb nach mehreren Tagen unbeaufsichtigt lässt, ist der Anführungspreis für einige Artikel möglicherweise nicht mehr derselbe. Standardmäßig ist die Anführungszeitdauer auf 30 Tage eingestellt.

**_So konfigurieren Sie die Lebensdauer des Zitats:_**

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich den Wert **[!UICONTROL Sales]** und wählen Sie **[!UICONTROL Checkout]** aus.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) im Abschnitt **[!UICONTROL Shopping Cart]** .

   ![Die Konfigurationseinstellungen des Warenkorbs wurden auf der Seite eingeblendet](../configuration-reference/sales/assets/checkout-shopping-cart.png){width="600" zoomable="yes"}

1. Wenn die Einstellung für eine bestimmte Store-Ansicht gilt, wählen Sie [die Store-Ansicht](../configuration-reference/scope-change.md#set-the-scope), in der die Konfiguration gilt.

   Klicken Sie nach Aufforderung auf **[!UICONTROL OK]** , um fortzufahren.

1. Geben Sie für &quot;**[!UICONTROL Quote Lifetime (days)]**&quot;die Anzahl der Tage an, für die ein notierter Preis gültig bleibt.

1. Klicken Sie auf **[!UICONTROL Save Config]**.

## Mindestauftragsbetrag

Mit der Konfiguration können Sie einen Mindestbetrag festlegen, um nach Anwendung von Rabatten die Bestellteilsummen zu erfüllen. An mehrere Adressen versandte Bestellungen können zur Erfüllung des Mindestbestellbetrags pro Adresse erforderlich sein. Die Schaltfläche Auschecken wird erst verfügbar, nachdem der Mindestbestellbetrag erreicht wurde.

![Der Warenkorb zeigt eine Mindestbestellnachricht an](./assets/storefront-cart-minimum-order-amount.png){width="700" zoomable="yes"}

**_So konfigurieren Sie einen Mindestbestellbetrag:_**

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bedienfeld den Wert **[!UICONTROL Sales]** und wählen Sie unter &quot;**[!UICONTROL Sales]**&quot;.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) im Abschnitt **[!UICONTROL Minimum Order Amount]** .

   ![Die auf der Seite eingeblendeten Konfigurationsoptionen für Mindestbestellungen](../configuration-reference/sales/assets/sales-minimum-order-amount.png){width="600" zoomable="yes"}

1. Um einen Mindestbestellbetrag zu verlangen, setzen Sie **[!UICONTROL Enable]** auf `Yes`.

1. Wenn die Mindestreihenfolge aktiviert ist, legen Sie die folgenden Optionen zum Konfigurieren der Anforderung fest:

   - Geben Sie die **[!UICONTROL Minimum Amount]** ein, die für die Zwischensumme erforderlich ist, nachdem Rabatte angewendet wurden.

   - Setzen Sie **[!UICONTROL Include Discount Amount]** auf einen der folgenden Werte:

      - `Yes` - Erfordert, dass die Zwischensumme den Mindestbetrag mit allen enthaltenen Rabatten erfüllt. Wenn der Warenkorb ein Beispiel für einen Mindestbetrag von 50 USD enthält und ein Top-60-Wert von 60 USD mit einem angewendeten Rabatt von 25 % angewendet wird, beträgt die resultierende Zwischensumme 45 USD, und der Warenkorb würde nicht das Minimum erreichen.
      - `No` - Erfordert, dass die Zwischensumme den Mindestbetrag ohne Rabatte erfüllt.

   - Setzen Sie **[!UICONTROL Include Tax to Amount]** auf einen der folgenden Werte:

      - `Yes` - Erfordert, dass die Zwischensumme den Mindestbetrag einschließlich Steuern erfüllt.
      - `No` - Erfordert, dass die Zwischensumme den Mindestbetrag ohne Steuern erfüllt.

1. Passen Sie optional die Einstellungen für die Mindestbestellmenge an Nachricht an:

   - Geben Sie für **[!UICONTROL Description Message]** den Text ein, den Sie verwenden möchten, um die Nachricht anzupassen, die oben im Warenkorb erscheint, wenn die Zwischensumme nicht den Mindestwert erreicht.

   - Geben Sie für &quot;**[!UICONTROL Error to Show in Shopping Cart]**&quot;den Text ein, den Sie zum Anpassen der Warenkorbfehlermeldung verwenden möchten.

   Lassen Sie die Felder der Nachrichtenbeschreibung leer, um die Standardmeldungen zu verwenden.

1. Konfigurieren Sie bei Bedarf die Mindestbestellmenge für Bestellungen mit mehreren Adressen:

   - Um zu verlangen, dass jede Adresse in einer Bestellung mit mehreren Adressen den Mindestbestellbetrag erfüllt, setzen Sie **[!UICONTROL Validate Each Address Separately in Multi-address Checkout]** auf `Yes`.

   - Passen Sie optional die Einstellungen für die Mindestbestellmenge an Nachricht an:

      - **[!UICONTROL Multi-address Description Message]** - Geben Sie den Text ein, den Sie verwenden möchten, um die Nachricht anzupassen, die oben im Warenkorb für Bestellungen mit mehreren Adressen angezeigt wird, die nicht das Minimum erreichen.

      - **[!UICONTROL Multi-address Error to Show in Shopping Cart]** - Geben Sie den Text ein, den Sie verwenden möchten, um die Fehlermeldung zum Warenkorb für Bestellungen mit mehreren Adressen anzupassen, die nicht die Mindestanforderungen erfüllen, und geben Sie den Text in das Feld ein.

     Lassen Sie die Felder der Nachrichtenbeschreibung leer, um die Standardmeldungen zu verwenden.

1. Klicken Sie auf **[!UICONTROL Save Config]**.

## Mindestauftragsmenge

Sie können die für eine Bestellung zulässige Mindestmenge festlegen. Die Mindestmenge kann auch entsprechend der jeweiligen Kundengruppe konfiguriert werden.

1. Gehen Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich den Wert **[!UICONTROL Catalog]** und wählen Sie **[!UICONTROL Inventory]** aus.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) im Abschnitt **[!UICONTROL Product Stock Options]** .

   ![Optionen für Produktspeicher](../configuration-reference/catalog/assets/catalog-inventory-product-stock-options.png){width="600" zoomable="yes"}

1. Legen Sie für **[!UICONTROL Minimum Qty Allowed in Shopping Cart]** die Mindestmenge des Produkts für eine Bestellung fest.

   Deaktivieren Sie bei Bedarf das Kontrollkästchen **[!UICONTROL Use system value]** , um diese Einstellungen zu ändern.

   - Ändern Sie die Einstellung **[!UICONTROL Customer Group]** in eine bestimmte Gruppe und geben Sie die **[!UICONTROL Minimum Qty]** für diese Gruppe ein. Um eine weitere Gruppe und Mengenbegrenzung hinzuzufügen, klicken Sie auf **[!UICONTROL Add Minimum Qty]**.

   - Behalten Sie die Auswahl `ALL GROUPS` bei und geben Sie den Wert **[!UICONTROL Minimum Qty]** ein, um dieselbe Mindestmengenbegrenzung für alle Kunden festzulegen.

1. Klicken Sie auf **[!UICONTROL Save Config]**.

   ![Mindestanforderungen an die Menge im Warenkorb](./assets/minimum-qty-allowed-in-shopping-cart.png){width="700" zoomable="yes"}

## Warenkorb-Miniaturansichten

![Adobe Commerce](../assets/adobe-logo.svg) (nur Adobe Commerce)

Die im Warenkorb angezeigten Miniaturansichten geben Kunden einen schnellen Überblick über die Artikel, die sie kaufen werden. Bei Produkten mit mehreren Optionen stimmt das Bild jedoch möglicherweise nicht mit der Variante des Produkts überein, das sich im Warenkorb befindet. Wenn der Kunde einen Artikel in einer bestimmten Farbe kauft, sollte idealerweise die Miniaturansicht im Warenkorb übereinstimmen.

Das Miniaturbild für gruppierte und konfigurierbare Produkte kann so eingestellt werden, dass es das Bild aus dem &quot;übergeordneten&quot;Produkt oder aus der Produktvariante anzeigt.

![Der Warenkorb zeigt Miniaturansichten für jedes Produkt an](./assets/storefront-cart.png){width="700" zoomable="yes"}

**_So konfigurieren Sie Warenkorbminiaturansichten:_**

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich den Wert **[!UICONTROL Sales]** und wählen Sie **[!UICONTROL Checkout]** aus.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) im Abschnitt **[!UICONTROL Shopping Cart]** .

   ![Die Konfigurationseinstellungen des Warenkorbs wurden auf der Seite eingeblendet](../configuration-reference/sales/assets/checkout-shopping-cart.png){width="600" zoomable="yes"}

1. Legen Sie **[!UICONTROL Grouped Product Image]** fest, um die Miniaturansicht zu bestimmen, die im Warenkorb für [gruppierte Produkte](../catalog/product-create-grouped.md) verwendet wird:

   - `Product Thumbnail Itself` - Verwendet die der Produktvariante zugewiesene Miniaturansicht, die dem Warenkorb hinzugefügt wird.
   - `Parent Product Thumbnail` - Verwendet die dem übergeordneten Produkt zugewiesene Miniaturansicht.

1. Legen Sie **[!UICONTROL Configurable Product Image]** fest, um die Miniaturansicht zu bestimmen, die im Warenkorb für [konfigurierbare Produkte](../catalog/product-create-configurable.md) verwendet wird:

   - `Product Thumbnail Itself` - Verwendet die der Produktvariante zugewiesene Miniaturansicht, die dem Warenkorb hinzugefügt wird.
   - `Parent Product Thumbnail` - Verwendet die dem übergeordneten Produkt zugewiesene Miniaturansicht.

1. Klicken Sie auf **[!UICONTROL Save Config]**.

## Geschenkoptionen

Die Auswahl der verfügbaren Geschenkoptionen wird im Warenkorb angezeigt, bevor der Checkout-Prozess beginnt. Die Konfiguration der Geschenkoptionen bestimmt, ob Kunden Geschenkgutschriften oder Grußkarten hinzufügen können und ob Geschenkverpackungsoptionen verfügbar sind. Jeder Artikel in der Bestellung kann eine separate Nachricht und Geschenkverpackung haben. Bei Anwendung auf die gesamte Bestellung können Kunden auch einen Geschenkgutschein und eine Grußkarte hinzufügen.

![Beispiel-Storefront - Geschenkoptionen im Warenkorb](./assets/storefront-cart-gift-options-for-products-or-order.png){width="700" zoomable="yes"}

Die Konfiguration der Geschenkoptionen gilt für die gesamte Website, kann jedoch auf Produktebene überschrieben werden.

### Geschenkoptionen aktivieren

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bedienfeld den Wert **[!UICONTROL Sales]** und wählen Sie unter &quot;**[!UICONTROL Sales]**&quot;.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) **[!UICONTROL Gift Options]** auf der Seite.

   ![Verkaufskonfiguration - Einstellungen für Geschenkoptionen](../configuration-reference/sales/assets/sales-gift-options.png){width="600" zoomable="yes"}

1. Legen Sie die Optionen für die Geschenkgutschrift entsprechend Ihrer Voreinstellung fest:

   - Wählen Sie für **[!UICONTROL Allow Gift Messages on Order Level]** `Yes` aus, um eine einzelne Geschenknachricht für die gesamte Bestellung zu aktivieren.
   - Wählen Sie für **[!UICONTROL Allow Gift Messages for Order Items]** `Yes` aus, um das Hinzufügen separater Geschenkmeldungen für einzelne Artikel im Warenkorb des Kunden zu aktivieren.

1. ![Adobe Commerce](../assets/adobe-logo.svg) (nur Adobe Commerce) Legen Sie die Geschenkverpackungsoptionen entsprechend Ihrer Voreinstellung fest:

   - Wählen Sie für **[!UICONTROL Allow Gift Wrapping on Order Level]** `Yes` aus, um eine einzelne Geschenkverpackung für die gesamte Bestellung zu aktivieren.
   - Wählen Sie für **[!UICONTROL Allow Gift Wrapping for Order Items]** `Yes` aus, um das individuelle Hinzufügen der Geschenkverpackung zu jedem Artikel im Warenkorb zu aktivieren.

   Sie können auch verschiedene [Geschenkdesigns](#gift-wrap) definieren, damit Kunden die Verpackung wählen können.

1. ![Adobe Commerce](../assets/adobe-logo.svg) (Nur Adobe Commerce) Um Kunden die Möglichkeit zu geben, einen Geschenkgutschein einzuschließen, setzen Sie **[!UICONTROL Allow Gift Receipt]** auf `Yes`.

1. ![Adobe Commerce](../assets/adobe-logo.svg) (Nur Adobe Commerce) Um Kunden die Möglichkeit zu geben, eine gedruckte Karte einzuschließen, setzen Sie **[!UICONTROL Allow Printed Card]** auf `Yes`.

1. ![Adobe Commerce](../assets/adobe-logo.svg) (nur Adobe Commerce) Geben Sie den **[!UICONTROL Default Price for Printed Card]** ein.

1. Klicken Sie auf **[!UICONTROL Save Config]**.

### Geschenkpackung

![Adobe Commerce](../assets/adobe-logo.svg) (nur Adobe Commerce)

Geschenkverpackungen sind für alle Produkte erhältlich, die versandfähig sind, und können für einzelne Artikel oder für die gesamte Bestellung angeboten werden. Sie können für jedes Geschenkverpackungsdesign einen separaten Preis berechnen und ein Miniaturbild für jedes Design hochladen, das als Option für ein Produkt im Warenkorb angezeigt wird. Wenn ein Kunde auf die Miniaturansicht der Geschenkpackung klickt, wird ein Bild in voller Größe angezeigt. Während des Checkout-Reviews wird die Ladung für die Geschenkverpackung mit den anderen [Gesamtsummen für den Checkout](checkout-totals-sort-order.md) im Abschnitt _Bestellzusammenfassung_ angezeigt.

Das Geschenkverpackungsbild sollte ein Muster sein, das das Wiederholungsmuster anzeigt, und kann auch eine Probe des zu verwendenden Band enthalten. Sie können entweder das Papier scannen oder ein Foto eines eingepackten Packages machen. Das hochgeladene Bild kann ein GIF-, JPG- oder PNG-Bild sein und sollte quadratisch sein. Im folgenden Beispiel beträgt das hochgeladene Geschenkverpackungsbild 230 x 230 Pixel.

![Geschenkoptionen im Warenkorb](./assets/storefront-cart-gift-options-gift-wrap.png){width="700" zoomable="yes"}

#### Hinzufügen eines Geschenkverpackungsdesigns

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Other Settings]_>**[!UICONTROL Gift Wrapping]**.

   ![Geschenkraster](./assets/gift-wrapping.png){width="700" zoomable="yes"}

1. Klicken Sie in der oberen rechten Ecke auf **[!UICONTROL Add Gift Wrapping]**.

1. Geben Sie den Namen für die **[!UICONTROL Gift Wrapping Design]** ein, die beim Checkout angezeigt werden soll.

   Bei Bedarf können Sie den **[!UICONTROL Scope]** ändern und für jede Store-Ansicht einen anderen Namen konfigurieren.

1. Wählen Sie die **[!UICONTROL Websites]** aus, wo das Geschenkverpackungsdesign verfügbar ist.

1. Setzen Sie **[!UICONTROL Status]** auf `Enabled`.

   Wenn Sie eine saisonale Wrapping-Option haben, können Sie diese auf `Disabled` setzen, wenn die Option nicht verfügbar sein soll.

1. Geben Sie den **[!UICONTROL Price]** des Geschenkverpackungsdesigns ein.

   Diese Einstellung kann durch den auf der Produktebene festgelegten Geschenkverpackungspreis überschrieben werden.

   ![Neues Geschenk umbrechen](./assets/gift-wrapping-new.png){width="600" zoomable="yes"}

1. Um eine Miniaturansicht **[!UICONTROL Image]** der Geschenkverpackung hochzuladen, klicken Sie auf **[!UICONTROL Choose File]** und wählen Sie die hochzuladende Datei aus Ihrem Verzeichnis aus.

   Eine Miniaturansicht des Bildes wird im _[!UICONTROL Gift Wrapping Information]_angezeigt, nachdem der Datensatz gespeichert wurde.

1. Klicken Sie auf **[!UICONTROL Save]**.

#### Design einer Geschenkpackung bearbeiten

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Other Settings]_>**[!UICONTROL Gift Wrapping]**.

1. Finden Sie den Eintrag der Geschenkverpackung in der Liste.

1. Klicken Sie in der Spalte _Aktion_ auf **[!UICONTROL Edit]**.

   ![Bearbeiten von Geschenkverpackungsinformationen](./assets/gift-wrapping-edit.png){width="600" zoomable="yes"}

1. Nehmen Sie die erforderlichen Änderungen vor.

1. Klicken Sie auf **[!UICONTROL Save]**.

#### Löschen von Geschenkverpackungsdesigns

Wenn das Raster _Geschenkverpackung_ geöffnet ist, verwenden Sie eine dieser Methoden, um Wrap-Designs zu löschen.

**_Methode 1: Löschen eines einzelnen Geschenkverpackungsdesigns_**

1. Öffnen Sie das Geschenkpapier im Bearbeitungsmodus.

1. Klicken Sie oben im Arbeitsbereich auf **[!UICONTROL Delete]**.

1. Klicken Sie nach Aufforderung zur Bestätigung auf **[!UICONTROL OK]** .

**_Methode 2: Löschen mehrerer Geschenkverpackungsentwürfe_**

1. Aktivieren Sie im Raster _Geschenkumbruch_ das Kontrollkästchen der einzelnen Geschenkverpackungsentwürfe, die Sie löschen möchten.

1. Setzen Sie das Steuerelement **[!UICONTROL Actions]** auf `Delete`.

1. Klicken Sie auf **[!UICONTROL Submit]**.

### Steuern auf Geschenkoptionen

![Adobe Commerce](../assets/adobe-logo.svg) (nur Adobe Commerce)

Die Preise für Geschenkverpackungen und gedruckte Geschenkkarten können so konfiguriert werden, dass sie Steuern einschließen oder ausschließen oder beide Optionen anzeigen. Sie können für diese Elemente auch eine Steuerklasse festlegen, entweder auf globaler oder auf Website-Ebene.

**_So konfigurieren Sie die Steuern der Geschenkoptionen:_**

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich den Wert **[!UICONTROL Sales]** und wählen Sie **[!UICONTROL Tax]** aus.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) im Abschnitt **[!UICONTROL Tax Classes]** .

   ![Konfiguration der Steuerklasse](../configuration-reference/sales/assets/tax-tax-classes.png){width="600" zoomable="yes"}

1. Setzen Sie **[!UICONTROL Tax Class for Gift Options]** auf die anwendbare Steuerklasse.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) im Abschnitt **[!UICONTROL Orders, Invoices, Credit Memos Display Settings]** .

   ![Anzeigeeinstellungen für Bestellungen, Rechnungen, Kreditkarten](../configuration-reference/sales/assets/tax-orders-invoices-credit-memos-display-settings.png){width="600" zoomable="yes"}

1. Setzen Sie **[!UICONTROL Display Gift Wrapping Prices]** auf einen der folgenden Werte:

   - `Excluding Tax`
   - `Including Tax`
   - `Including and Excluding Tax`

1. Setzen Sie **[!UICONTROL Display Printed Card Prices]** auf einen der folgenden Werte:

   - `Excluding Tax`
   - `Including Tax`
   - `Including and Excluding Tax`

1. Klicken Sie auf **[!UICONTROL Save Config]**.
