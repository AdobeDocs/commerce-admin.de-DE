---
title: Preisregeln für Warenkorb
description: Erfahren Sie mehr über die Preisregeln für Warenkorb, die Rabatte auf Artikel im Warenkorb auf der Grundlage einer Reihe von Bedingungen anwenden.
exl-id: f3038f2a-9d34-4696-a39e-f87fbb1294a2
feature: Merchandising, Price Rules, Shopping Cart
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '448'
ht-degree: 0%

---

# Preisregeln für Warenkorb

Preisregeln für Warenkorb gelten für Artikel im Warenkorb, die auf einer Reihe von Bedingungen basieren. Der Rabatt kann automatisch angewendet werden, wenn die Bedingungen erfüllt sind oder wenn der Kunde einen gültigen Gutscheincode eingibt. Wenn der Rabatt angewendet wird, wird er im Warenkorb unter der Zwischensumme angezeigt. Eine Warenkorbpreisregel kann bei Bedarf für eine Saison oder eine Promotion verwendet werden, indem ihr Status und ihr Datumsbereich geändert werden.

>[!NOTE]
>
>Wenn die Coupon-Warenkorbregel Bedingungen enthält, die Checkout-Optionen festlegen, wie bestimmte Versand- oder Zahlungsmethoden, werden die Bedingungen erst beim Checkout erfüllt, nachdem die spezifischen Versand-/Zahlungsmethoden ausgewählt wurden. In diesem Fall kann der Gutschein beim Checkout im letzten Schritt angewendet werden.

![Beispiel-Storefront - Coupon auf den Warenkorb anwenden](./assets/storefront-cart-apply-coupon.png){width="600" zoomable="yes"}

## Preisregeln für den Warenkorb

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_>**[!UICONTROL Cart Price Rules]**.

   ![Preisregel für Warenkorb](./assets/price-rule-cart.png){width="700" zoomable="yes"}

1. Wenn Sie viele Regeln haben, verwenden Sie die Filteroptionen oben in jeder Spalte, um die Liste zu optimieren, und klicken Sie auf **[!UICONTROL Search]** , um die Filter anzuwenden.

1. Um alle Filteroptionen zu löschen und die vollständige Liste anzuzeigen, klicken Sie auf **[!UICONTROL Reset Filter]**.

1. Eigenschaften für eine Regel aktualisieren:

   - ![Adobe Commerce](../assets/adobe-logo.svg) (nur Adobe Commerce) Klicken Sie auf **[!UICONTROL Edit]** , um die Seite &quot;Regelinformationen&quot;anzuzeigen.

   - ![Magento Open Source](../assets/open-source.svg) (nur Magento Open Source) Klicken Sie auf die Regel in der Liste, um die Seite Regelinformationen anzuzeigen.

   Dort können Sie die Einstellungen für die Regel ändern (ähnlich wie beim Erstellen einer Regel).

## Filteroptionen nach Spalte

| Spalte | Beschreibung |
|--- |--- |
| [!UICONTROL ID] | Geben Sie Text ein, um die Liste nach einer bestimmten Regel-ID-Nummer zu filtern. |
| [!UICONTROL Rule] | Geben Sie Text ein, um die Liste anhand des bei der Regelerstellung definierten Regelnamens zu filtern. |
| [!UICONTROL Coupon Code] | Geben Sie Text ein, um die Liste anhand des bei der Erstellung der Regel definierten Codenamens zu filtern. |
| [!UICONTROL Priority] | Freitextfeld, das die Liste basierend auf der für eine Regel definierten Priorität filtert. |
| [!UICONTROL Status] | Verwenden Sie diese Option, um die Liste nach Regelstatus (`Active` oder `Inactive`) zu filtern. |
| [!UICONTROL Web Site] | Verwenden Sie diese Option, um die Liste auf der Grundlage der für eine Regel definierten Websites zu filtern. |
| [!UICONTROL Action] | ![Adobe Commerce](../assets/adobe-logo.svg) (nur Adobe Commerce) Klicken Sie auf **[!UICONTROL Edit]** , um die Seite _[!UICONTROL Rule Information]_anzuzeigen und die Regeleinstellungen zu aktualisieren (ähnlich wie beim Erstellen einer Regel). |
| [!UICONTROL Start] | ![Magento Open Source](../assets/open-source.svg) (nur Magento Open Source) Verwenden Sie die dynamischen Kalenderfelder (_[!UICONTROL To:]_und_[!UICONTROL From:]_), um die Liste nach dem Startdatum für die Regel zu filtern, wie bei der Regelerstellung definiert. |
| [!UICONTROL End] | ![Magento Open Source](../assets/open-source.svg) (nur Magento Open Source) Verwenden Sie die dynamischen Kalenderfelder (_[!UICONTROL To:]_und_[!UICONTROL From:]_), um die Liste nach dem Enddatum für die Regel zu filtern, wie bei der Regelerstellung definiert. |

{style="table-layout:auto"}

## Real-Time CDP-Audiences zur Information über Warenkorbpreisregeln verwenden

Erfahren Sie, wie Sie Real-Time CDP-Zielgruppen [aktivieren](../customers/audience-activation.md) in Ihrer Adobe Commerce-Instanz aktivieren, um über die Preisregeln für den Warenkorb zu informieren.
