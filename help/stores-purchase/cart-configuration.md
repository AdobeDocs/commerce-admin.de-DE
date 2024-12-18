---
title: Warenkorbkonfiguration
description: Erfahren Sie mehr über die Funktionen des Warenkorbs, die Sie konfigurieren können, um das Kauferlebnis in Ihrem Geschäft zu unterstützen.
exl-id: b98ec7ce-9354-4f03-b67e-dd1587f0c866
feature: Shopping Cart, Configuration
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '2449'
ht-degree: 0%

---

# Warenkorbkonfiguration

Die Konfiguration des Warenkorbs bestimmt, wie der Warenkorb für Ihre Store-Kunden funktioniert, einschließlich der Fälle, in denen der Kunde zur Warenkorbseite weitergeleitet wird und welche Bilder für Produktminiaturen verwendet werden. Sie können auch eine Bestellung verlangen, um einen Mindestbetrag zu erreichen, bevor der Checkout-Prozess beginnt, die Anzahl der Tage angeben, die die angegebenen Preise gültig bleiben, und die Reihenfolge der Artikel im Abschnitt _Bestellsummen_ angeben.

[**Mini-Warenkorb**](#mini-cart) - Konfigurieren Sie diese Option, um festzustellen, ob der Warenkorb-Link/das Symbol die Anzahl der verschiedenen Produkte (oder SKUs) im Warenkorb oder die Gesamtmenge aller Artikel anzeigt.

[**Mini-Warenkorb-Link**](#configure-the-cart-link) - Konfigurieren Sie diese Option, um zu bestimmen, ob der Mini-Warenkorb angezeigt wird, wenn ein Kunde auf die Anzahl der Artikel im Warenkorb-Symbol oben auf einer Shop-Seite klickt.

[**Zum Warenkorb umleiten**](#redirect-to-cart) - Konfigurieren Sie diese Option, um zu bestimmen, ob die Warenkorbseite immer dann angezeigt wird, wenn ein Artikel zum Warenkorb hinzugefügt wird, oder nur dann, wenn ein Kunde zur Seite wechselt.

[**Angebotslebensdauer**](#quote-lifetime) - Konfigurieren Sie diese Option, um anzugeben, wie lange ein Preis gültig ist.

[**Mindestbestellbetrag**](#minimum-order-amount) - Konfigurieren Sie diese Optionen, um einen Mindestbetrag anzugeben, den die Zwischensummen der Bestellungen nach Anwendung der Rabatte einhalten müssen, und die im Warenkorb angezeigte Nachricht.

[**Mindestbestellmenge**](#minimum-order-quantity) - Konfigurieren Sie diese Optionen, um eine Mindestanzahl von Artikeln anzugeben, die für die Bestellung erforderlich sind.

[**Warenkorbminiaturen**](#cart-thumbnails) - Konfigurieren Sie die Optionen für Warenkorbminiaturen, um die Miniaturen zu bestimmen, die im Warenkorb für gruppierte oder konfigurierbare Produkte angezeigt werden.

[**Geschenkoptionen**](#gift-options) - Konfigurieren Sie Geschenkoptionen, um festzustellen, ob Kunden eine Geschenknachricht oder eine Grußkarte hinzufügen können, und ob Geschenkverpackungsoptionen verfügbar sind.

>[!NOTE]
>
>Informationen zum Konfigurieren des Checkout-Prozesses finden Sie unter [Checkout-Optionen](checkout-process.md).

## Mini-Cart

Der _Mini-_) zeigt eine Zusammenfassung der Artikel im Warenkorb an. Sie ist standardmäßig aktiviert und wird angezeigt, wenn Sie oben auf der Seite auf den Link „Warenkorb“ klicken.
Der Link kann so konfiguriert werden, dass die Anzahl verschiedener Produkte (oder SKUs) im Warenkorb oder die Gesamtmenge aller Artikel angezeigt wird.

![Der Käufer zeigt die Seitenleiste des Warenkorbs von einer Produktseite aus an](./assets/storefront-mini-cart-watch.png){width="700" zoomable="yes"}

>[!NOTE]
>
>Bei _(registrierten_ Kunden gibt es Fälle, in denen der Mini-Warenkorb möglicherweise nicht über mehrere Geräte und Browser hinweg automatisch synchronisiert wird. Um in solchen Fällen den Mini-Warenkorb zu synchronisieren, kann der Kunde einfach die Seite [Warenkorb](cart.md) auf diesem Gerät oder Browser öffnen.

### Konfigurieren des Mini-Cart

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Sales]** und wählen Sie **[!UICONTROL Checkout]**.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt _[!UICONTROL Mini Cart]_.

   ![Konfigurieren des Mini-Warenkorbs](../configuration-reference/sales/assets/checkout-mini-cart.png){width="600" zoomable="yes"}

1. Wenn die Einstellung für eine bestimmte Store-Ansicht ist, wählen [die Store-Ansicht aus](../configuration-reference/scope-change.md#set-the-scope) für die die Konfiguration gilt.

   Wenn Sie dazu aufgefordert werden, klicken Sie auf **[!UICONTROL OK]** , um fortzufahren.

1. Legen Sie **[!UICONTROL Display Mini Cart]** auf eine der folgenden Einstellungen fest:

   - `Yes` - Zeigt den Mini-Warenkorb auf Store-Seiten an. Das Erscheinungsbild der Seitenleiste hängt vom Design ab.
   - `No` - Deaktiviert die Anzeige des Mini-Warenkorbs auf Store-Seiten.

1. Wenn die Anzeige aktiviert ist, aktualisieren Sie die anderen Optionen, um die Anzeige zu konfigurieren:

   - Geben Sie **[!UICONTROL Number of Items to Display Scrollbar]** die Anzahl der Elemente ein, die in der Seitenleiste angezeigt werden können, bevor die Bildlaufleiste ausgelöst wird.
   - Geben Sie **[!UICONTROL Maximum Display Recently Added Item(s)]** die maximale Anzahl der kürzlich hinzugefügten Artikel ein, die im Mini-Warenkorb angezeigt werden sollen.

1. Klicken Sie auf **[!UICONTROL Save Config]**.

### Konfigurieren des Warenkorb-Links

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Sales]** und wählen Sie **[!UICONTROL Checkout]**.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL My Cart Link]** .

1. Legen Sie **[!UICONTROL Display Cart Summary]** auf eine der folgenden Einstellungen fest:

   - `Display item quantities` - Diese Einstellung zeigt die Gesamtzahl der Produkte im Warenkorb an, wobei die Mengen für jedes Produkt hinzugefügt werden.
   - `Display number of items in cart` - Diese Einstellung zeigt die Anzahl der Artikel im Warenkorb an, unabhängig von der Menge.

   ![Konfigurationsoptionen für „Link zum Warenkorb“](../configuration-reference/sales/assets/checkout-my-cart-link.png){width="600" zoomable="yes"}

1. Klicken Sie auf **[!UICONTROL Save Config]**.

## Zu Warenkorb umleiten

Die Warenkorbseite kann so konfiguriert werden, dass sie immer dann angezeigt wird, wenn ein Artikel zum Warenkorb hinzugefügt wird, oder nur dann, wenn Kunden zur Seite gehen. Die grundlegenden Informationen zu den Artikeln, die sich derzeit im Warenkorb befinden, sind immer im [Mini-Warenkorb](#mini-cart) verfügbar. Bei der Entscheidung geht es darum, die Vorteile, die es hat, wenn die Kunden weiterhin einkaufen, mit den Vorteilen abzuwägen, die es hat, wenn die Kunden zum Checkout ermutigt werden. Es könnte eine einfache Frage persönlicher Präferenz sein. Wenn Sie sie jedoch mit Zahlen sichern möchten, können Sie einen A/B-Test durchführen, um zu sehen, welcher Ansatz eine höhere Konversionsrate erzeugt.

**_So konfigurieren Sie, wann der Warenkorb angezeigt wird:_**

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Sales]** und wählen Sie **[!UICONTROL Checkout]**.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Shopping Cart]** .

   ![Die Konfigurationseinstellungen für den Warenkorb wurden auf der Seite erweitert](../configuration-reference/sales/assets/checkout-shopping-cart.png){width="600" zoomable="yes"}

1. Wenn die Einstellung für eine bestimmte Store-Ansicht ist, wählen [die Store-Ansicht aus](../configuration-reference/scope-change.md#set-the-scope) für die die Konfiguration gilt.

   Wenn Sie dazu aufgefordert werden, klicken Sie auf **[!UICONTROL OK]** , um fortzufahren.

1. Legen Sie **[!UICONTROL After Adding a Product Redirect to Shopping Cart]** auf eine der folgenden Einstellungen fest:

   - `Yes` - Zeigt die Warenkorbseite unmittelbar nach dem Hinzufügen eines Produkts zum Warenkorb an.
   - `No` - Deaktiviert die Umleitung zum Warenkorb nach dem Hinzufügen eines Produkts zum Warenkorb.

1. Klicken Sie auf **[!UICONTROL Save Config]**.

## Angebotslebensdauer

Mit der Installation und Aktivierung von Adobe Commerce B2B können Sie Unterstützung für die Funktion _Quotes_ hinzufügen. Mit dieser Funktion können autorisierte Käufer den Prozess der Preisaushandlung starten, indem sie eine Anfrage aus dem Warenkorb senden. Das _Quotes_-Raster listet jedes erhaltene Angebot auf und bewahrt einen Verlauf der Kommunikation zwischen Käufer und Verkäufer auf. Weitere Informationen zu den B2B-Funktionen finden Sie unter [Ausgehandelte ](../b2b/quotes.md)) im _Adobe Commerce B2B-Benutzerhandbuch_.

Sie können feststellen, wie lange ein Preis gültig ist, indem Sie die Lebensdauer des Warenkorbangebots in der Konfiguration festlegen. Wenn beispielsweise ein Käufer einen Warenkorb nach mehreren Tagen unbeaufsichtigt lässt, ist der Angebotspreis für einige Artikel möglicherweise nicht mehr identisch. Standardmäßig ist die Lebensdauer des Angebots auf 30 Tage festgelegt.

**_So konfigurieren Sie die Angebotslebensdauer:_**

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Sales]** und wählen Sie **[!UICONTROL Checkout]**.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Shopping Cart]** .

   ![Die Konfigurationseinstellungen für den Warenkorb wurden auf der Seite erweitert](../configuration-reference/sales/assets/checkout-shopping-cart.png){width="600" zoomable="yes"}

1. Wenn die Einstellung für eine bestimmte Store-Ansicht ist, wählen [die Store-Ansicht aus](../configuration-reference/scope-change.md#set-the-scope) für die die Konfiguration gilt.

   Wenn Sie dazu aufgefordert werden, klicken Sie auf **[!UICONTROL OK]** , um fortzufahren.

1. Geben Sie **[!UICONTROL Quote Lifetime (days)]** die Anzahl der Tage ein, an denen ein angegebener Preis gültig bleibt.

1. Klicken Sie auf **[!UICONTROL Save Config]**.

## Mindestbestellmenge

Mit der Konfiguration können Sie einen Mindestbetrag angeben, den Zwischensummen für Bestellungen nach der Anwendung von Rabatten einhalten müssen. Bestellungen, die an mehrere Adressen gesendet werden, können erforderlich sein, um den Mindestbestellbetrag pro Adresse zu erfüllen. Die Checkout-Schaltfläche ist erst verfügbar, nachdem der Mindestbestellwert erreicht wurde.

![Der Warenkorb zeigt eine Nachricht zur Mindestbestellung an](./assets/storefront-cart-minimum-order-amount.png){width="700" zoomable="yes"}

**_So konfigurieren Sie eine Mindestbestellmenge:_**

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Sales]** und wählen Sie darunter **[!UICONTROL Sales]**.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Minimum Order Amount]** .

   ![Die Konfigurationsoptionen für die Mindestreihenfolge wurden auf der Seite erweitert](../configuration-reference/sales/assets/sales-minimum-order-amount.png){width="600" zoomable="yes"}

1. Um einen Mindestbestellbetrag zu verlangen, setzen Sie **[!UICONTROL Enable]** auf `Yes`.

1. Wenn die Mindestreihenfolge aktiviert ist, stellen Sie die folgenden Optionen ein, um die Anforderung zu konfigurieren:

   - Geben Sie die **[!UICONTROL Minimum Amount]** ein, die für die Zwischensumme erforderlich ist, nachdem Rabatte angewendet wurden.

   - Legen Sie **[!UICONTROL Include Discount Amount]** auf eine der folgenden Einstellungen fest:

      - `Yes` - Erfordert, dass die Zwischensumme den Mindestbetrag mit etwaigen Rabatten erfüllt. Unter Verwendung eines Beispiels für mindestens 50 $ würde, wenn der Warenkorb eine Obergrenze von 60 $ mit einem angewendeten Rabatt von 25 % enthält, die resultierende Zwischensumme 45 $ betragen und der Warenkorb das Minimum nicht erfüllen würde.
      - `No` - Erfordert, dass die Zwischensumme den Mindestbetrag ohne Rabatte erfüllt.

   - Legen Sie **[!UICONTROL Include Tax to Amount]** auf eine der folgenden Einstellungen fest:

      - `Yes` - Erfordert, dass die Zwischensumme den Mindestbetrag mit eingeschlossener Steuer erreicht.
      - `No` - Erfordert, dass die Zwischensumme den Mindestbetrag ohne Steuer erreicht.

1. Optional können Sie die Nachrichteneinstellungen für den Mindestbestellwert anpassen:

   - Geben Sie **[!UICONTROL Description Message]** den Text ein, mit dem Sie die Nachricht anpassen möchten, die oben im Warenkorb angezeigt wird, wenn die Zwischensumme nicht den Mindestbetrag erreicht.

   - Geben Sie **[!UICONTROL Error to Show in Shopping Cart]** den Text ein, mit dem Sie die Fehlermeldung zum Warenkorb anpassen möchten.

   Lassen Sie die Felder für die Nachrichtenbeschreibung leer, um die Standardnachrichten zu verwenden.

1. Konfigurieren Sie bei Bedarf die Einstellung Mindestbestellmenge für Bestellungen mit mehreren Adressen:

   - Um zu verlangen, dass jede Adresse in einer Bestellung mit mehreren Adressen den Mindestbestellwert erreicht, setzen Sie **[!UICONTROL Validate Each Address Separately in Multi-address Checkout]** auf `Yes`.

   - Optional können Sie die Nachrichteneinstellungen für den Mindestbestellwert anpassen:

      - **[!UICONTROL Multi-address Description Message]** - Geben Sie den Text ein, mit dem Sie die Nachricht anpassen möchten, die oben im Warenkorb für Bestellungen mit mehreren Adressen angezeigt wird, die nicht das Minimum erfüllen.

      - **[!UICONTROL Multi-address Error to Show in Shopping Cart]** - Geben Sie den Text in das Feld ein, mit dem Sie die Fehlermeldung für den Warenkorb bei Bestellungen mit mehreren Adressen, die nicht den Mindestwert erreichen, anpassen möchten.

     Lassen Sie die Felder für die Nachrichtenbeschreibung leer, um die Standardnachrichten zu verwenden.

1. Klicken Sie auf **[!UICONTROL Save Config]**.

## Mindestbestellmenge

Sie können die für einen Auftrag zulässige Mindestmenge festlegen. Die Mindestmenge kann auch entsprechend jeder Kundengruppe konfiguriert werden.

1. Navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Catalog]** und wählen Sie **[!UICONTROL Inventory]**.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Product Stock Options]** .

   ![Produktaktienoptionen](../configuration-reference/catalog/assets/catalog-inventory-product-stock-options.png){width="600" zoomable="yes"}

1. Legen Sie **[!UICONTROL Minimum Qty Allowed in Shopping Cart]** die Mindestmenge des Produkts für eine Bestellung fest.

   Deaktivieren Sie bei Bedarf das Kontrollkästchen **[!UICONTROL Use system value]** , um diese Einstellungen zu ändern.

   - Ändern Sie die **[!UICONTROL Customer Group]** auf eine bestimmte Gruppe und geben Sie die **[!UICONTROL Minimum Qty]** für diese Gruppe ein. Um eine weitere Gruppe und ein weiteres Mengenlimit hinzuzufügen, klicken Sie auf **[!UICONTROL Add Minimum Qty]**.

   - Wenn Sie für alle Kunden dieselbe Mindestmenge festlegen möchten, behalten Sie die `ALL GROUPS` Auswahl bei und geben Sie die **[!UICONTROL Minimum Qty]** ein.

1. Klicken Sie auf **[!UICONTROL Save Config]**.

   ![Mindestmengenanforderung im Warenkorb](./assets/minimum-qty-allowed-in-shopping-cart.png){width="700" zoomable="yes"}

## Warenkorb-Miniaturen

![Adobe Commerce](../assets/adobe-logo.svg) (nur Adobe Commerce)

Die im Warenkorb angezeigten Miniaturbilder geben Kundinnen und Kunden einen schnellen Überblick über die Artikel, die sie kaufen werden. Bei Produkten mit mehreren Optionen entspricht das Bild jedoch möglicherweise nicht der Variante des Produkts, das sich im Warenkorb befindet. Wenn der Kunde einen Artikel in einer bestimmten Farbe kauft, sollte idealerweise die Miniaturansicht im Warenkorb übereinstimmen.

Das Miniaturbild für gruppierte und konfigurierbare Produkte kann so eingestellt werden, dass das Bild entweder aus dem übergeordneten Produkt oder aus der Produktvariante angezeigt wird.

![Der Warenkorb zeigt Miniaturbilder für jedes Produkt an](./assets/storefront-cart.png){width="700" zoomable="yes"}

**_So konfigurieren Sie Miniaturansichten für den Warenkorb:_**

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Sales]** und wählen Sie **[!UICONTROL Checkout]**.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Shopping Cart]** .

   ![Die Konfigurationseinstellungen für den Warenkorb wurden auf der Seite erweitert](../configuration-reference/sales/assets/checkout-shopping-cart.png){width="600" zoomable="yes"}

1. Legen Sie **[!UICONTROL Grouped Product Image]** fest, um die Miniaturansicht zu bestimmen, die im Warenkorb für (gruppierte [) verwendet ](../catalog/product-create-grouped.md):

   - `Product Thumbnail Itself` - Verwendet die Miniaturansicht, die der Produktvariante zugewiesen ist, die dem Warenkorb hinzugefügt wird.
   - `Parent Product Thumbnail` - Verwendet die Miniaturansicht, die dem übergeordneten Produkt zugewiesen ist.

1. Legen Sie **[!UICONTROL Configurable Product Image]** fest, um die Miniaturansicht zu bestimmen, die im Warenkorb für ([ Produkte) verwendet ](../catalog/product-create-configurable.md):

   - `Product Thumbnail Itself` - Verwendet die Miniaturansicht, die der Produktvariante zugewiesen ist, die dem Warenkorb hinzugefügt wird.
   - `Parent Product Thumbnail` - Verwendet die Miniaturansicht, die dem übergeordneten Produkt zugewiesen ist.

1. Klicken Sie auf **[!UICONTROL Save Config]**.

## Geschenkoptionen

Die Auswahl der verfügbaren Geschenkoptionen wird im Warenkorb angezeigt, bevor der Checkout-Prozess beginnt. Die Konfiguration der Geschenkoptionen bestimmt, ob Kunden eine Geschenknachricht oder Grußkarte hinzufügen können und ob Geschenkverpackungsoptionen verfügbar sind. Jeder Artikel in der Bestellung kann eine separate Nachricht und Geschenkverpackung haben. Bei Anwendung auf die gesamte Bestellung können Kunden auch einen Geschenkbeleg und eine Grußkarte hinzufügen.

![Beispiel-Storefront - Geschenkoptionen im Warenkorb](./assets/storefront-cart-gift-options-for-products-or-order.png){width="700" zoomable="yes"}

Die Konfiguration der Geschenkoptionen gilt für die gesamte Website, kann jedoch auf Produktebene überschrieben werden.

### Geschenkoptionen aktivieren

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Sales]** und wählen Sie darunter **[!UICONTROL Sales]**.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) **[!UICONTROL Gift Options]** auf der Seite.

   ![Verkaufskonfiguration - Einstellungen für Geschenkoptionen](../configuration-reference/sales/assets/sales-gift-options.png){width="600" zoomable="yes"}

1. Legen Sie die Geschenknachrichtenoptionen nach Ihren Wünschen fest:

   - Wählen Sie **[!UICONTROL Allow Gift Messages on Order Level]** die Option `Yes` aus, um eine einzelne Geschenknachricht für die gesamte Bestellung zu aktivieren.
   - Wählen Sie **[!UICONTROL Allow Gift Messages for Order Items]** die Option `Yes` aus, um das Hinzufügen separater Geschenknachrichten für einzelne Artikel im Warenkorb des Kunden zu aktivieren.

1. ![Adobe Commerce](../assets/adobe-logo.svg) (nur Adobe Commerce) Legen Sie die Optionen für das Geschenkverpacken nach Ihren Wünschen fest:

   - Wählen Sie **[!UICONTROL Allow Gift Wrapping on Order Level]** die Option `Yes` aus, um eine einzelne Geschenkverpackung für die gesamte Bestellung zu aktivieren.
   - Wählen Sie **[!UICONTROL Allow Gift Wrapping for Order Items]** die Option `Yes` aus, um das individuelle Hinzufügen von Geschenkverpackungen zu jedem Artikel im Warenkorb des Kunden zu aktivieren.

   Sie können auch verschiedene [Geschenkverpackungs-Designs) definieren](#gift-wrap) sodass Kunden die Verpackung auswählen können.

1. ![Adobe Commerce](../assets/adobe-logo.svg) (nur Adobe Commerce) Wenn Sie Kundinnen und Kunden die Möglichkeit geben möchten, einen Geschenkgutschein einzuschließen, setzen Sie **[!UICONTROL Allow Gift Receipt]** auf `Yes`.

1. ![Adobe Commerce](../assets/adobe-logo.svg) (nur Adobe Commerce) Legen Sie **[!UICONTROL Allow Printed Card]** auf `Yes` fest, um Kundinnen und Kunden die Möglichkeit zu geben, eine gedruckte Karte einzuschließen.

1. ![Adobe Commerce](../assets/adobe-logo.svg) (nur Adobe Commerce) Geben Sie die **[!UICONTROL Default Price for Printed Card]** ein.

1. Klicken Sie auf **[!UICONTROL Save Config]**.

### Geschenkverpackung

![Adobe Commerce](../assets/adobe-logo.svg) (nur Adobe Commerce)

Geschenkverpackungen sind für jedes Produkt verfügbar, das versendet werden kann, und können für einzelne Artikel oder für die gesamte Bestellung angeboten werden. Sie können für jedes Geschenkpapier-Design einen separaten Preis berechnen und ein Miniaturbild für jedes Design hochladen, das als Option für ein Produkt im Warenkorb angezeigt wird. Wenn ein Kunde auf die Miniaturansicht des Geschenkverpackungs-Fensters klickt, wird ein Bild in voller Größe angezeigt. Während der Kaufbestätigung wird die Gebühr für den Geschenkverpackungsauftrag zusammen mit den anderen [Kaufsummen](checkout-totals-sort-order.md) im Abschnitt _Bestellzusammenfassung_ angezeigt.

Das Geschenkverpackungsbild sollte ein Muster sein, das das sich wiederholende Muster anzeigt, und kann auch ein Beispiel des zu verwendenden Bands enthalten. Sie können entweder das Papier einscannen oder ein Foto von einem verpackten Paket machen. Das hochgeladene Bild kann ein GIF-, JPG- oder PNG-Bild sein und sollte quadratisch sein. Im folgenden Beispiel hat das hochgeladene Geschenkverpackungsbild eine Größe von 230 x 230 Pixel.

![Geschenkoptionen im Warenkorb](./assets/storefront-cart-gift-options-gift-wrap.png){width="700" zoomable="yes"}

#### Geschenkpapier-Design hinzufügen

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Other Settings]_>**[!UICONTROL Gift Wrapping]**.

   ![Geschenkverpackungsraster](./assets/gift-wrapping.png){width="700" zoomable="yes"}

1. Klicken Sie oben rechts auf **[!UICONTROL Add Gift Wrapping]**.

1. Geben Sie den Namen für die **[!UICONTROL Gift Wrapping Design]** ein, die während des Auscheckens angezeigt werden soll.

   Bei Bedarf können Sie die **[!UICONTROL Scope]** ändern und für jede Store-Ansicht einen anderen Namen konfigurieren.

1. Wählen Sie die **[!UICONTROL Websites]** aus, in der das Geschenkpapier-Design verfügbar ist.

1. Legen Sie **[!UICONTROL Status]** auf `Enabled` fest.

   Wenn Sie die Option für das saisonale Verpacken haben, können Sie sie auf `Disabled` setzen, wenn die Option nicht verfügbar sein soll.

1. Geben Sie den **[!UICONTROL Price]** des Geschenkpapier-Designs ein.

   Diese Einstellung kann durch den Geschenkverpackungspreis auf Produktebene außer Kraft gesetzt werden.

   ![Neue Geschenkverpackung](./assets/gift-wrapping-new.png){width="600" zoomable="yes"}

1. Um eine Miniaturansicht **[!UICONTROL Image]** Geschenkverpackung hochzuladen, klicken Sie auf **[!UICONTROL Choose File]** und wählen Sie die hochzuladende Datei aus Ihrem Verzeichnis aus.

   Nach dem Speichern des Datensatzes wird in der _[!UICONTROL Gift Wrapping Information]_eine Miniaturansicht des Bildes angezeigt.

1. Klicken Sie auf **[!UICONTROL Save]**.

#### Bearbeiten eines Geschenkverpackungsdesigns

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Other Settings]_>**[!UICONTROL Gift Wrapping]**.

1. Suchen Sie den Geschenkpapier-Datensatz in der Liste.

1. Klicken Sie in _Spalte_ Aktion **[!UICONTROL Edit]** auf.

   ![Informationen zur Geschenkverpackung bearbeiten](./assets/gift-wrapping-edit.png){width="600" zoomable="yes"}

1. Nehmen Sie die erforderlichen Änderungen vor.

1. Klicken Sie auf **[!UICONTROL Save]**.

#### Geschenkpapier-Designs löschen

Verwenden Sie bei geöffnetem _Geschenkumbruch_-Raster eine dieser Methoden, um Umschlagdesigns zu löschen.

**_Methode 1: Löschen eines einzelnen Geschenkverpackungs-Designs_**

1. Öffnen Sie das Design für die Geschenkverpackung im Bearbeitungsmodus.

1. Klicken Sie oben im Arbeitsbereich auf **[!UICONTROL Delete]**.

1. Wenn Sie dazu aufgefordert werden, klicken Sie zur Bestätigung auf **[!UICONTROL OK]** .

**_Methode 2: Löschen mehrerer Geschenkverpackungs-Designs_**

1. Aktivieren _im Raster „Geschenkverpackung_ das Kontrollkästchen jedes Geschenkverpackungs-Designs, das Sie löschen möchten.

1. Setzen Sie das **[!UICONTROL Actions]** auf `Delete`.

1. Klicken Sie auf **[!UICONTROL Submit]**.

### Steuer auf Geschenkoptionen

![Adobe Commerce](../assets/adobe-logo.svg) (nur Adobe Commerce)

Die Preise für Geschenkverpackungen und gedruckte Geschenkkarten können so konfiguriert werden, dass die Steuer ein- oder ausgeschlossen oder beide Optionen angezeigt werden. Sie können für diese Artikel auch eine Steuerklasse angeben, entweder auf globaler Ebene oder auf Website-Ebene.

**_So konfigurieren Sie die Steuern für Geschenkoptionen:_**

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Sales]** und wählen Sie **[!UICONTROL Tax]**.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Tax Classes]** .

   ![Konfiguration der Steuerklasse](../configuration-reference/sales/assets/tax-tax-classes.png){width="600" zoomable="yes"}

1. Setzen Sie **[!UICONTROL Tax Class for Gift Options]** auf die entsprechende Steuerklasse.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Orders, Invoices, Credit Memos Display Settings]** .

   ![Anzeigeeinstellungen für Bestellungen, Rechnungen, Gutschriften](../configuration-reference/sales/assets/tax-orders-invoices-credit-memos-display-settings.png){width="600" zoomable="yes"}

1. Legen Sie **[!UICONTROL Display Gift Wrapping Prices]** auf eine der folgenden Einstellungen fest:

   - `Excluding Tax`
   - `Including Tax`
   - `Including and Excluding Tax`

1. Legen Sie **[!UICONTROL Display Printed Card Prices]** auf eine der folgenden Einstellungen fest:

   - `Excluding Tax`
   - `Including Tax`
   - `Including and Excluding Tax`

1. Klicken Sie auf **[!UICONTROL Save Config]**.
