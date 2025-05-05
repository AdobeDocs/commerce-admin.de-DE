---
title: Warenkorb-Preisregeln
description: Erfahren Sie mehr über die Regeln für den Warenkorbpreis, die Rabatte auf Artikel im Warenkorb basierend auf einer Reihe von Bedingungen anwenden.
exl-id: f3038f2a-9d34-4696-a39e-f87fbb1294a2
feature: Merchandising, Price Rules, Shopping Cart
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '448'
ht-degree: 0%

---

# Warenkorb-Preisregeln

Die Regeln für den Warenkorbpreis wenden Rabatte auf Artikel im Warenkorb an, die auf einer Reihe von Bedingungen basieren. Der Rabatt kann automatisch angewendet werden, wenn die Bedingungen erfüllt sind oder wenn der Kunde einen gültigen Gutscheincode eingibt. Wenn angewendet, wird der Rabatt im Warenkorb unter der Zwischensumme angezeigt. Eine Warenkorb-Preisregel kann bei Bedarf für eine Saison oder Promotion verwendet werden, indem ihr Status und ihr Datumsbereich geändert werden.

>[!NOTE]
>
>Wenn die Warenkorbregel für Coupons Bedingungen enthält, die Checkout-Optionen angeben, z. B. bestimmte Versand- oder Zahlungsmethoden, werden die Bedingungen erst beim Checkout erfüllt, nachdem die spezifischen Versand-/Zahlungsmethoden ausgewählt wurden. In diesem Fall kann der Coupon an der Kasse im letzten Schritt angewendet werden.

![Beispiel-Storefront - Warenkorb - Gutschein anwenden](./assets/storefront-cart-apply-coupon.png){width="600" zoomable="yes"}

## Preisregeln für Warenkorb aufrufen

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_>**[!UICONTROL Cart Price Rules]**.

   ![Warenkorb-Preisregel](./assets/price-rule-cart.png){width="700" zoomable="yes"}

1. Wenn Sie über viele Regeln verfügen, verwenden Sie die Filteroptionen oben in jeder Spalte, um die Liste zu optimieren, und klicken Sie auf **[!UICONTROL Search]** , um die Filter anzuwenden.

1. Um alle Filteroptionen zu löschen und die vollständige Liste anzuzeigen, klicken Sie auf **[!UICONTROL Reset Filter]**.

1. Aktualisieren von Eigenschaften für eine Regel:

   - ![Adobe Commerce](../assets/adobe-logo.svg) (nur Adobe Commerce) Klicken Sie auf **[!UICONTROL Edit]** , um die Seite mit den Regelinformationen anzuzeigen.

   - ![Magento Open Source ](../assets/open-source.svg) (nur Magento Open Source) Klicken Sie auf die Regel in der Liste, um die Seite mit den Regelinformationen anzuzeigen.

   Dort können Sie die Einstellungen für die Regel ändern (ähnlich wie beim Erstellen einer Regel).

## Optionen nach Spalte filtern

| Spalte | Beschreibung |
|--- |--- |
| [!UICONTROL ID] | Geben Sie einen Text ein, um die Liste nach einer bestimmten Regel-ID-Nummer zu filtern. |
| [!UICONTROL Rule] | Geben Sie einen Text ein, um die Liste nach dem Regelnamen zu filtern, der bei der Erstellung der Regel definiert wurde. |
| [!UICONTROL Coupon Code] | Geben Sie einen Text ein, um die Liste nach dem bei der Regelerstellung definierten Codenamen zu filtern. |
| [!UICONTROL Priority] | Ein Freitextfeld, das die Liste nach der für eine Regel definierten Priorität filtert. |
| [!UICONTROL Status] | Verwenden Sie diese Option, um die Liste nach Regelstatus (`Active` oder `Inactive`) zu filtern. |
| [!UICONTROL Web Site] | Verwenden Sie diese Option, um die Liste nach für eine Regel definierten Websites zu filtern. |
| [!UICONTROL Action] | ![Adobe Commerce](../assets/adobe-logo.svg) (nur Adobe Commerce) Klicken Sie auf **[!UICONTROL Edit]**, um die Seite &quot;_[!UICONTROL Rule Information]_&quot; anzuzeigen und die Regeleinstellungen zu aktualisieren (ähnlich wie beim Erstellen einer Regel). |
| [!UICONTROL Start] | ![Magento Open Source ](../assets/open-source.svg) (nur Magento Open Source) Verwenden Sie die dynamischen Kalenderfelder (_[!UICONTROL To:]_&#x200B;und&#x200B;_[!UICONTROL From:]_), um die Liste nach dem Startdatum für die Regel zu filtern, wie es bei der Erstellung der Regel definiert wurde. |
| [!UICONTROL End] | ![Magento Open Source ](../assets/open-source.svg) (nur Magento Open Source) Verwenden Sie die dynamischen Kalenderfelder (_[!UICONTROL To:]_&#x200B;und&#x200B;_[!UICONTROL From:]_), um die Liste nach dem Enddatum für die Regel zu filtern, wie es zum Zeitpunkt der Regelerstellung definiert wurde. |

{style="table-layout:auto"}

## Verwenden Sie Real-Time CDP-Zielgruppen, um die Preisregeln für den Warenkorb zu informieren

Erfahren Sie, wie [ Real-Time CDP](../customers/audience-activation.md)Zielgruppen in Ihrer Adobe Commerce-Instanz aktivieren, um über die Regeln für den Warenkorbpreis zu informieren.
