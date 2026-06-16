---
title: Warenkorb-Preisregeln
description: Erfahren Sie mehr über die Regeln für den Warenkorbpreis, die Rabatte auf Artikel im Warenkorb basierend auf einer Reihe von Bedingungen anwenden.
exl-id: f3038f2a-9d34-4696-a39e-f87fbb1294a2
feature: Merchandising, Price Rules, Shopping Cart
TQID: https://experienceleague.adobe.com/i3G3iGuomU0cjy3aX9eynyzAtpCgQxeEFAyRUdUUu44
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: b5520579-b31f-4df7-9281-f0d9f91e2edcid: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 451
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

   - ![Magento Open Source](../assets/open-source.svg) (nur Magento Open Source) Klicken Sie auf die Regel in der Liste, um die Seite mit den Regelinformationen anzuzeigen.

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
| [!UICONTROL Start] | ![Magento Open Source](../assets/open-source.svg) (nur Magento Open Source) Verwenden Sie die dynamischen Kalenderfelder (_[!UICONTROL To:]_und_[!UICONTROL From:]_), um die Liste nach dem Startdatum für die Regel zu filtern, wie es bei der Erstellung der Regel definiert wurde. |
| [!UICONTROL End] | ![Magento Open Source](../assets/open-source.svg) (nur Magento Open Source) Verwenden Sie die dynamischen Kalenderfelder (_[!UICONTROL To:]_und_[!UICONTROL From:]_), um die Liste nach dem Enddatum für die Regel zu filtern, wie es zum Zeitpunkt der Regelerstellung definiert wurde. |

{style="table-layout:auto"}

## Verwenden Sie Real-Time CDP-Zielgruppen, um die Preisregeln für den Warenkorb zu informieren

Erfahren Sie, wie [ Real-Time CDP](../customers/audience-activation.md)Zielgruppen in Ihrer Adobe Commerce-Instanz aktivieren, um über die Regeln für den Warenkorbpreis zu informieren.
