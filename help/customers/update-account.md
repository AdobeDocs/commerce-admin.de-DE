---
title: Kundenprofil aktualisieren
description: Greifen Sie auf Informationen zu Kundenaktivitäten zu, z. B. wann der Kunde sich zuletzt bei seinem Konto angemeldet oder das Konto verlassen hat, und aktualisieren Sie das Kundenprofil.
exl-id: 8e805095-76b2-4237-98dc-aa32f15f2637
source-git-commit: c855a691ed33e1e6e74865ebdfb30ddad21ad83e
workflow-type: tm+mt
source-wordcount: '505'
ht-degree: 0%

---

# Kundenprofil aktualisieren

Das linke Bedienfeld der Seite &quot;_[!UICONTROL Customer Information]_&quot; enthält Informationen zu Kundenaktivitäten, Adressen, Bestellstatistiken, aktuellen Bestellungen, Warenkorbinhalten, Produktbewertungen und Newsletter-Abonnements.

![Kundenprofil](assets/cust-profile.png){width="700" zoomable="yes"}

## Kundenkonto bearbeiten

Methode 1: **_Schnellbearbeitung_**

1. Aktivieren Sie in der ersten Spalte das Kontrollkästchen des zu bearbeitenden Kundenkontos.

1. Setzen Sie die Spalte **[!UICONTROL Actions]** auf `Edit`.

   >[!INFO]
   >
   >Der Wert jedes Werts, der aktualisiert werden kann, wird in einem Textfeld angezeigt. Nur einige Werte des ausgewählten Kundendatensatzes können aus dem Raster bearbeitet werden.

   ![Quick Edit](assets/customers-grid-quick-edit.png){width="700" zoomable="yes"}

1. Aktualisieren Sie nach Bedarf einen der folgenden Werte:

   * **[!UICONTROL Email]**
   * **[!UICONTROL Web Site]**
   * **[!UICONTROL Tax/VAT Number]**
   * **[!UICONTROL Gender]**

1. Klicken Sie auf **[!UICONTROL Save]**.

Methode 2: **_Vollständige Bearbeitung_**

1. Suchen Sie im Raster den zu bearbeitenden Kundendatensatz.

1. Klicken Sie in der Spalte _Aktionen_ ganz rechts auf **[!UICONTROL Edit]**.

1. Nehmen Sie die erforderlichen Änderungen an den Unternehmensinformationen vor.

   >[!INFO]
   >
   >Weitere Informationen finden Sie unter [Aktualisieren eines Kundenprofils](../customers/update-account.md).

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save Customer]**.

>[!INFO]
>
>Wenn Sie alle Änderungen vor dem Speichern rückgängig machen möchten, klicken Sie in der oberen Schaltflächenleiste auf **[!UICONTROL Reset]** , um alle Änderungen zur zuletzt gespeicherten Version zurückzugeben.

## Kundeninformationen

### [!UICONTROL Customer View]

Die Registerkarte _Kundenansicht_ enthält Informationen zum Kunden, einschließlich **[!UICONTROL Personal Information]**, **[!UICONTROL Reward Points Balance]** und **[!UICONTROL Store Credit Balance]**.

### [!UICONTROL Account Information]

Die Registerkarte [Kontoinformationen](../customers/account-dashboard-account-information.md) enthält detaillierte Informationen zum Kunden, in denen ein Admin-Benutzer persönliche Informationen, E-Mails, Remote-Kaufunterstützung, Geburtsdatum und Kunden an die Website oder das Unternehmen anhängen kann.

### [!UICONTROL Addresses]

Der Tab [Adressen](../customers/account-dashboard-address-book.md) enthält die standardmäßigen Abrechnungs- und Versandadressen des Kunden sowie alle weiteren häufig verwendeten Adressen.

### [!UICONTROL Orders]

Das Raster [Bestellungen](../stores-purchase/orders.md) enthält eine Liste aller aktuellen Kundenaufträge. Der Administrator kann den Fortschritt verfolgen.

### [!UICONTROL Returns]

{{ee-feature}}

Auf der Registerkarte [Rückgaben](../stores-purchase/returns.md) werden die aktuellen zurückgegebenen Kundenanforderungen aufgelistet.

### [!UICONTROL Shopping cart]

Auf der Registerkarte [Warenkorb](../stores-purchase/cart.md) werden Produkte angezeigt, die sich derzeit im Warenkorb befinden, aber aus irgendeinem Grund wurde der Kauf nicht abgeschlossen.

### [!UICONTROL Wish List]

Eine [Wunschliste](../stores-purchase/wishlists.md) zeigt eine Liste der Produkte an, die ein Kunde später in den Warenkorb übertragen kann.

### [!UICONTROL Gift Registry]

{{ee-feature}}

Im Abschnitt [Geschenkregistrierung](../merchandising-promotions/gift-registry-storefront.md) werden die aktuellen Geschenkgutachter des Kunden und das zugehörige Ereignis aufgelistet.


### [!UICONTROL Store Credit]

{{ee-feature}}

Auf der Registerkarte [Gutschrift speichern](../customers/store-credit.md) wird ein Betrag angezeigt, der in ein Kundenkonto wiederhergestellt wurde. Der Administrator kann diesen Wert verwalten.

### [!UICONTROL Newsletter]

Auf der Registerkarte [Newsletter](../merchandising-promotions/newsletters.md) werden alle E-Mails angezeigt, die an den aktuellen Kunden gesendet werden.

### [!UICONTROL Billing Agreements]

Im Tab [Abrechnungsabkommen](../stores-purchase/paypal-billing-agreements.md) werden alle PayPal-Abrechnungsvereinbarungen zwischen dem Store und dem Kunden aufgelistet.

### [!UICONTROL Product Reviews]

Auf der Registerkarte [Produktüberprüfungen](../catalog/settings-advanced-product-reviews.md) werden alle von diesem Kunden gesendeten Bewertungen angezeigt.

### [!UICONTROL Reward Points]

{{ee-feature}}

Der Abschnitt [Bonuspunkte](../merchandising-promotions/rewards-loyalty.md) zeigt den aktuellen Saldo der Belohnungspunkte des Kunden an. Ein Admin-Benutzer kann diesen Wert verwalten.

## Schaltflächenleiste

| Schaltfläche | Beschreibung |
|----------|--------------|
| **[!UICONTROL Back]** | Kehrt zur Kundenseite zurück, ohne Änderungen zu speichern. |
| **[!UICONTROL Login as Customer]** | Ermöglicht dem Händler, sich als Kunde anzumelden. |
| **[!UICONTROL Delete Customer]** | Löscht das Kundenkonto. |
| **[!UICONTROL Reset]** | Setzt nicht gespeicherte Änderungen im Kundenformular auf die vorherigen Werte zurück. |
| **[!UICONTROL Create Order]** | [Erstellt eine Bestellung](../stores-purchase/customer-account-create-order.md), die mit dem Kundenkonto verknüpft ist. |
| **[!UICONTROL Reset Password]** | Setzt das Kennwort des Kunden zurück. |
| **[!UICONTROL Force Sign-In]** | Löscht die mit dem Kennwort des Kunden verknüpften Token und gewährt dem Administrator Zugriff auf das Konto. |
| **[!UICONTROL Manage Shopping Cart]** | Bietet Zugriff auf den Warenkorb eines Kunden. |
| **[!UICONTROL Save and Continue Edit]** | Speichert Änderungen und hält das Kundenkonto offen. |
| **[!UICONTROL Save Customer]** | Speichert Änderungen und schließt das Kundenkonto. |

{style="table-layout:auto"}
