---
title: Rückerstattungen im Dashboard des Kundenkontos
description: Store-Kunden können die mit der Bestellung verbundenen Rückerstattungsinformationen in ihrem Konto-Dashboard anzeigen.
exl-id: 8fd6d4e7-74ba-4f39-9a19-7c77ee63b913
feature: Customers, Storefront
TQID: https://experienceleague.adobe.com/ggaeec6NA2K12-eHl7ESC10nU2u11ihbaxaPlbNAE9I
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 485
ht-degree: 0%

---

# Rückerstattungen im Dashboard des Kundenkontos

{{ee-feature}}

Wenn eine Rückerstattung für eine Bestellung ausgestellt wurde, können Kunden die mit der Bestellung verbundenen Rückerstattungsinformationen in ihrem Konto-Dashboard anzeigen. Wenn Sie die Option [!UICONTROL _Shop-Kreditverlauf für Kunden anzeigen_] für [Store-](../customers/credit-configure.md) aktiviert haben, können Kunden auch auf ihren [Shop-](../customers/store-credit.md) zugreifen.

## Eine Rückerstattung auf der Storefront anzeigen

1. In der Storefront meldet sich der Kunde bei seinem Konto an.

1. Ermittelt die Reihenfolge mithilfe einer der folgenden Methoden:

   * Suchen der Bestellung in der Liste der **letzten Bestellungen** und Klicken auf **[!UICONTROL View]**.
   * Wählen Sie im linken Bedienfeld **[!UICONTROL My Orders]** aus. Suchen Sie dann die Reihenfolge in der Liste und klicken Sie auf **[!UICONTROL View]**.

1. Der Kunde klickt auf die Registerkarte **[!UICONTROL Refunds]** , um die Details der Rückerstattung anzuzeigen.

   ![Details zur Rückerstattung in der Storefront](assets/customer-account-order-refunds.png){width="700" zoomable="yes"}

## Anzeigen des Kontostands und des Verlaufs des Shops in der Storefront

Methode 1: **Vom Kundenkonto-Dashboard**

1. In der Storefront meldet sich der Kunde beim Konto an.

1. Wenn die Rückerstattung für das Speichern von Guthaben angewendet wurde, wählen Sie im linken Bedienfeld **[!UICONTROL Store Credit]** aus.

1. Der Betrag, der an das Store-Guthaben zurückerstattet wurde, wird in der Liste mit Datum und Uhrzeit der Aktion angezeigt.

   ![Rückerstatteter Betrag zur Speicherung des Guthabens](assets/customer-account-store-credit.png){width="700" zoomable="yes"}

   >[!INFO]
   >
   >Die Store-Kreditseite enthält auch einen Link für den Kunden zum Einlösen einer [Geschenkkarte](../stores-purchase/product-gift-card-workflow.md#check-status-and-balance-of-the-gift-card).

Methode 2: **Von der Seite _Überprüfung und Zahlungen_**

1. Der Kunde fügt dem Warenkorb ein Produkt hinzu.

2. Wechselt zur Seite _Checkout_.

3. Übergibt den **[!UICONTROL Shipping]** Schritt.

4. Wenn ein Warenkorb verfügbar ist, klickt der Kunde auf **[!UICONTROL Use Store Credit]**.

   ![Gutschrift auf der Seite Überprüfen und Zahlungen speichern](assets/customer-account-order-refund-from-checkout.png){width="700" zoomable="yes"}

5. Wenn der Kunde die Verwendung des Gutscheins im Geschäft anders überlegt, klickt auf **[!UICONTROL Remove]** im Abschnitt _Bestellzusammenfassung_.

## Zahlungsaktionen in der Admin-Instanz

Sie können Zahlungsaktionen für Ihre spezifische [Zahlungsmethode](../configuration-reference/sales/payment-methods.md) konfigurieren. Jede Zahlungsmethode verfügt über einen anderen Satz von Zahlungsaktionen.

| Zahlungsaktion | Beschreibung |
|--- |---|
| [!UICONTROL Capture Online] | Wenn die Rechnung eingereicht wird, erfasst das System die Zahlung vom Zahlungs-Gateway eines Drittanbieters. Ein Administrator kann dann eine Gutschrift erstellen und die Rechnung annullieren. |
| [!UICONTROL Capture Offline] | Wenn die Rechnung übermittelt wird, erfasst das System die Zahlung nicht. Es wird davon ausgegangen, dass die Zahlung direkt über das Gateway erfasst wird und nicht über Adobe Commerce erfasst werden kann. Ein Administrator kann dann eine Gutschrift erstellen, die Rechnung jedoch nicht annullieren. (Obwohl für die Bestellung eine Online-Zahlung verwendet wurde, handelt es sich bei der Rechnung im Wesentlichen um eine Offline-Rechnung.) |
| [!UICONTROL Not Capture] | Wenn die Rechnung übermittelt wird, erfasst das System die Zahlung nicht. Es wird davon ausgegangen, dass die Zahlung später über Adobe Commerce erfasst wird. In der [!UICONTROL _Rechnung befindet sich_] Schaltfläche „Erfassen“. Vor der Erfassung können Sie die Rechnung stornieren. Nach der Erfassung können Sie eine Gutschrift erstellen und die Rechnung stornieren. |

{style="table-layout:auto"}

>[!WARNING]
>
>Wählen Sie die [!UICONTROL _Nicht erfassen_], es sei denn, Sie sind sicher, dass Sie die Zahlung später über Adobe Commerce erfassen werden. Eine Gutschrift kann erst erstellt werden, nachdem die Zahlung mit der Schaltfläche &quot;[!UICONTROL _&quot; erfasst_].
