---
title: Checkout-Prozess und Optionen
description: Erfahren Sie, wie der Checkout-Prozess für Adobe Commerce und Magento Open Source die zum Abschluss der Transaktion erforderlichen Informationen erfasst und die Checkout-Seite den Kunden durch jeden Prozessschritt führt.
exl-id: f503643b-a0bb-4763-9831-d592afb2c323
feature: Checkout
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '1097'
ht-degree: 0%

---

# Checkout-Prozess und Optionen

Wenn der Checkout-Prozess beginnt, wechselt die Transaktion zu einem sicheren, verschlüsselten Kanal. In der Adressleiste des Browsers wird ein Vorhängeschloss-Symbol angezeigt und die URL ändert sich von `http` nach `https`.

## Prozess

Das Ziel des Checkout-Prozesses besteht darin, die für den Abschluss der Transaktion erforderlichen Informationen zu sammeln. Die _Checkout_ -Seite führt den Kunden durch jeden Schritt des Prozesses. Kunden, die bei ihren Konten angemeldet sind, können den Kassengang schnell abschließen, da ein Großteil der Informationen bereits in ihren Konten enthalten ist. Kunden, die mit einem Unternehmenskonto verknüpft sind, das Bestellungen verwendet, haben einen etwas anderen Arbeitsablauf.

### Versand

Der erste Schritt des Checkout-Prozesses besteht darin, dass der Kunde die Versandadressen-Informationen ausfüllt und die Versandmethode auswählt. Wenn der Kunde über ein Konto verfügt, wird die Lieferadresse automatisch angegeben, kann aber bei Bedarf geändert werden.

![Adobe Commerce](../assets/adobe-logo.svg) (Nur Adobe Commerce) Das Format der Straßenadresse für Empfänger und Absender wird durch die Eigenschaften der [Kundenadressenattribut](../customers/address-attributes.md). Die Einstellung für die Eingabevalidierung bestimmt die gültigen Zeichen, die in einer Versandadresse verwendet werden können.

Die Fortschrittsleiste am oberen Seitenrand folgt jedem Schritt des Checkout-Prozesses und die Bestellzusammenfassung zeigt an, dass die bisher eingegebenen Informationen eingegeben wurden.

![Versandseite während des Checkout-Prozesses](./assets/storefront-checkout-step1-shipping.png){width="600" zoomable="yes"}

#### An eine andere Adresse schicken

1. Wenn im Adressbuch zusätzliche Einträge enthalten sind, findet der Kunde die Adresse, an der die Bestellung versandt werden soll.

1. Klicken Sie zur Auswahl der Adresse auf **[!UICONTROL Ship Here]**.

#### Adresse hinzufügen

1. Am unteren Rand des _[!UICONTROL Shipping Address]_-Abschnitt, auf den der Kunde klickt **[!UICONTROL + New Address]**.

1. Schließt die _[!UICONTROL Shipping Address]_Formular.

   Standardmäßig wird der Vor- und Nachname des Kunden zunächst im Formular angezeigt.

   ![Formular für Lieferadresse einschließlich Name und Adressinformationen](./assets/storefront-checkout-step1-shipping-add-new-address.png){width="600" zoomable="yes"}

1. Um die neue Adresse im Adressbuch zu speichern, aktiviert der Kunde das Kontrollkästchen am unteren Rand des Formulars.

1. Klicks **[!UICONTROL Save Address]**.

   Die neue Adresse ist jetzt als Lieferadresse ausgewählt.

   ![Die gespeicherte Adresse wird automatisch auf der Versandseite ausgewählt](./assets/storefront-checkout-step1-shipping-new-address-selected.png){width="600" zoomable="yes"}

#### Versandmethode auswählen

1. In der Liste der [Versand](delivery.md) -Methoden verwenden, wählt der Kunde die gewünschte Option aus.

   ![Auf der Versandseite werden Optionen für Versandmethoden angezeigt](./assets/storefront-checkout-step1-shipping-methods.png){width="600" zoomable="yes"}

1. Klicks **[!UICONTROL Next]** , um fortzufahren.

### Überprüfung und Zahlungen - Regelmäßige Bestellung

Im zweiten Schritt des Checkout-Prozesses wählt der Kunde die [Zahlungsmethode](payments.md)und wendet alle Gutscheine mit Werbecodes auf den Kauf an. Alle Informationen können bei Bedarf überprüft und bearbeitet werden. Sofern aktiviert, muss der Kunde vor der Bestellung den Verkaufsbedingungen zustimmen.

>[!NOTE]
>
>Commerce ermöglicht zwar die Konfiguration mehrerer Couponcodes, kann jedoch nur einen Couponcode auf den Warenkorb anwenden. (Siehe [Coupon-Codes](../merchandising-promotions/price-rules-cart-coupon.md) für weitere Informationen.)

![Überprüfungs- und Zahlungsseite während des Checkouts](./assets/storefront-checkout-step2-payment-review.png){width="700" zoomable="yes"}

### Überprüfung und Zahlungen - Bestellung

![Adobe Commerce B2B](../assets/b2b.svg) (Nur bei Adobe Commerce B2B verfügbar)

Wenn ein Kunde mit einem Unternehmen verknüpft ist, das [Bestellaufträge](../b2b/purchase-order-flow.md), werden alle Bestellungen als Bestellungen verarbeitet. Die verfügbaren Zahlungsmethoden werden durch die Kontoeinstellungen des Unternehmens bestimmt.

1. Der Kunde wählt eine Zahlungsmethode aus.

   Bei Verwendung von _Kontozahlung_ -Methode, [!UICONTROL Custom Reference Number] kann verwendet werden, um auf eine Rechnungsnummer zu verweisen.

1. Der Kunde klickt auf **[!UICONTROL Place Purchase Order]**.

   Die Bestellung wird aufgegeben.

Wenn das Unternehmen [Validierungsregeln](../b2b/account-dashboard-approval-rules.md), durchläuft die Bestellung den Genehmigungsprozess. Andernfalls wird sie sofort verarbeitet.

![Überprüfung und Zahlung des Kaufauftrags](./assets/checkout-storefront-step2-b2b.png){width="700" zoomable="yes"}

### Anzahl der in der Bestellübersicht angezeigten Elemente

Admin-Benutzer können die maximale Anzahl von Elementen ändern, die in der Bestellübersicht beim Checkout angezeigt werden, um die Anzeige mit weniger Produkten zu optimieren. Standardmäßig ist dieser Wert auf 10 gesetzt.

![Anzahl der in der Bestellübersicht angezeigten Elemente](./assets/order-summary.png){width="700" zoomable="yes"}

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Sales]** und wählen **[!UICONTROL Checkout]**.

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL Checkout Options]** Abschnitt.

1. Für **[!UICONTROL Maximum Number of Items to Display in Order Summary]**, geben Sie die maximale Anzahl der anzuzeigenden Elemente an.

1. Klicks **[!UICONTROL Save Config]**.

   Mit diesem Update ist die beim Checkout angezeigte Bestellübersicht auf die angegebene Anzahl von Elementen beschränkt.

### Bestellbestätigung

Die Bestellbestätigung wird angezeigt, nachdem die Bestellung aufgegeben wurde. Für registrierte Kunden enthält die Seite die Bestellnummer mit einem Link zum Kundenkonto und einen Link zur Generierung einer Quittung. Registrierte Kunden werden angewiesen, Auftragsbestätigungs- und Trackinginformationen per E-Mail zu erwarten. Es wird empfohlen, ein Konto zu erstellen, um die Bestellung zu verfolgen. Registrierte Kunden können eine Quittung durch Klicken auf einen Link generieren.

Die Bestellbestätigungsseite wird auch als _Erfolg_ und wird von Analyseprogrammen verwendet, um Konversionen zu verfolgen.

![Auf der Seite Auftragsbestätigung wird eine Erfolgsmeldung und eine Bestellnummer angezeigt.](./assets/storefront-checkout-confirmation-customer.png){width="700" zoomable="yes"}

## Optionen zum Auschecken

Die Checkout-Optionen steuern verschiedene Attribute für die Checkout-Seite, einschließlich des Layouts. Es gibt Optionen, die Sie konfigurieren können, um Beschränkungen für das Auschecken einzuführen, darunter das Zulassen des Auscheckens für Gäste und das Erzwingen einer Vereinbarung über Geschäftsbedingungen. Es gibt auch Optionen zum Steuern der Anzeige von Informationen während des Checkout-Prozesses.

![Konfiguration - Checkout-Optionen](./assets/checkout-checkout-options.png){width="700" zoomable="yes"}

Eine ausführliche Beschreibung der einzelnen Konfigurationseinstellungen finden Sie unter [Checkout-Optionen](../configuration-reference/sales/checkout.md#checkout-options) im _Konfigurationshandbuch_.

### Checkout-Optionen ändern

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.
1. Erweitern Sie im linken Bereich **[!UICONTROL Sales]** und wählen **[!UICONTROL Checkout]**.
1. Legen Sie die folgenden erforderlichen Optionen fest.
1. Klicks **[!UICONTROL Save Config]**.

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL Checkout Options]** Abschnitt.

1. Wenn die Einstellungen für eine bestimmte Store-Ansicht gelten, [Auswählen der Store-Ansicht](../configuration-reference/scope-change.md#set-the-scope) wo die Konfiguration gilt.

   Klicken Sie bei Aufforderung auf **[!UICONTROL OK]** , um fortzufahren.

1. Legen Sie die Checkout-Optionen fest.

1. Klicks **[!UICONTROL Save Config]**.

### Verfügbare Checkout-Optionen

| Feld | [Anwendungsbereich](../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Enable Onepage Checkout] | Store-Ansicht | Bestimmt, ob [einseitige Kasse](checkout-one-page.md) ist das standardmäßige Checkout-Format. Optionen: Ja/Nein |
| [!UICONTROL Allow Guest Checkout] | Store-Ansicht | Bestimmt, ob Gäste durchgehen können [Checkout ohne Registrierung](checkout-guest.md) für ein Konto bei Ihrem Geschäft. Optionen: `Yes` / `No` |
| [!UICONTROL Enable Terms and Conditions] | Store-Ansicht | Bestimmt, ob Kunden dem [Geschäftsbedingungen](terms-and-conditions.md) des Verkaufs vor dem Kauf. Optionen: `Yes` / `No` |
| [!UICONTROL Display Billing Address On] | Store-Ansicht | Bestimmt den Speicherort der Rechnungsadresse während des Checkouts. Optionen: `Payment Method` / `Payment Page` |
| [!UICONTROL Maximum Number of Items to Display in Order Summary] | Store-Ansicht | Bestimmt die maximale Anzahl von Elementen, die während des Auscheckens in der Bestellübersicht angezeigt werden können. Der Standardwert ist `10`. |
| [!UICONTROL Enable Address Search] | Webseite | ![Adobe Commerce](../assets/adobe-logo.svg) (Nur Adobe Commerce) Stellt fest, ob Kunden [Adresssuche](checkout-address-search.md) Funktionalität für _Versand_ und die _Überprüfung und Zahlungen_ Schritte. Wenn diese Funktion aktiviert ist, verwenden Sie die _[!UICONTROL Number of Customer Addresses Limit]_, um die Anzahl der gespeicherten Adressen festzulegen, die zum Aktivieren dieser Funktion während des Auscheckens erforderlich sind. Optionen: `Yes` / `No` |
| [!UICONTROL Number of Customer Addresses Limit] | Webseite | ![Adobe Commerce](../assets/adobe-logo.svg) (Nur Adobe Commerce) Wenn die Adresssuche **[!UICONTROL Enabled]** bestimmt die Anzahl der gespeicherten Adressen, die zum Aktivieren dieser Funktion während des Checkout erforderlich sind. Wenn die Anzahl der gespeicherten Adressen des Kunden diese Zahl erreicht oder überschreitet, wird nur die Standardadresse auf der Seite _Versand_ und _Überprüfung und Zahlungen_ Schritte. Der Kunde kann eine Suchfunktion verwenden, um die ausgewählte Adresse zu ändern. Der Standardwert ist 10. |

{style="table-layout:auto"}
