---
title: Kundenprofil aktualisieren
description: Greifen Sie auf Informationen zu Kundenaktivitäten zu, z. B. wann der Kunde sich zuletzt bei seinem Konto angemeldet oder das Konto verlassen hat, und aktualisieren Sie das Kundenprofil.
exl-id: 8e805095-76b2-4237-98dc-aa32f15f2637
source-git-commit: c855a691ed33e1e6e74865ebdfb30ddad21ad83e
workflow-type: tm+mt
source-wordcount: '503'
ht-degree: 0%

---

# Kundenprofil aktualisieren

Das linke Bedienfeld der _[!UICONTROL Customer Information]_enthält Informationen zu Kundenaktivität, Adressen, Bestellstatistiken, aktuellen Bestellungen, Warenkorbinhalten, Produktbewertungen und Newsletter-Abonnements.

![Kundenprofil](assets/cust-profile.png){width="700" zoomable="yes"}

## Kundenkonto bearbeiten

Methode 1: **_Schnellbearbeitung_**

1. Aktivieren Sie in der ersten Spalte das Kontrollkästchen des zu bearbeitenden Kundenkontos.

1. Legen Sie die **[!UICONTROL Actions]** Spalte zu `Edit`.

   >[!INFO]
   >
   >Der Wert jedes Werts, der aktualisiert werden kann, wird in einem Textfeld angezeigt. Nur einige Werte des ausgewählten Kundendatensatzes können aus dem Raster bearbeitet werden.

   ![Schnellbearbeitung](assets/customers-grid-quick-edit.png){width="700" zoomable="yes"}

1. Aktualisieren Sie nach Bedarf einen der folgenden Werte:

   * **[!UICONTROL Email]**
   * **[!UICONTROL Web Site]**
   * **[!UICONTROL Tax/VAT Number]**
   * **[!UICONTROL Gender]**

1. Klicken **[!UICONTROL Save]**.

Methode 2: **_Vollständige Bearbeitung_**

1. Suchen Sie im Raster den zu bearbeitenden Kundendatensatz.

1. Im _Aktionen_ -Spalte ganz rechts klicken Sie auf **[!UICONTROL Edit]**.

1. Nehmen Sie die erforderlichen Änderungen an den Unternehmensinformationen vor.

   >[!INFO]
   >
   >Weitere Informationen finden Sie unter [Kundenprofil aktualisieren](../customers/update-account.md).

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save Customer]**.

>[!INFO]
>
>Wenn Sie alle Änderungen vor dem Speichern rückgängig machen möchten, klicken Sie auf **[!UICONTROL Reset]** in der oberen Schaltflächenleiste, um alle Änderungen zur zuletzt gespeicherten Version zurückzugeben.

## Kundeninformationen

### [!UICONTROL Customer View]

Die _Kundenansicht_ enthält Informationen zum Kunden, einschließlich **[!UICONTROL Personal Information]**, **[!UICONTROL Reward Points Balance]**, und **[!UICONTROL Store Credit Balance]**.

### [!UICONTROL Account Information]

Die [Kontoinformationen](../customers/account-dashboard-account-information.md) -Tab enthält detaillierte Informationen zum Kunden, in denen ein Admin-Benutzer personenbezogene Daten, E-Mails, Remote-Einkaufsunterstützung, Geburtsdatum bearbeiten und Kunden an die Website oder das Unternehmen anhängen kann.

### [!UICONTROL Addresses]

Die [Adressen](../customers/account-dashboard-address-book.md) enthält die standardmäßigen Abrechnungs- und Versandadressen des Kunden sowie alle zusätzlichen häufig verwendeten Adressen.

### [!UICONTROL Orders]

Die [Bestellungen](../stores-purchase/orders.md) enthält eine Liste aller aktuellen Kundenaufträge. Der Administrator kann den Fortschritt verfolgen.

### [!UICONTROL Returns]

{{ee-feature}}

Die [Rückgabe](../stores-purchase/returns.md) -Tab listet die aktuellen zurückgegebenen Kundenanfragen auf.

### [!UICONTROL Shopping cart]

Die [Warenkorb](../stores-purchase/cart.md) -Tab zeigt Produkte an, die sich derzeit im Warenkorb befinden, aber aus irgendeinem Grund wurde der Kauf nicht abgeschlossen.

### [!UICONTROL Wish List]

A [Wunschliste](../stores-purchase/wishlists.md) zeigt eine Liste der Produkte an, die ein Kunde zu einem späteren Zeitpunkt in den Warenkorb übertragen kann.

### [!UICONTROL Gift Registry]

{{ee-feature}}

Die [Geschenkregistrierung](../merchandising-promotions/gift-registry-storefront.md) enthält die aktuellen Geschenkgutscheine des Kunden und das zugehörige Ereignis.


### [!UICONTROL Store Credit]

{{ee-feature}}

Die [Store-Gutschrift](../customers/store-credit.md) einen Betrag anzeigt, der in einem Kundenkonto wiederhergestellt wurde, kann der Administrator diesen Wert verwalten.

### [!UICONTROL Newsletter]

Die [Newsletter](../merchandising-promotions/newsletters.md) zeigt alle E-Mails an, die an den aktuellen Kunden gesendet wurden.

### [!UICONTROL Billing Agreements]

Die [Abrechnungsabkommen](../stores-purchase/paypal-billing-agreements.md) auf der Registerkarte werden alle PayPal-Abrechnungsvereinbarungen zwischen dem Store und dem Kunden aufgelistet.

### [!UICONTROL Product Reviews]

Die [Produktüberprüfungen](../catalog/settings-advanced-product-reviews.md) zeigt alle von diesem Kunden übermittelten Bewertungen an.

### [!UICONTROL Reward Points]

{{ee-feature}}

Die [Prämienpunkte](../merchandising-promotions/rewards-loyalty.md) zeigt den aktuellen Saldo der Belohnungspunkte des Kunden an. Ein Admin-Benutzer kann diesen Wert verwalten.

## Schaltflächenleiste

| Schaltfläche | Beschreibung |
|----------|--------------|
| **[!UICONTROL Back]** | Kehrt zur Kundenseite zurück, ohne Änderungen zu speichern. |
| **[!UICONTROL Login as Customer]** | Ermöglicht dem Händler, sich als Kunde anzumelden. |
| **[!UICONTROL Delete Customer]** | Löscht das Kundenkonto. |
| **[!UICONTROL Reset]** | Setzt nicht gespeicherte Änderungen im Kundenformular auf die vorherigen Werte zurück. |
| **[!UICONTROL Create Order]** | [Erstellt eine Bestellung](../stores-purchase/customer-account-create-order.md) , das mit dem Kundenkonto verknüpft ist. |
| **[!UICONTROL Reset Password]** | Setzt das Kennwort des Kunden zurück. |
| **[!UICONTROL Force Sign-In]** | Löscht die mit dem Kennwort des Kunden verknüpften Token und gewährt dem Administrator Zugriff auf das Konto. |
| **[!UICONTROL Manage Shopping Cart]** | Bietet Zugriff auf den Warenkorb eines Kunden. |
| **[!UICONTROL Save and Continue Edit]** | Speichert Änderungen und hält das Kundenkonto offen. |
| **[!UICONTROL Save Customer]** | Speichert Änderungen und schließt das Kundenkonto. |

{style="table-layout:auto"}
