---
title: Steuerkonfigurationseinstellungen
description: Erfahren Sie, wie Sie grundlegende Steuereinstellungen konfigurieren, einschließlich Steuerklassen, Berechnungen und des standardmäßigen Steuerziels.
exl-id: e32747f9-20d0-4717-9cee-aa1bcffebb65
feature: Taxes
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '1052'
ht-degree: 0%

---

# Steuerkonfigurationseinstellungen

Die folgenden Anweisungen führen Sie durch die grundlegende Steuerkonfiguration für Ihre Commerce-Instanz. Bevor Sie Ihre Steuern einrichten, sollten Sie sich mit den steuerlichen Anforderungen Ihrer [locale](store-localize.md#step-3-change-the-locale-of-the-store-view). Schließen Sie dann die Steuerkonfiguration entsprechend Ihren Anforderungen ab.

Admin [Berechtigungen](../systems/permissions.md) kann auf [access](../systems/permissions-user-roles.md) auf der Grundlage des Geschäfts steuerliche Mittel, _Notwendigkeit zu wissen_. Um eine Administratorrolle mit Zugriff auf Steuereinstellungen zu erstellen, wählen Sie die Ressourcen Verkauf/Steuern und System/Steuern aus. Wenn Sie eine Website für eine Region einrichten, die sich von Ihrem standardmäßigen Versandort unterscheidet, müssen Sie auch den Zugriff auf die System-/Versandressourcen für die Rolle zulassen. Die Versandeinstellungen bestimmen den für Katalogpreise verwendeten Steuersatz.

## Allgemeine Steuereinstellungen konfigurieren

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Für eine Multisite-Konfiguration legen Sie **[!UICONTROL Store View]** auf die Website klicken und speichern, das das Ziel der Konfiguration ist.

1. Erweitern Sie im linken Bereich **[!UICONTROL Sales]** und wählen **[!UICONTROL Tax]**.

1. Führen Sie die folgenden Konfigurationseinstellungen aus.

   Falls erforderlich, löschen Sie die **[!UICONTROL Use system value]** Kontrollkästchen aller abgeblendeten Einstellungen.

### [!UICONTROL Tax Classes]

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL Tax Classes]** Abschnitt.

   ![Steuerklassen](../configuration-reference/sales/assets/tax-tax-classes.png){width="600" zoomable="yes"}

   - **Steuerklasse für den Versand** — Wird auf die entsprechende Klasse gesetzt. Die Standardklassen sind: `None` und `Taxable Goods`
   - **Steuerklasse für Geschenkoptionen** — ![Adobe Commerce](../assets/adobe-logo.svg) (Nur Adobe Commerce) Stellen Sie auf die entsprechende Klasse ein. Die Standardklassen sind: `None` und `Taxable Goods`
   - **Standardsteuerklasse für das Produkt** — Wird auf die entsprechende Klasse gesetzt. Die Standardklassen sind: `None` und `Taxable Goods`
   - **Standardsteuerklasse für Kunden** — Wird auf die entsprechende Klasse gesetzt. Die Standardklasse lautet: `Retail Customer` und `Wholesale Customer`

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save Config]**.

### [!UICONTROL Calculation Settings]

1. Erweitern Sie die **[!UICONTROL Calculation Settings]** Abschnitt.

   ![Berechnungseinstellungen](../configuration-reference/sales/assets/tax-calculation-settings.png){width="600" zoomable="yes"}

1. Satz **[!UICONTROL Tax Calculation Method Based On]** auf einen der folgenden Werte zu:

   - `Unit Price` - Preis jedes Erzeugnisses
   - `Row Total` - Gesamtwert des Zeileneintrags in der Bestellung, abzüglich Rabatte
   - `Total` - Bestellsumme

1. Satz **[!UICONTROL Tax Calculation Based On]** auf einen der folgenden Werte zu:

   - `Shipping Address` - Anschrift, an die die Bestellung versandt werden soll
   - `Billing Address` - Rechnungsadresse des Kunden oder Unternehmens
   - `Shipping Origin` - Die Adresse, die als [Ursprungsort](shipping-settings.md#point-of-origin) für Ihren Store

1. Satz **[!UICONTROL Catalog Prices]** nach `Excluding Tax` oder `Including Tax`.

1. Satz **[!UICONTROL Shipping Prices]** nach `Excluding Tax` oder `Including Tax`.

1. Satz **[!UICONTROL Apply Customer Tax]** auf einen der folgenden Punkte zu setzen, um festzustellen, ob die Steuer auf den ursprünglichen oder den ermäßigten Preis angewendet wird: `After Discount` oder `Before Discount`

1. Satz **[!UICONTROL Apply Discount on Prices]** auf einen der folgenden Punkte zu setzen, um festzustellen, ob Rabatte Steuern enthalten oder ausschließen: `Excluding Tax` oder `Including Tax`

1. Satz **[!UICONTROL Apply Tax On]** nach `Custom price if available` oder `Original price only`.

1. Satz **[!UICONTROL Enable Cross-Border Trade]** auf einen der folgenden Werte zu:

   - `Yes` - Einheitliche Preisgestaltung über verschiedene Steuersätze hinweg. Wenn der Katalogpreis Steuern enthält, wählen Sie diese Einstellung, um den Preis unabhängig vom Steuersatz des Kunden festzusetzen.
   - `No` - Variieren Sie den Preis nach Steuersatz.

   >[!IMPORTANT]
   >
   >Wenn [grenzüberschreitender Handel](#cross-border-price-consistency) aktiviert ist, ändert sich die Gewinnspanne nach Steuersatz. Der Gewinn wird anhand der Formel (`Revenue - CustomerVAT - CostOfGoodsSold`). Um den grenzüberschreitenden Handel zu ermöglichen, müssen die Preise so festgesetzt werden, dass sie die Steuer einschließen.

### [!UICONTROL Default Tax Destination Calculation]

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL Default Tax Destination Calculation]** Abschnitt.

   ![Standardmäßige Berechnung des Steuerziels](../configuration-reference/sales/assets/tax-default-tax-destination-calculation.png){width="600" zoomable="yes"}

1. Geben Sie die **[!UICONTROL Default Country]** für Steuerberechnungen.

1. Falls zutreffend, geben Sie die **[!UICONTROL Default State]** für Steuerberechnungen.

1. Falls zutreffend, geben Sie die **[!UICONTROL Default Post Code]** für Steuerberechnungen.

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save Config]**.

### [!UICONTROL Price Display Settings]

>[!IMPORTANT]
>
>Einige Kombinationen von Einstellungen, die sich auf eine Preisanzeige beziehen und sowohl die Steuer einschließen als auch die Steuer ausschließen, können für den Kunden verwirrend sein. Um das Auslösen einer Warnmeldung zu vermeiden, lesen Sie den Abschnitt [empfohlene Einstellungen](taxes.md#warning-messages).

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL Price Display Settings]** Abschnitt.

   ![Preisanzeigeeinstellungen](../configuration-reference/sales/assets/tax-price-display-settings.png){width="600" zoomable="yes"}

1. Satz **[!UICONTROL Display Product Prices in Catalog]** auf einen der folgenden Werte zu:

   - `Excluding Tax` - Die Katalogpreise, die in der Storefront erscheinen, beinhalten keine Steuern.
   - `Including Tax` - Die Katalogpreise in der Storefront beinhalten nur dann die Steuer, wenn eine Steuervorschrift mit der steuerlichen Herkunft übereinstimmt oder wenn die Adresse des Kunden mit der Steuervorschrift übereinstimmt. Dies kann geschehen, nachdem ein Kunde ein Konto erstellt, sich angemeldet oder das Tool für die geschätzte Steuer und den Versand im Warenkorb verwendet hat.
   - `Including and Excluding Tax` - In der Storefront angezeigte Katalogpreise werden sowohl mit als auch ohne Steuern angezeigt.

1. Satz **[!UICONTROL Display Shipping Prices]** nach `Excluding Tax`, `Including Tax`oder `Including and Excluding Tax`.

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save Config]**.

### [!UICONTROL Shopping Cart Display Settings]

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL Shopping Cart Display Settings]** Abschnitt.

   ![Anzeigeeinstellungen für Warenkorb](../configuration-reference/sales/assets/tax-shopping-cart-display-settings.png){width="600" zoomable="yes"}

1. Wählen Sie für jede der folgenden Einstellungen aus, wie Steuern und Preise im Warenkorb angezeigt werden sollen, entsprechend den Anforderungen Ihres Stores und Gebietsschemas:

   - Satz **[!UICONTROL Display Prices]** nach `Excluding Tax`, `Including Tax`oder `Including and Excluding Tax`.

   - Satz **[!UICONTROL Display Subtotal]** nach `Excluding Tax`, `Including Tax`oder `Including and Excluding Tax`.

   - Satz **[!UICONTROL Display Shipping Amount]** nach `Excluding Tax`, `Including Tax`oder `Including and Excluding Tax`.

   - ![Adobe Commerce](../assets/adobe-logo.svg) (Nur Adobe Commerce) Festlegen **[!UICONTROL Display Gift Wrapping Prices]** nach `Excluding Tax`, `Including Tax`oder `Including and Excluding Tax`.

   - ![Adobe Commerce](../assets/adobe-logo.svg) (Nur Adobe Commerce) Festlegen **[!UICONTROL Display Printed Card Prices]** nach `Excluding Tax`, `Including Tax`oder `Including and Excluding Tax`.

1. Legen Sie die folgenden Anzeigeoptionen auf Folgendes fest: `Yes` oder `No`entsprechend Ihren Anforderungen:

   - **[!UICONTROL Include Tax in Order Total]**
   - **[!UICONTROL Display Full Tax Summary]**
   - **[!UICONTROL Display Zero Tax Subtotal]**

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save Config]**.

### [!UICONTROL Orders, Invoices, Credit Memos Display Settings]

1. Erweitern ![Erweiterung](../assets/icon-display-expand.png) die **[!UICONTROL Orders, Invoices, Credit Memos Display Settings]** Abschnitt.

   ![Anzeigeeinstellungen für Bestellungen, Rechnungen, Credit Memos](../configuration-reference/sales/assets/tax-orders-invoices-credit-memos-display-settings.png){width="600" zoomable="yes"}

1. Geben Sie an, wie Preise und Steuern in Bestellungen, Rechnungen und Kreditkarten angezeigt werden:

   - Satz **[!UICONTROL Display Prices]** nach `Excluding Tax`, `Including Tax`oder `Including and Excluding Tax`.

   - Satz **[!UICONTROL Display Subtotal]** nach `Excluding Tax`, `Including Tax`oder `Including and Excluding Tax`.

   - Satz **[!UICONTROL Display Shipping Amount]** nach `Excluding Tax`, `Including Tax`oder `Including and Excluding Tax`.

   - ![Adobe Commerce](../assets/adobe-logo.svg) (Nur Adobe Commerce) Festlegen **[!UICONTROL Display Gift Wrapping Prices]** nach `Excluding Tax`, `Including Tax`oder `Including and Excluding Tax`.

   - ![Adobe Commerce](../assets/adobe-logo.svg) (Nur Adobe Commerce) Festlegen **[!UICONTROL Display Printed Card Prices]** nach `Excluding Tax`, `Including Tax`oder `Including and Excluding Tax`.

1. Legen Sie die folgenden Anzeigeoptionen auf `Yes` oder `No`, entsprechend Ihren Anforderungen:

   - **[!UICONTROL Include Tax in Order Total]**
   - **[!UICONTROL Display Full Tax Summary]**
   - **[!UICONTROL Display Zero Tax Subtotal]**

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save Config]**.

### [!UICONTROL Fixed Product Taxes]

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL Fixed Product Taxes]** Abschnitt.

   ![Feste Produktsteuern](../configuration-reference/sales/assets/tax-fixed-product-taxes.png){width="600" zoomable="yes"}

1. Satz **[!UICONTROL Enable FPT]** entweder `Yes` oder `No`, entsprechend Ihren Anforderungen.

1. Wenn FPT aktiviert ist, legen Sie die FPT-Anzeigeoptionen fest:

   - **[!UICONTROL Display Prices in Product Lists]**
   - **[!UICONTROL Display Price On Product view Page]**
   - **[!UICONTROL Display Prices in Sales Modules]**
   - **[!UICONTROL Display Prices in Emails]**

   - `Including FPT Only` - Die angezeigten Preise beinhalten die festen Produktsteuern. Der FPT-Betrag wird nicht separat angezeigt.
   - `Including FPT and FPT description` - Die angezeigten Preise beinhalten die festen Produktsteuern. Der FPT-Betrag wird separat angezeigt.
   - `Excluding FPT. Including FPT description and final price` - Die angegebenen Preise enthalten keine festen Produktsteuern. Der FPT-Betrag wird separat angezeigt.
   - `Excluding FPT` - Die angegebenen Preise enthalten keine festen Produktsteuern. Der FPT-Betrag wird nicht separat angezeigt.

1. Satz **[!UICONTROL Apply Discounts to FPT]** nach `Yes` oder `No`, entsprechend Ihren Anforderungen.

1. Satz **[!UICONTROL FPT Tax Configuration]** um zu bestimmen, wie die FPT berechnet wird.

   - `Not Taxed` - Wählen Sie diese Option aus, wenn Ihr Steuergebiet FPT nicht besteuert. (Zum Beispiel Kalifornien.)
   - `Taxed` - Wählen Sie diese Option aus, wenn Ihr Steuergebiet FPT besteuert. (Beispiel: Kanada.)
   - `Loaded and Displayed with Tax` - Klicken Sie auf diese Option, wenn FPT vor der Anwendung der Steuer zur Bestellsumme hinzugefügt wird. (Zum Beispiel EU-Länder.)

1. Satz **[!UICONTROL Include FPT in Subtotal]** nach `Yes` oder `No`, entsprechend Ihren Anforderungen.

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save Config]**.

## Grenzüberschreitende Preiskonsistenz

Der grenzübergreifende Handel (auch als Preiskonsistenz bezeichnet) unterstützt die Europäische Union (EU) und andere Händler, die einheitliche Preise für Kunden anstreben, deren Steuersätze sich vom Steuersatz der Verkaufsstellen unterscheiden.

Händler, die regional und geografisch tätig sind, können einen einzigen Preis anzeigen, indem sie die Steuer in den Preis des Produkts einbeziehen. Die Preise sind sauber und unübersichtlich, unabhängig von den Steuerstrukturen und Steuersätzen, die von Land zu Land variieren. Diese Einstellungen erfordern, dass eine Erweiterung der Steuerberechnung über die [Marketplace](../getting-started/commerce-marketplace.md), beispielsweise _Vertex Cloud_.

>[!NOTE]
>
>Wenn der grenzüberschreitende Handel aktiviert ist, ändert sich Ihre Gewinnspanne nach Steuersatz. Der Gewinn wird anhand der Formel bestimmt:<br>
>`Revenue - CustomerVAT - CostOfGoodsSold`

**_Gewährleistung der grenzüberschreitenden Preiskonsistenz:_**

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Für eine Multisite-Konfiguration legen Sie **[!UICONTROL Store View]** auf die Website klicken und speichern, das das Ziel der Konfiguration ist.

1. Erweitern Sie im linken Bereich **[!UICONTROL Sales]** und wählen **[!UICONTROL Tax]**.

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL Calculation Settings]** Abschnitt.

1. Satz **[!UICONTROL Catalog Prices]** nach `Including Tax`.

1. Um eine grenzüberschreitende Preiskonsistenz zu ermöglichen, legen Sie **[!UICONTROL Enable Cross Border Trade]** nach `Yes`.

   ![Aktivieren der Einstellungen für den grenzüberschreitenden Handel](./assets/cross-border-calculations-settings.png){width="600" zoomable="yes"}

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save Config]**.
