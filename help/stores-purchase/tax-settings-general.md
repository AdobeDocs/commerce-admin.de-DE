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

Die folgenden Anweisungen führen Sie durch die grundlegende Steuerkonfiguration für Ihre Commerce-Instanz. Stellen Sie vor dem Einrichten Ihrer Steuern sicher, dass Sie mit den Steueranforderungen Ihres [Gebietsschemas](store-localize.md#step-3-change-the-locale-of-the-store-view) vertraut sind. Schließen Sie dann die Steuerkonfiguration entsprechend Ihren Anforderungen ab.

Admin [permissions](../systems/permissions.md) kann so eingestellt werden, dass [access](../systems/permissions-user-roles.md) auf steuerliche Ressourcen beschränkt wird, je nachdem, was das Unternehmen _wissen muss_. Um eine Administratorrolle mit Zugriff auf Steuereinstellungen zu erstellen, wählen Sie die Ressourcen Verkauf/Steuern und System/Steuern aus. Wenn Sie eine Website für eine Region einrichten, die sich von Ihrem standardmäßigen Versandort unterscheidet, müssen Sie auch den Zugriff auf die System-/Versandressourcen für die Rolle zulassen. Die Versandeinstellungen bestimmen den für Katalogpreise verwendeten Steuersatz.

## Allgemeine Steuereinstellungen konfigurieren

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Legen Sie für eine Multisite-Konfiguration **[!UICONTROL Store View]** auf die Website fest und speichern Sie, das das Ziel der Konfiguration ist.

1. Erweitern Sie im linken Bereich den Wert **[!UICONTROL Sales]** und wählen Sie **[!UICONTROL Tax]** aus.

1. Führen Sie die folgenden Konfigurationseinstellungen aus.

   Deaktivieren Sie bei Bedarf das Kontrollkästchen **[!UICONTROL Use system value]** aller abgeblendeten Einstellungen.

### [!UICONTROL Tax Classes]

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) im Abschnitt **[!UICONTROL Tax Classes]** .

   ![Steuerklassen](../configuration-reference/sales/assets/tax-tax-classes.png){width="600" zoomable="yes"}

   - **Steuerklasse für die Schifffahrt** - Wird auf die entsprechende Klasse gesetzt. Die Standardklassen sind: `None` und `Taxable Goods`
   - **Steuerklasse für Geschenkoptionen** - ![Adobe Commerce](../assets/adobe-logo.svg) (nur Adobe Commerce) Auf die entsprechende Klasse gesetzt. Die Standardklassen sind: `None` und `Taxable Goods`
   - **Standardsteuerklasse für Produkt** - Wird auf die entsprechende Klasse gesetzt. Die Standardklassen sind: `None` und `Taxable Goods`
   - **Standardsteuerklasse für Kunden** - Wird auf die entsprechende Klasse gesetzt. Die Standardklasse lautet: `Retail Customer` und `Wholesale Customer`

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save Config]**.

### [!UICONTROL Calculation Settings]

1. Erweitern Sie den Abschnitt **[!UICONTROL Calculation Settings]** .

   ![Berechnungseinstellungen](../configuration-reference/sales/assets/tax-calculation-settings.png){width="600" zoomable="yes"}

1. Setzen Sie **[!UICONTROL Tax Calculation Method Based On]** auf einen der folgenden Werte:

   - `Unit Price` - Der Preis jedes Produkts
   - `Row Total` - Die Summe des Zeileneintrags in der Bestellung, abzüglich Rabatte
   - `Total` - Die Bestellsumme

1. Setzen Sie **[!UICONTROL Tax Calculation Based On]** auf einen der folgenden Werte:

   - `Shipping Address` - Die Adresse, an die die Bestellung versandt werden soll
   - `Billing Address` - Die Rechnungsadresse des Kunden oder Unternehmens
   - `Shipping Origin` - Die Adresse, die als [Ausgangspunkt](shipping-settings.md#point-of-origin) für Ihren Store angegeben ist

1. Setzen Sie **[!UICONTROL Catalog Prices]** auf `Excluding Tax` oder `Including Tax`.

1. Setzen Sie **[!UICONTROL Shipping Prices]** auf `Excluding Tax` oder `Including Tax`.

1. Setzen Sie **[!UICONTROL Apply Customer Tax]** auf einen der folgenden Werte, um zu bestimmen, ob die Steuer auf den ursprünglichen oder den diskontierten Preis angewendet wird: `After Discount` oder `Before Discount`

1. Setzen Sie **[!UICONTROL Apply Discount on Prices]** auf einen der folgenden Punkte, um zu bestimmen, ob Rabatte die Steuer einschließen oder ausschließen: `Excluding Tax` oder `Including Tax`

1. Setzen Sie **[!UICONTROL Apply Tax On]** auf `Custom price if available` oder `Original price only`.

1. Setzen Sie **[!UICONTROL Enable Cross-Border Trade]** auf einen der folgenden Werte:

   - `Yes` - Verschiedene Steuersätze können konsistent beachtet werden. Wenn der Katalogpreis Steuern enthält, wählen Sie diese Einstellung, um den Preis unabhängig vom Steuersatz des Kunden festzusetzen.
   - `No` - Variieren Sie den Preis nach Steuersatz.

   >[!IMPORTANT]
   >
   >Wenn [grenzüberschreitender Handel](#cross-border-price-consistency) aktiviert ist, ändert sich die Gewinnspanne nach Steuersatz. Der Gewinn wird durch die Formel (`Revenue - CustomerVAT - CostOfGoodsSold`) bestimmt. Um den grenzüberschreitenden Handel zu ermöglichen, müssen die Preise so festgesetzt werden, dass sie die Steuer einschließen.

### [!UICONTROL Default Tax Destination Calculation]

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) im Abschnitt **[!UICONTROL Default Tax Destination Calculation]** .

   ![Berechnung des steuerlichen Ziels ](../configuration-reference/sales/assets/tax-default-tax-destination-calculation.png){width="600" zoomable="yes"}

1. Geben Sie den **[!UICONTROL Default Country]** für Steuerberechnungen an.

1. Falls zutreffend, geben Sie den **[!UICONTROL Default State]** für Steuerberechnungen an.

1. Falls zutreffend, geben Sie den **[!UICONTROL Default Post Code]** für Steuerberechnungen an.

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save Config]**.

### [!UICONTROL Price Display Settings]

>[!IMPORTANT]
>
>Einige Kombinationen von Einstellungen, die sich auf eine Preisanzeige beziehen und sowohl die Steuer einschließen als auch die Steuer ausschließen, können für den Kunden verwirrend sein. Um zu vermeiden, dass eine Warnmeldung ausgelöst wird, lesen Sie die [empfohlenen Einstellungen](taxes.md#warning-messages).

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) im Abschnitt **[!UICONTROL Price Display Settings]** .

   ![Preisanzeigeeinstellungen](../configuration-reference/sales/assets/tax-price-display-settings.png){width="600" zoomable="yes"}

1. Setzen Sie **[!UICONTROL Display Product Prices in Catalog]** auf einen der folgenden Werte:

   - `Excluding Tax` - Die in der Storefront angezeigten Katalogpreise enthalten keine Steuern.
   - `Including Tax` - Die Katalogpreise in der Storefront beinhalten nur dann Steuern, wenn eine Steuervorschrift mit der steuerlichen Herkunft übereinstimmt oder wenn die Adresse des Kunden mit der Steuervorschrift übereinstimmt. Dies kann geschehen, nachdem ein Kunde ein Konto erstellt, sich angemeldet oder das Tool für die geschätzte Steuer und den Versand im Warenkorb verwendet hat.
   - `Including and Excluding Tax` - Katalogpreise, die in der Storefront angezeigt werden, werden sowohl mit als auch ohne Steuern angezeigt.

1. Setzen Sie **[!UICONTROL Display Shipping Prices]** auf `Excluding Tax`, `Including Tax` oder `Including and Excluding Tax`.

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save Config]**.

### [!UICONTROL Shopping Cart Display Settings]

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) im Abschnitt **[!UICONTROL Shopping Cart Display Settings]** .

   ![Anzeigeeinstellungen für Warenkorb](../configuration-reference/sales/assets/tax-shopping-cart-display-settings.png){width="600" zoomable="yes"}

1. Wählen Sie für jede der folgenden Einstellungen aus, wie Steuern und Preise im Warenkorb angezeigt werden sollen, entsprechend den Anforderungen Ihres Stores und Gebietsschemas:

   - Setzen Sie **[!UICONTROL Display Prices]** auf `Excluding Tax`, `Including Tax` oder `Including and Excluding Tax`.

   - Setzen Sie **[!UICONTROL Display Subtotal]** auf `Excluding Tax`, `Including Tax` oder `Including and Excluding Tax`.

   - Setzen Sie **[!UICONTROL Display Shipping Amount]** auf `Excluding Tax`, `Including Tax` oder `Including and Excluding Tax`.

   - ![Adobe Commerce](../assets/adobe-logo.svg) (nur Adobe Commerce) Setzen Sie **[!UICONTROL Display Gift Wrapping Prices]** auf `Excluding Tax`, `Including Tax` oder `Including and Excluding Tax`.

   - ![Adobe Commerce](../assets/adobe-logo.svg) (nur Adobe Commerce) Setzen Sie **[!UICONTROL Display Printed Card Prices]** auf `Excluding Tax`, `Including Tax` oder `Including and Excluding Tax`.

1. Legen Sie die folgenden Anzeigeoptionen entsprechend Ihren Anforderungen auf `Yes` oder `No` fest:

   - **[!UICONTROL Include Tax in Order Total]**
   - **[!UICONTROL Display Full Tax Summary]**
   - **[!UICONTROL Display Zero Tax Subtotal]**

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save Config]**.

### [!UICONTROL Orders, Invoices, Credit Memos Display Settings]

1. Erweitern Sie den Abschnitt **[!UICONTROL Orders, Invoices, Credit Memos Display Settings]** um ![Erweiterung](../assets/icon-display-expand.png).

   ![Anzeigeeinstellungen für Bestellungen, Rechnungen, Credit Memos](../configuration-reference/sales/assets/tax-orders-invoices-credit-memos-display-settings.png){width="600" zoomable="yes"}

1. Geben Sie an, wie Preise und Steuern in Bestellungen, Rechnungen und Kreditkarten angezeigt werden:

   - Setzen Sie **[!UICONTROL Display Prices]** auf `Excluding Tax`, `Including Tax` oder `Including and Excluding Tax`.

   - Setzen Sie **[!UICONTROL Display Subtotal]** auf `Excluding Tax`, `Including Tax` oder `Including and Excluding Tax`.

   - Setzen Sie **[!UICONTROL Display Shipping Amount]** auf `Excluding Tax`, `Including Tax` oder `Including and Excluding Tax`.

   - ![Adobe Commerce](../assets/adobe-logo.svg) (nur Adobe Commerce) Setzen Sie **[!UICONTROL Display Gift Wrapping Prices]** auf `Excluding Tax`, `Including Tax` oder `Including and Excluding Tax`.

   - ![Adobe Commerce](../assets/adobe-logo.svg) (nur Adobe Commerce) Setzen Sie **[!UICONTROL Display Printed Card Prices]** auf `Excluding Tax`, `Including Tax` oder `Including and Excluding Tax`.

1. Legen Sie die folgenden Anzeigeoptionen gemäß Ihren Anforderungen entweder auf `Yes` oder auf `No` fest:

   - **[!UICONTROL Include Tax in Order Total]**
   - **[!UICONTROL Display Full Tax Summary]**
   - **[!UICONTROL Display Zero Tax Subtotal]**

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save Config]**.

### [!UICONTROL Fixed Product Taxes]

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) im Abschnitt **[!UICONTROL Fixed Product Taxes]** .

   ![Feste Produktsteuern](../configuration-reference/sales/assets/tax-fixed-product-taxes.png){width="600" zoomable="yes"}

1. Setzen Sie **[!UICONTROL Enable FPT]** gemäß Ihren Anforderungen entweder auf `Yes` oder auf `No`.

1. Wenn FPT aktiviert ist, legen Sie die FPT-Anzeigeoptionen fest:

   - **[!UICONTROL Display Prices in Product Lists]**
   - **[!UICONTROL Display Price On Product view Page]**
   - **[!UICONTROL Display Prices in Sales Modules]**
   - **[!UICONTROL Display Prices in Emails]**

   - `Including FPT Only` - Die angezeigten Preise beinhalten feste Produktsteuern. Der FPT-Betrag wird nicht separat angezeigt.
   - `Including FPT and FPT description` - Die angezeigten Preise beinhalten feste Produktsteuern. Der FPT-Betrag wird separat angezeigt.
   - `Excluding FPT. Including FPT description and final price` - Die angezeigten Preise enthalten keine festen Produktsteuern. Der FPT-Betrag wird separat angezeigt.
   - `Excluding FPT` - Die angezeigten Preise enthalten keine festen Produktsteuern. Der FPT-Betrag wird nicht separat angezeigt.

1. Setzen Sie **[!UICONTROL Apply Discounts to FPT]** gemäß Ihren Anforderungen auf `Yes` oder `No`.

1. Legen Sie **[!UICONTROL FPT Tax Configuration]** fest, um zu bestimmen, wie FPT berechnet wird.

   - `Not Taxed` - Wählen Sie diese Option aus, wenn Ihr Steuergebiet die FPT nicht besteuert. (Zum Beispiel Kalifornien.)
   - `Taxed` - Wählen Sie diese Option aus, wenn Ihr Steuergebiet FPT besteuert. (Beispiel: Kanada.)
   - `Loaded and Displayed with Tax` - Klicken Sie auf diese Option, wenn die FPT vor Anwendung der Steuer zur Bestellsumme hinzugefügt wird. (Zum Beispiel EU-Länder.)

1. Setzen Sie **[!UICONTROL Include FPT in Subtotal]** gemäß Ihren Anforderungen auf `Yes` oder `No`.

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save Config]**.

## Grenzüberschreitende Preiskonsistenz

Der grenzübergreifende Handel (auch als Preiskonsistenz bezeichnet) unterstützt die Europäische Union (EU) und andere Händler, die einheitliche Preise für Kunden anstreben, deren Steuersätze sich vom Steuersatz der Verkaufsstellen unterscheiden.

Händler, die regional und geografisch tätig sind, können einen einzigen Preis anzeigen, indem sie die Steuer in den Preis des Produkts einbeziehen. Die Preise sind sauber und unübersichtlich, unabhängig von den Steuerstrukturen und Steuersätzen, die von Land zu Land variieren. Diese Einstellungen erfordern, dass eine Steuerberechnungserweiterung über den [Marketplace](../getting-started/commerce-marketplace.md) installiert wird, z. B. _Vertex Cloud_.

>[!NOTE]
>
>Wenn der grenzüberschreitende Handel aktiviert ist, ändert sich Ihre Gewinnspanne nach Steuersatz. Der Gewinn wird durch folgende Formel bestimmt:<br>
>`Revenue - CustomerVAT - CostOfGoodsSold`

**_So aktivieren Sie die grenzüberschreitende Preiskonsistenz:_**

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Legen Sie für eine Multisite-Konfiguration **[!UICONTROL Store View]** auf die Website fest und speichern Sie, das das Ziel der Konfiguration ist.

1. Erweitern Sie im linken Bereich den Wert **[!UICONTROL Sales]** und wählen Sie **[!UICONTROL Tax]** aus.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) im Abschnitt **[!UICONTROL Calculation Settings]** .

1. Setzen Sie **[!UICONTROL Catalog Prices]** auf `Including Tax`.

1. Um eine grenzüberschreitende Preiskonsistenz zu ermöglichen, setzen Sie **[!UICONTROL Enable Cross Border Trade]** auf `Yes`.

   ![Grenzüberschreitende Handelseinstellungen aktivieren](./assets/cross-border-calculations-settings.png){width="600" zoomable="yes"}

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save Config]**.
