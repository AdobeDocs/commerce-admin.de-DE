---
title: Sofortiger Kauf
description: Erfahren Sie mehr über den sofortigen Kauf und wie er einen schnellen Checkout für registrierte Kundenkonten bieten kann.
exl-id: f299f364-d7e3-4567-8c7b-955129011a19
feature: Checkout
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '396'
ht-degree: 0%

---

# Sofortiger Kauf

Mit _Sofortiger Kauf_ können Kunden den Checkout-Prozess mithilfe von Informationen, die in ihrem Konto gespeichert sind, beschleunigen. Wenn diese Option aktiviert ist, wird die Schaltfläche _Sofortiger Kauf_ auf der Produktseite unter der Schaltfläche _Zum Warenkorb hinzufügen_ für Kunden angezeigt, die die Anforderungen erfüllen.

![Produktseite mit der Option &quot;Sofortiger Kauf&quot;angezeigt](./assets/storefront-checkout-instant-purchase.png){width="700" zoomable="yes"}

## Kundenanforderungen

- Der Kunde ist [in ](../customers/customer-sign-in.md) für sein Konto angemeldet.

- Das Kundenkonto verfügt über eine standardmäßige Abrechnungs- und Lieferadresse ](../customers/account-dashboard-address-book.md).[

- Mindestens eine [Versandmethode](delivery.md) ist für das Land verfügbar, das in der standardmäßigen Versandadresse angegeben ist.

- Das Kundenkonto verfügt über eine [gespeicherte Zahlung](../stores-purchase/stored-payment-methods.md) -Methode mit aktiviertem Vault.

  Die folgenden Zahlungsmethoden bieten sicheren Zugriff auf gespeicherte Kreditkarteninformationen:

   - [Braintree-Kreditkarten](braintree.md) (Der sofortige Kauf kann nicht mit Braintree-Kreditkarten verwendet werden, wenn die Option 3D Secure aktiviert ist.)
   - [Braintree mit PayPal aktiviert](braintree.md)
   - [PayPal Payflow Pro](paypal-payflow-pro.md)

## Sofortiger Kauf auf der Storefront

1. Auf der Storefront ruft der Kunde die Produktseite des zu kaufenden Artikels auf.

1. Wählt die erforderlichen Optionen aus und klickt auf **[!UICONTROL Instant Purchase]**.

   ![Bestätigungsdialogfeld zur Bestätigung des sofortigen Kaufs](./assets/storefront-checkout-instant-purchase-confirmation.png){width="500" zoomable="yes"}

1. Überprüfen Sie die **[!UICONTROL Instant Purchase Confirmation]** -Informationen und klicken Sie auf **[!UICONTROL OK]** , um die Transaktion abzuschließen.

   Oben auf der Produktseite werden eine Bestätigungsmeldung und eine Bestellnummer angezeigt.

## Sofortiger Kauf konfigurieren

### Schritt 1: Öffnen Sie die Konfigurationsseite

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

### Schritt 2: Zahlungsmethode konfigurieren

Sie können Instant Purchase mit Braintree oder Payment Services für Adobe Commerce und Magento Open Source verwenden. Die Funktion &quot;Vaulting&quot;muss aktiviert sein, bevor ein Käufer die Funktion &quot;Instant Purchase&quot;verwenden kann.

Erfahren Sie, wie Sie die Zahlungsmethode konfigurieren und die Überprüfung für Braintree- oder Zahlungsdienste aktivieren:

- [Braintree](braintree.md)
- [Dokumentation zu Zahlungsdiensten](https://experienceleague.adobe.com/docs/commerce-merchant-services/payment-services/guide-overview.html)

### Schritt 3: Sofortigen Kauf aktivieren

1. Wählen Sie im linken Bereich unter dem Abschnitt _[!UICONTROL Sales]_die Option **[!UICONTROL Sales]**.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) im Abschnitt **[!UICONTROL Instant Purchase]** .

1. Wenn diese Änderung für eine bestimmte Store-Ansicht gilt, wählen Sie [die Store-Ansicht](../configuration-reference/scope-change.md#set-the-scope), für die die Konfiguration gilt.

   Klicken Sie nach Aufforderung auf **[!UICONTROL OK]** , um fortzufahren.

1. Setzen Sie **[!UICONTROL Enabled]** auf `Yes`.

1. Geben Sie den **[!UICONTROL Button Text]** ein, der auf der Schaltfläche angezeigt werden soll.

   Der Schaltflächentext kann für jede Store-Ansicht oder Sprache geändert werden. Standardmäßig lautet der Schaltflächentext `Instant Purchase`.

   ![Konfiguration - sofortige Kaufoptionen](../configuration-reference/sales/assets/sales-instant-purchase.png){width="600" zoomable="yes"}

   Eine ausführliche Beschreibung der einzelnen Konfigurationseinstellungen finden Sie unter [Sofortiger Kauf](../configuration-reference/sales/sales.md#instant-purchase) im _Konfigurationshandbuch_.

1. Klicken Sie auf **[!UICONTROL Save Config]**.

1. Wenn Sie aufgefordert werden, den Cache zu aktualisieren, klicken Sie in der Systemmeldung auf **[!UICONTROL Cache Management]** und befolgen Sie die Anweisungen zum Leeren des Caches.
