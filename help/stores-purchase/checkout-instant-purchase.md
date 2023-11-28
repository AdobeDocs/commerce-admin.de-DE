---
title: Sofortiger Kauf
description: Erfahren Sie mehr über den sofortigen Kauf und wie er einen schnellen Checkout für registrierte Kundenkonten bieten kann.
exl-id: f299f364-d7e3-4567-8c7b-955129011a19
feature: Checkout
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '398'
ht-degree: 0%

---

# Sofortiger Kauf

_Sofortiger Kauf_ ermöglicht es Kunden, den Checkout-Prozess mit in ihrem Konto gespeicherten Informationen zu beschleunigen. Wenn diese Option aktiviert ist, wird die _Sofortiger Kauf_ -Schaltfläche wird unter der _Zum Warenkorb hinzufügen_ auf der Produktseite für Kunden, die die Anforderungen erfüllen.

![Produktseite mit angezeigter Option &quot;Sofortiger Kauf&quot;](./assets/storefront-checkout-instant-purchase.png){width="700" zoomable="yes"}

## Kundenanforderungen

- Der Kunde ist [angemeldet](../customers/customer-sign-in.md) auf ihr Konto.

- Kundenkonto verfügt über eine [standardmäßige Abrechnungs- und Lieferadresse](../customers/account-dashboard-address-book.md).

- Mindestens ein [Versandmethode](delivery.md) ist für das Land verfügbar, das in der Standard-Versandadresse angegeben ist.

- Kundenkonto verfügt über eine [gespeicherte Zahlung](../stores-purchase/stored-payment-methods.md) -Methode mit aktiviertem Vault.

  Die folgenden Zahlungsmethoden bieten sicheren Zugriff auf gespeicherte Kreditkarteninformationen:

   - [Braintree-Kreditkarten](braintree.md) (Der Sofortkauf kann nicht mit Braintree-Kreditkarten verwendet werden, wenn 3D Secure aktiviert ist.)
   - [Braintree mit PayPal aktiviert](braintree.md)
   - [PayPal Payflow Pro](paypal-payflow-pro.md)

## Sofortiger Kauf auf der Storefront

1. Auf der Storefront ruft der Kunde die Produktseite des zu kaufenden Artikels auf.

1. Auswahl der erforderlichen Optionen und Klicks **[!UICONTROL Instant Purchase]**.

   ![Bestätigungsdialogfeld zur Bestätigung des sofortigen Kaufs](./assets/storefront-checkout-instant-purchase-confirmation.png){width="500" zoomable="yes"}

1. Überprüft die **[!UICONTROL Instant Purchase Confirmation]** Informationen und Klicks **[!UICONTROL OK]** , um die Transaktion abzuschließen.

   Oben auf der Produktseite werden eine Bestätigungsmeldung und eine Bestellnummer angezeigt.

## Sofortiger Kauf konfigurieren

### Schritt 1: Öffnen Sie die Konfigurationsseite

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

### Schritt 2: Zahlungsmethode konfigurieren

Sie können Instant Purchase mit Braintree oder Payment Services für Adobe Commerce und Magento Open Source verwenden. Die Funktion &quot;Vaulting&quot;muss aktiviert sein, bevor ein Käufer die Funktion &quot;Instant Purchase&quot;verwenden kann.

Erfahren Sie, wie Sie die Zahlungsmethode konfigurieren und die Überprüfung für Braintree- oder Zahlungsdienste aktivieren:

- [Braintree](braintree.md)
- [Dokumentation zu Zahlungsdiensten](https://experienceleague.adobe.com/docs/commerce-merchant-services/payment-services/guide-overview.html)

### Schritt 3: Sofortigen Kauf aktivieren

1. Im linken Bereich unter dem _[!UICONTROL Sales]_auswählen **[!UICONTROL Sales]**.

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL Instant Purchase]** Abschnitt.

1. Wenn diese Änderung für eine bestimmte Store-Ansicht gilt, [Auswählen der Store-Ansicht](../configuration-reference/scope-change.md#set-the-scope) wo die Konfiguration gilt.

   Klicken Sie bei Aufforderung auf **[!UICONTROL OK]** , um fortzufahren.

1. Satz **[!UICONTROL Enabled]** nach `Yes`.

1. Geben Sie die **[!UICONTROL Button Text]** die auf der Schaltfläche angezeigt werden sollen.

   Der Schaltflächentext kann für jede Store-Ansicht oder Sprache geändert werden. Standardmäßig lautet der Schaltflächentext `Instant Purchase`.

   ![Konfiguration - Optionen zum sofortigen Kauf](../configuration-reference/sales/assets/sales-instant-purchase.png){width="600" zoomable="yes"}

   Eine ausführliche Beschreibung der einzelnen Konfigurationseinstellungen finden Sie unter [Sofortiger Kauf](../configuration-reference/sales/sales.md#instant-purchase) im _Konfigurationshandbuch_.

1. Klicken **[!UICONTROL Save Config]**.

1. Wenn Sie aufgefordert werden, den Cache zu aktualisieren, klicken Sie auf **[!UICONTROL Cache Management]** in der Systemmeldung und befolgen Sie die Anweisungen zum Leeren des Caches.
