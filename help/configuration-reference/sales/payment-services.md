---
title: '[!UICONTROL Sales] &gt; [!UICONTROL Payment Methods] &gt; [!UICONTROL Payment Services]'
description: Überprüfen Sie die Konfigurationseinstellungen im Abschnitt [!UICONTROL Payment Services] auf der Seite [!UICONTROL Sales] &gt; [!UICONTROL Payment Methods] des Commerce-Administrators.
exl-id: 255b7bd8-1d32-4393-9eba-43dc7754c752
feature: Configuration, Payments
source-git-commit: bf166c1debd7f10a4d988d231a1a47f32c4cea9e
workflow-type: tm+mt
source-wordcount: '526'
ht-degree: 0%

---

# [!UICONTROL Sales] > [!UICONTROL Payment Methods] > [!UICONTROL Payment Services]



Zahlungsdienste bieten eine schlüsselfertige Self-Service-Lösung, einschließlich Sandbox-Tests und einer einfachen Einrichtung, um eine robuste und sichere Zahlungsverarbeitung zu gewährleisten. Weitere Informationen finden Sie im [_Benutzerhandbuch für Zahlungsdienste_](https://experienceleague.adobe.com/docs/commerce-merchant-services/payment-services/guide-overview.html).

Um auf die Konfigurationseinstellungen für Zahlungsdienste zuzugreifen, gehen Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Sales]** > **[!UICONTROL Payment Services]** und klicken Sie auf **[!UICONTROL Settings]**.

![Zahlungsdiensteinstellungen](assets/payment-services-menu-small.png){width="400"}

>[!NOTE]
>
>Informationen zur Verwendung der alten Konfiguration anstelle von [Einstellungen](https://experienceleague.adobe.com/docs/commerce-merchant-services/payment-services/configure/settings.html) finden Sie unter [Legacy configuration](https://experienceleague.adobe.com/docs/commerce-merchant-services/payment-services/configure/configure-admin.html).

## [!UICONTROL General]

![Allgemeine Einstellungen](assets/payments-general-settings.png){width="600" zoomable="yes"}

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|---|---|---|
| [!UICONTROL Enable] | website | Aktivieren oder deaktivieren Sie [!DNL Payment Services] für Ihre Website. Optionen: [!UICONTROL Yes] / [!UICONTROL No] |
| [!UICONTROL Payment mode] | Store-Ansicht | Legen Sie die -Methode oder -Umgebung für Ihren Store fest. Optionen: [!UICONTROL Sandbox] / [!UICONTROL Production] |
| [!UICONTROL Sandbox Merchant ID] | Store-Ansicht | Ihre Sandbox-Händler-ID, die beim Sandbox-Onboarding automatisch generiert wird. |
| [!UICONTROL Production Merchant ID] | Store-Ansicht | Ihre Produktions-Händler-ID, die beim Sandbox-Onboarding automatisch generiert wird. |
| [!UICONTROL Soft Descriptor] | Website- oder Store-Ansicht | Fügen Sie Ihren Websites einen weichen Deskriptor hinzu und speichern Sie Ansichten, die Informationen für Kundentransaktionen bereitstellen und Marken, Stores oder Produktlinien abgrenzen. Mit dem Umschalter [!UICONTROL Use website] wird jeder weiche Deskriptor angewendet, der auf Website-Ebene hinzugefügt wird. Mit dem Umschalter [!UICONTROL Use default] wird jeder weiche Deskriptor angewendet, der als Standard hinzugefügt wurde. |

{style="table-layout:auto"}

## [!UICONTROL Credit card fields]

![Einstellungen für Kreditkartenfelder](assets/payments-ccfields-settings.png){width="600" zoomable="yes"}

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|---|---|---|
| [!UICONTROL Title] | Store-Ansicht | Fügen Sie den Text für die Anzeige als Titel für diese Zahlungsoption in der Ansicht Zahlungsmethode während des Checkouts hinzu. |
| [!UICONTROL Payment Action] | website | Die [Zahlungsaktion](payment-methods.md#payment-actions) für die angegebene Zahlungsmethode. Optionen: [!UICONTROL Authorize] / [!UICONTROL Authorize and Capture] |
| [!UICONTROL 3DS Secure authentication] | website | Aktivieren oder deaktivieren Sie die sichere [3DS-Authentifizierung](https://experienceleague.adobe.com/docs/commerce-merchant-services/payment-services/security-compliance/security.html#3ds). Optionen: [!UICONTROL Always] / [!UICONTROL When Required] / [!UICONTROL Off] |
| [!UICONTROL Show on checkout page] | website | Aktivieren oder deaktivieren Sie Kreditkartenfelder, die auf der Checkout-Seite angezeigt werden. Optionen: [!UICONTROL Yes] / [!UICONTROL No] |
| [!UICONTROL Vault enabled] | Store-Ansicht | Aktivieren oder deaktivieren Sie die [Kreditkartenausgabe](https://experienceleague.adobe.com/docs/commerce-merchant-services/payment-services/payments-checkout/vaulting.html). Optionen: [!UICONTROL Yes] / [!UICONTROL No] |
| [!UICONTROL Show vaulted payment methods in Admin] | Store-Ansicht | Aktivieren oder deaktivieren Sie die Möglichkeit, Kundenaufträge in der Admin-Konsole [mit einer gültigen Zahlungsmethode](https://experienceleague.adobe.com/docs/commerce-merchant-services/payment-services/payments-checkout/vaulting.html) abzuschließen. Optionen: [!UICONTROL Yes] / [!UICONTROL No] |
| [!UICONTROL Debug Mode] | website | Aktivieren oder deaktivieren Sie den Debug-Modus. Optionen: [!UICONTROL Yes] / [!UICONTROL No] |

{style="table-layout:auto"}

## [!UICONTROL Payment buttons]

![PayPal-Zahlungsschaltflächen-Einstellungen](assets/payments-ppbuttons-settings.png){width="600" zoomable="yes"}

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|---|---|---|
| [!UICONTROL Title] | Store-Ansicht | Fügen Sie den Text hinzu, der beim Checkout als Titel für diese Zahlungsoption angezeigt werden soll. |
| [!UICONTROL Payment Action] | website | Die [Zahlungsaktion](payment-methods.md#payment-actions){target="_blank"} für die angegebene Zahlungsmethode. Optionen: [!UICONTROL Authorize] / [!UICONTROL Authorize and Capture] |
| [!UICONTROL Show PayPal buttons on checkout page] | Store-Ansicht | Aktivieren oder deaktivieren Sie [!DNL PayPal Smart Buttons] auf der Checkout-Seite. Optionen: [!UICONTROL  Yes] / [!UICONTROL No] |
| [!UICONTROL Show PayPal buttons on product detail page] | Store-Ansicht | Aktivieren oder deaktivieren Sie [!DNL PayPal Smart Buttons] auf der Produktdetailseite. Optionen: [!UICONTROL  Yes] / [!UICONTROL No] |
| [!UICONTROL Show PayPal buttons in mini-cart preview] | Store-Ansicht | Aktivieren oder deaktivieren Sie [!DNL PayPal Smart Buttons] in der Vorschau des Mini-Warenkorbs. Optionen: [!UICONTROL Yes] / [!UICONTROL No] |
| [!UICONTROL Show PayPal buttons on cart page] | Store-Ansicht | Aktivieren oder deaktivieren Sie [!DNL PayPal Smart Buttons] auf der Warenkorbseite. Optionen: [!UICONTROL Yes] / [!UICONTROL No] |
| [!UICONTROL Show PayPal Pay Later button] | Store-Ansicht | Aktivieren oder deaktivieren Sie das Erscheinungsbild der Zahlungsoption Spätere Zahlung , wenn Zahlungsschaltflächen angezeigt werden. Optionen: [!UICONTROL Yes] / [!UICONTROL No] |
| [!UICONTROL Show PayPal Pay Later Message] | website | Aktivieren oder deaktivieren Sie die &quot;Später bezahlen&quot;-Benachrichtigung im Warenkorb, auf der Produktseite, im Mini-Warenkorb und während des Checkout-Verfahrens. Optionen: [!UICONTROL Yes] / [!UICONTROL No] |
| [!UICONTROL Show Venmo button] | Store-Ansicht | Aktivieren oder deaktivieren Sie die Zahlungsoption Venmo , wenn Zahlungsschaltflächen angezeigt werden. Optionen: [!UICONTROL Yes] / [!UICONTROL No] |
| [!UICONTROL Show Apple Pay button] | Store-Ansicht | Aktivieren oder deaktivieren Sie die Apple-Zahlungsoption, bei der Zahlungsschaltflächen angezeigt werden. Optionen: [!UICONTROL Yes] / [!UICONTROL No] |
| [!UICONTROL Show PayPal Credit and Debit card button] | Store-Ansicht | Aktivieren oder deaktivieren Sie die Option Kreditkartenzahlung und Debitkarte, wenn Zahlungsschaltflächen angezeigt werden. Optionen: [!UICONTROL Yes] / [!UICONTROL No] |
| [!UICONTROL Debug Mode] | website | Aktivieren oder deaktivieren Sie den Debug-Modus. Optionen: [!UICONTROL Yes] / [!UICONTROL No] |

{style="table-layout:auto"}

## [!UICONTROL PayPal Smart Button Styling]

![Stileinstellungen für PayPal-Zahlungsschaltflächen](assets/payments-buttonstyle-settings.png){width="600" zoomable="yes"}

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Layout] | Store-Ansicht | Definieren Sie den Stil des Layouts für Zahlungsschaltflächen. Optionen: [!UICONTROL Vertical] / [!UICONTROL Horizontal] |
| [!UICONTROL Tagline] | Store-Ansicht | Aktivieren/deaktivieren Sie die Tagline. Optionen: [!UICONTROL Yes] / [!UICONTROL No] |
| [!UICONTROL Color] | Store-Ansicht | Definieren Sie die Farbe der Zahlungsschaltflächen. Optionen: [!UICONTROL Blue] / [!UICONTROL Gold] / [!UICONTROL Silver] / [!UICONTROL White] / [!UICONTROL Black] |
| [!UICONTROL Shape] | Store-Ansicht | Definieren Sie die Form der Zahlungsschaltflächen. Optionen: [!UICONTROL Rectangular] / [!UICONTROL Pill] |
| [!UICONTROL Responsive Button Height] | Store-Ansicht | Definiert, ob Zahlungsschaltflächen eine Standardhöhe verwenden. Optionen: [!UICONTROL Yes] / [!UICONTROL No] |
| [!UICONTROL Height] | Store-Ansicht | Definieren Sie die Höhe der Zahlungsschaltflächen. Standardwert: keiner |
| [!UICONTROL Label] | Store-Ansicht | Definieren Sie den Titel, der in den Zahlungsschaltflächen angezeigt wird. Optionen: [!UICONTROL PayPal] / [!UICONTROL Checkout] / [!UICONTROL Buynow] / [!UICONTROL Pay] / [!UICONTROL Installment] |

{style="table-layout:auto"}
