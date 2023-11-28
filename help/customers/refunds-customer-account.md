---
title: Erstattungen im Dashboard des Kundenkontos
description: Store-Kunden können die mit der Bestellung verbundenen Erstattungsinformationen in ihrem Konto-Dashboard anzeigen.
exl-id: 8fd6d4e7-74ba-4f39-9a19-7c77ee63b913
feature: Customers, Storefront
source-git-commit: 7de285d4cd1e25ec890f1efff9ea7bdf2f0a9144
workflow-type: tm+mt
source-wordcount: '482'
ht-degree: 0%

---

# Erstattungen im Dashboard des Kundenkontos

{{ee-feature}}

Wenn eine Rückerstattung für eine Bestellung erteilt wurde, können Kunden die mit der Bestellung verbundenen Rückerstattungsinformationen in ihrem Konto-Dashboard anzeigen. Wenn Sie die [!UICONTROL _Anzeigen des Store-Kreditverlaufs für Kunden_] -Option für [Konfiguration von Store-Guthaben](../customers/credit-configure.md), können Kunden auch auf ihre [Store-Guthaben](../customers/store-credit.md) Geschichte.

## Anzeigen einer Rückerstattung an die Storefront

1. Über die Storefront meldet sich der Kunde bei seinem Konto an.

1. Lokalisiert ihre Reihenfolge mit einer der folgenden Methoden:

   * Suchen der Bestellung in der Liste der **Letzte Bestellungen** und klicken **[!UICONTROL View]**.
   * Wählen Sie im linken Bereich **[!UICONTROL My Orders]**. Suchen Sie dann die Reihenfolge in der Liste und klicken Sie auf **[!UICONTROL View]**.

1. Der Kunde klickt auf **[!UICONTROL Refunds]** um die Details der Rückerstattung anzuzeigen.

   ![Erstattungsdetails in der Storefront](assets/customer-account-order-refunds.png){width="700" zoomable="yes"}

## Anzeigen des Kontostands und des Verlaufs des Storefront

Methode 1: **Über das Dashboard des Kundenkontos**

1. Über die Storefront meldet sich der Kunde bei seinem Konto an.

1. Wurde die Erstattung auf die Kreditspeicherung angewandt, so wird **[!UICONTROL Store Credit]** im linken Bereich.

1. Der Betrag, der dem Store-Guthaben zurückerstattet wurde, erscheint in der Liste mit Datum und Uhrzeit der Aktion.

   ![Erstattungsbetrag für die Kreditspeicherung](assets/customer-account-store-credit.png){width="700" zoomable="yes"}

   >[!INFO]
   >
   >Die Seite &quot;Store Credit&quot;enthält auch einen Link, über den der Kunde eine [Geschenkkarte](../stores-purchase/product-gift-card-workflow.md#check-status-and-balance-of-the-gift-card).

Methode 2: **Aus dem _Überprüfung und Zahlungen_ page**

1. Der Kunde fügt dem Warenkorb ein Produkt hinzu.

2. Fahren Sie mit dem _Checkout_ Seite.

3. Übergibt die **[!UICONTROL Shipping]** Schritt.

4. Wenn die Store-Gutschrift verfügbar ist, klickt der Kunde auf **[!UICONTROL Use Store Credit]**.

   ![Store-Gutschrift von der Seite &quot;Review &amp; Zahlungen&quot;](assets/customer-account-order-refund-from-checkout.png){width="700" zoomable="yes"}

5. Wenn der Kunde seine Meinung zur Verwendung des Store-Guthabens ändert, klickt **[!UICONTROL Remove]** im _Bestellübersicht_ Abschnitt.

## Zahlungsaktionen im Admin

Sie können Zahlungsaktionen für Ihre spezifischen [Zahlungsmethode](../configuration-reference/sales/payment-methods.md). Jede Zahlungsmethode verfügt über einen anderen Satz von Zahlungsaktionen.

| Zahlungsaktion | Beschreibung |
|--- |---|
| [!UICONTROL Capture Online] | Wenn die Rechnung übermittelt wird, erfasst das System die Zahlung vom Zahlungseingang des Drittanbieters. Ein Admin-Benutzer kann dann ein Kreditmemo erstellen und die Rechnung löschen. |
| [!UICONTROL Capture Offline] | Wenn die Rechnung übermittelt wird, erfasst das System die Zahlung nicht. Es wird davon ausgegangen, dass die Zahlung direkt über das Gateway erfasst wird und die Zahlung nicht über Adobe Commerce erfasst werden kann. Ein Admin-Benutzer kann dann ein Kreditmemo erstellen, die Rechnung jedoch nicht annullieren. (Obwohl die Bestellung eine Online-Zahlung verwendet hat, ist die Rechnung im Wesentlichen eine Offline-Rechnung.) |
| [!UICONTROL Not Capture] | Wenn die Rechnung übermittelt wird, erfasst das System die Zahlung nicht. Es wird davon ausgegangen, dass die Zahlung später über Adobe Commerce erfasst wird. Es gibt eine [!UICONTROL _Capture_] in der ausgefüllten Rechnung. Vor der Erfassung können Sie die Rechnung stornieren. Nach der Erfassung können Sie ein Kreditmemo erstellen und die Rechnung annullieren. |

{style="table-layout:auto"}

>[!WARNING]
>
>Wählen Sie die [!UICONTROL _Nicht erfassen_] , es sei denn, Sie sind sicher, dass Sie die Zahlung später über Adobe Commerce erfassen werden. Sie können ein Kreditmemo erst dann erstellen, wenn die Zahlung mithilfe der Variablen [!UICONTROL _Capture_] Schaltfläche.
