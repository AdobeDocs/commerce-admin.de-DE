---
title: '[!UICONTROL Security] &gt; [!UICONTROL Google reCAPTCHA Storefront]'
description: Überprüfen Sie die Konfigurationseinstellungen auf der Seite [!UICONTROL Security] &gt; [!UICONTROL Google reCAPTCHA Storefront] des Commerce-Administrators.
exl-id: 6c03ee68-7421-4c74-bdc1-0855f088b7f9
feature: Configuration, Security
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '1283'
ht-degree: 0%

---

# [!UICONTROL Security] > [!UICONTROL Google reCAPTCHA Storefront]

>[!IMPORTANT]
>
>Bevor Google reCAPTCHA konfiguriert werden kann, müssen Sie sicherstellen, dass Ihre `PHP.ini`-Datei die folgende Einstellung enthält: `allow_url_fopen = 1`. Dies erfordert möglicherweise Hilfe von Entwicklern. Siehe [PHP-Einstellungen](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/php-settings.html) im _Installationshandbuch_.

{{config}}

Weitere Informationen zur Verwendung von Google reCAPTCHA zum Schützen Ihres Stores finden Sie unter Google [reCAPTCHA](../../systems/security-google-recaptcha.md) im _Administratorsystemhandbuch_.

## [!UICONTROL reCAPTCHA v2 ("I am not a robot")]

![reCAPTCHA v2 (&quot;Ich bin kein Roboter&quot;)](./assets/recaptcha-storefront-v2-not-robot.png)<!-- zoom -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--|--|--|
| [!UICONTROL Google API Website Key] | Webseite | Der Website-Schlüssel, der bei der Registrierung Ihres Google reCAPTCHA-Kontos erstellt wird. |
| [!UICONTROL Google API Secret Key] | Webseite | Der geheime Schlüssel, der mit Ihrem Google reCAPTCHA-Konto verknüpft ist. |
| [!UICONTROL Size] | Webseite | Die Größe des Google reCAPTCHA-Felds, das angezeigt wird, wenn sich ein Kunde bei seinem Konto anmeldet. Optionen: `Normal` (Standard) / `Compact` |
| [!UICONTROL Theme] | Webseite | Bestimmt den Stil des Google reCAPTCHA-Felds. Optionen: `Light Theme` (Standard) / `Dark Theme` |
| [!UICONTROL Language Code] | Store-Ansicht | Der [zweistellige Code](https://developers.google.com/recaptcha/docs/language), der die Sprache angibt, die für Google-reCAPTCHA-Text und -Messaging verwendet wird. |

{style="table-layout:auto"}

## [!UICONTROL reCAPTCHA v2 Invisible]

![reCAPTCHA v2 Invisible](./assets/recaptcha-storefront-v2-invisible.png)<!-- zoom -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--|--|--|
| [!UICONTROL Google API Website Key] | Webseite | Der Website-Schlüssel, der bei der Registrierung Ihres Google reCAPTCHA-Kontos erstellt wird. |
| [!UICONTROL Google API Secret Key] | Webseite | Der geheime Schlüssel, der mit Ihrem Google reCAPTCHA-Konto verknüpft ist. |
| [!UICONTROL Invisible Badge Position] | Webseite | Die Position des unsichtbaren reCAPTCHA-Badges auf jeder Seite. Optionen: `Inline` / `Bottom Right` / `Bottom Left` |
| [!UICONTROL Theme] | Global | Bestimmt den Stil des Google reCAPTCHA-Felds. Optionen: `Light Theme` (Standard) / `Dark Theme` |
| [!UICONTROL Language Code] | Store-Ansicht | Ein [zweistelliger Code](https://developers.google.com/recaptcha/docs/language), der die Sprache angibt, die für Google-reCAPTCHA-Text und -Nachrichten verwendet wird. |

{style="table-layout:auto"}

## [!UICONTROL reCAPTCHA v3 Invisible]

![reCAPTCHA v3 Invisible](./assets/recaptcha-storefront-v3-invisible.png)<!-- zoom -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--|--|--|
| [!UICONTROL Google API Website Key] | Webseite | Der Website-Schlüssel, der bei der Registrierung Ihres Google reCAPTCHA-Kontos erstellt wird. |
| [!UICONTROL Google API Secret Key] | Webseite | Der geheime Schlüssel, der mit Ihrem Google reCAPTCHA-Konto verknüpft ist. |
| [!UICONTROL Minimum Score Threshold] | Global | Der Mindestwert, der eine Benutzerinteraktion als potenzielles Risiko angibt, wobei 1.0 eine typische Benutzerinteraktion und 0.0 wahrscheinlich ein Bot ist. Standard: `0.5` |
| [!UICONTROL Invisible Badge Position] | Webseite | Die Position des unsichtbaren reCAPTCHA-Badges auf jeder Seite. Optionen: `Inline` / `Bottom Right` / `Bottom Left` |
| [!UICONTROL Theme] | Webseite | Bestimmt den Stil des Google reCAPTCHA-Felds. Optionen: `Light Theme` (Standard) / `Dark Theme` |
| [!UICONTROL Language Code] | Store-Ansicht | Ein [zweistelliger Code](https://developers.google.com/recaptcha/docs/language), der die Sprache angibt, die für Google-reCAPTCHA-Text und -Nachrichten verwendet wird. |

{style="table-layout:auto"}

## [!UICONTROL reCAPTCHA Failure Messages]

![Fehlermeldungen](./assets/recaptcha-storefront-failure-messages.png)<!-- zoom -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--|--|--|
| [!UICONTROL reCAPTCHA Validation Failure Message] | Store-Ansicht | Die Meldung, die in der Storefront angezeigt wird, wenn die Überprüfung fehlschlägt. Standardtext: `reCAPTCHA verification failed.` |
| [!UICONTROL reCAPTCHA Technical Failure Message] | Store-Ansicht | Die Meldung, die in der Storefront angezeigt wird, wenn reCAPTCHA kein Überprüfungsergebnis zurückgibt. Standardtext: `Something went wrong with reCAPTCHA. Please contact the store owner.` |

{style="table-layout:auto"}

## [!UICONTROL Storefront]

![Storefront](./assets/recaptcha-storefront.png)<!-- zoom -->

>[!NOTE]
>
>Der von Ihnen ausgewählte reCAPTCHA-Typ muss mit dem Typ übereinstimmen, der dem API-Schlüssel aus Ihrem Google reCAPTCHA-Konto zugeordnet ist.

>[!WARNING]
>
>Bei Verwendung von reCAPTCHA Version 3 kann ein echter Benutzer mit niedrigem Score nicht fortfahren. Für Version 2 erhält ein echter Benutzer mit einer niedrigen Punktzahl eine Herausforderung. Überlegen Sie genau, ob echte Benutzer mit einem niedrigen Score die Möglichkeit haben sollten, eine Herausforderung zu lösen (Version 2) oder blockiert zu werden (Version 3).

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--|--|--|
| [!UICONTROL Enable for Customer Login] | Webseite | Gibt den Typ von reCAPTCHA an, der verwendet wird, wenn Kunden [sich bei ihren Konten anmelden](../../customers/customer-sign-in.md). Optionen:<br/>**`No`**- (Standard) Die Anmeldeanforderung wird nicht validiert.<br />**`reCAPTCHA v2 ("I am not a robot")`** - Erfordert, dass der Benutzer das Kontrollkästchen _Ich bin kein Roboter_ auswählt.<br />**`Invisible reCAPTCHA v2`**- Validiert das Benutzerverhalten im Hintergrund, ohne dass Interaktionen basierend auf dem Ergebnis erforderlich sind.<br/>**`Invisible reCAPTCHA v3`** - (Empfohlen) Validiert das Benutzerverhalten im Hintergrund basierend auf dem Interaktionsergebnis. |
| [!UICONTROL Enable for Forgot Password] | Webseite | Gibt den Typ von reCAPTCHA an, der verwendet wird, wenn Kunden eine [Kennwortrücksetzung](../../customers/password-reset.md) anfordern. Optionen:<br/>**`No`**- (Standard) Prüft die Anforderung zum Zurücksetzen des Kennworts nicht.<br />**`reCAPTCHA v2 ("I am not a robot")`** - Erfordert, dass der Benutzer das Kontrollkästchen _Ich bin kein Roboter_ auswählt.<br />**`Invisible reCAPTCHA v2`**- Validiert das Benutzerverhalten im Hintergrund, ohne dass Interaktionen basierend auf dem Ergebnis erforderlich sind.<br/>**`Invisible reCAPTCHA v3`** - (Empfohlen) Validiert das Benutzerverhalten im Hintergrund basierend auf dem Interaktionsergebnis. |
| [!UICONTROL Enable for Create New Customer Account] | Webseite | Gibt den Typ von reCAPTCHA an, der verwendet wird, wenn sich der Kunde für ein [neues Konto](../../customers/account-create.md) anmeldet. Optionen:<br/>**`No`**- (Standard) Die Kontoanforderung wird nicht validiert.<br />**`reCAPTCHA v2 ("I am not a robot")`** - Erfordert, dass der Benutzer das Kontrollkästchen _Ich bin kein Roboter_ auswählt.<br />**`Invisible reCAPTCHA v2`**- Validiert das Benutzerverhalten im Hintergrund, ohne dass Interaktionen basierend auf dem Ergebnis erforderlich sind.<br/>**`Invisible reCAPTCHA v3`** - (Empfohlen) Validiert das Benutzerverhalten im Hintergrund basierend auf dem Interaktionsergebnis. |
| [!UICONTROL Enable for Edit Customer Account] | Webseite | Gibt den Typ von reCAPTCHA an, der verwendet wird, wenn der Kunde seine [Kontoinformationen](../../customers/account-dashboard-account-information.md) ändert. Optionen:<br/>**`No`**- (Standard) Die Kontoanforderung wird nicht validiert.<br />**`reCAPTCHA v2 ("I am not a robot")`** - Erfordert, dass der Benutzer das Kontrollkästchen _Ich bin kein Roboter_ auswählt.<br />**`Invisible reCAPTCHA v2`**- Validiert das Benutzerverhalten im Hintergrund, ohne dass Interaktionen basierend auf dem Ergebnis erforderlich sind.<br/>**`Invisible reCAPTCHA v3`** - (Empfohlen) Validiert das Benutzerverhalten im Hintergrund basierend auf dem Interaktionsergebnis. |
| [!UICONTROL Enable for Create New Company Account] | Webseite | ![Adobe Commerce B2B](../../assets/b2b.svg) (Nur für Adobe Commerce B2B verfügbar) Gibt den Typ von reCAPTCHA an, der verwendet wird, wenn ein neues [Unternehmenskonto](../../b2b/account-company-create.md) erstellt wird. Optionen:<br/>**`No`**- (Standard) Die Kontoanforderung wird nicht validiert.<br />**`reCAPTCHA v2 ("I am not a robot")`** - Erfordert, dass der Benutzer das Kontrollkästchen _Ich bin kein Roboter_ auswählt.<br />**`Invisible reCAPTCHA v2`**- Validiert das Benutzerverhalten im Hintergrund, ohne dass Interaktionen basierend auf dem Ergebnis erforderlich sind.<br/>**`Invisible reCAPTCHA v3`** - (Empfohlen) Validiert das Benutzerverhalten im Hintergrund basierend auf dem Interaktionsergebnis. |
| [!UICONTROL Enable for Contact Us] | Webseite | Gibt den Typ von reCAPTCHA an, der zum Senden einer Nachricht von der Seite [Kontaktaufnahme](../../getting-started/store-details.md#contact-us-form) Ihres Stores verwendet wird. Optionen:<br/>**`No`**- (Standard) Die Nachrichtenanforderung wird nicht validiert.<br />**`reCAPTCHA v2 ("I am not a robot")`** - Erfordert, dass der Benutzer das Kontrollkästchen _Ich bin kein Roboter_ auswählt.<br />**`Invisible reCAPTCHA v2`**- Validiert das Benutzerverhalten im Hintergrund, ohne dass Interaktionen basierend auf dem Ergebnis erforderlich sind.<br/>**`Invisible reCAPTCHA v3`** - (Empfohlen) Validiert das Benutzerverhalten im Hintergrund basierend auf dem Interaktionsergebnis. |
| [!UICONTROL Enable for Product Review] | Webseite | Gibt den Typ von reCAPTCHA an, der verwendet wird, wenn Kunden eine [Produktüberprüfung](../../merchandising-promotions/product-reviews.md) einreichen. Optionen:<br/>**`No`**- (Standard) Prüft die Produktüberprüfungsanforderung nicht.<br />**`reCAPTCHA v2 ("I am not a robot")`** - Erfordert, dass der Benutzer das Kontrollkästchen _Ich bin kein Roboter_ auswählt.<br />**`Invisible reCAPTCHA v2`**- Validiert das Benutzerverhalten im Hintergrund, ohne dass Interaktionen basierend auf dem Ergebnis erforderlich sind.<br/>**`Invisible reCAPTCHA v3`** - (Empfohlen) Validiert das Benutzerverhalten im Hintergrund basierend auf dem Interaktionsergebnis. |
| [!UICONTROL Enable for Newsletter Subscription] | Webseite | Gibt den Typ des unsichtbaren reCAPTCHA an, der verwendet wird, wenn sich Kunden für ein [Newsletter-Abonnement](../../merchandising-promotions/newsletter-subscribers.md) anmelden. Optionen:<br/>**`No`**- (Standard) Die Newsletter-Abonnementanforderung wird nicht validiert.<br />**`reCAPTCHA v2 ("I am not a robot")`** - Erfordert, dass der Benutzer das Kontrollkästchen _Ich bin kein Roboter_ auswählt.<br />**`Invisible reCAPTCHA v2`**- Validiert das Benutzerverhalten im Hintergrund, ohne dass Interaktionen basierend auf dem Ergebnis erforderlich sind.<br/>**`Invisible reCAPTCHA v3`** - (Empfohlen) Validiert das Benutzerverhalten im Hintergrund basierend auf dem Interaktionsergebnis. |
| [!UICONTROL Enable for Gift Card] | Webseite | ![Adobe Commerce](../../assets/adobe-logo.svg) (nur Adobe Commerce) Gibt den Typ von reCAPTCHA an, der verwendet wird, wenn Kunden einen Code für eine [Geschenkkarte](../../catalog/product-gift-card-create.md) eingeben. Optionen:<br/>**`No`**- (Standard) Die Übermittlung des Gutscheincodes wird nicht validiert.<br />**`reCAPTCHA v2 ("I am not a robot")`** - Erfordert, dass der Benutzer das Kontrollkästchen _Ich bin kein Roboter_ auswählt.<br />**`Invisible reCAPTCHA v2`**- Validiert das Benutzerverhalten im Hintergrund, ohne Interaktionen basierend auf dem Ergebnis erforderlich zu sein.<br/>**`Invisible reCAPTCHA v3`** - (Empfohlen) Validiert das Benutzerverhalten im Hintergrund basierend auf dem Interaktionsergebnis. |
| [!UICONTROL Enable for Invitation Create Account] | Webseite | Gibt den Typ von reCAPTCHA an, der verwendet wird, wenn Kunden einen Code zur Kontoerstellung senden, [Einladung](../../merchandising-promotions/invitations.md). Optionen:<br/>**`No`**- (Standard) Die Einladungs-E-Mail-Übermittlung wird nicht validiert.<br />**`reCAPTCHA v2 ("I am not a robot")`** - Erfordert, dass der Benutzer das Kontrollkästchen _Ich bin kein Roboter_ auswählt.<br />**`Invisible reCAPTCHA v2`**- Validiert das Benutzerverhalten im Hintergrund, ohne Interaktionen basierend auf dem Ergebnis erforderlich zu sein.<br/>**`Invisible reCAPTCHA v3`** - (Empfohlen) Validiert das Benutzerverhalten im Hintergrund basierend auf dem Interaktionsergebnis. |
| [!UICONTROL Enable for Send to Friend] | Webseite | Gibt den Typ von reCAPTCHA an, der verwendet wird, wenn Kunden [ein Produkt mit einem Freund teilen](../../stores-purchase/email-a-friend.md). Optionen:<br/>**`No`**- (Standard) Die Übermittlung der E-Mail wird nicht validiert.<br />**`reCAPTCHA v2 ("I am not a robot")`** - Erfordert, dass der Benutzer das Kontrollkästchen _Ich bin kein Roboter_ auswählt.<br />**`Invisible reCAPTCHA v2`**- Validiert das Benutzerverhalten im Hintergrund, ohne dass Interaktionen basierend auf dem Ergebnis erforderlich sind.<br/>**`Invisible reCAPTCHA v3`** - (Empfohlen) Validiert das Benutzerverhalten im Hintergrund basierend auf dem Interaktionsergebnis. |
| [!UICONTROL Enable for Wishlist Sharing] | Webseite | Gibt den Typ von reCAPTCHA an, der verwendet wird, wenn Kunden [eine Wunschliste teilen](../../stores-purchase/wishlist-storefront.md#share-the-wish-list). Optionen:<br/>**`No`**- (Standard) Prüft die Nachricht und die E-Mail-Übermittlung nicht.<br />**`reCAPTCHA v2 ("I am not a robot")`** - Erfordert, dass der Benutzer das Kontrollkästchen _Ich bin kein Roboter_ auswählt.<br />**`Invisible reCAPTCHA v2`**- Validiert das Benutzerverhalten im Hintergrund, ohne Interaktionen basierend auf dem Ergebnis erforderlich zu sein.<br/>**`Invisible reCAPTCHA v3`** - (Empfohlen) Validiert das Benutzerverhalten im Hintergrund basierend auf dem Interaktionsergebnis. |
| [!UICONTROL Enable for Coupon Codes] | Webseite | Gibt den Typ von reCAPTCHA an, der verwendet wird, wenn Kunden einen [Couponcode](../../merchandising-promotions/price-rules-cart-coupon.md) eingeben. Optionen:<br/>**`No`**- (Standard) Die Übermittlung des Gutscheincodes wird nicht validiert.<br />**`reCAPTCHA v2 ("I am not a robot")`** - Erfordert, dass der Benutzer das Kontrollkästchen _Ich bin kein Roboter_ auswählt.<br />**`Invisible reCAPTCHA v2`**- Validiert das Benutzerverhalten im Hintergrund, ohne Interaktionen basierend auf dem Ergebnis erforderlich zu sein.<br/>**`Invisible reCAPTCHA v3`** - (Empfohlen) Validiert das Benutzerverhalten im Hintergrund basierend auf dem Interaktionsergebnis. |
| [!UICONTROL Enable for PayPal Payflow Pro payment form] | Webseite | Gibt den Typ von reCAPTCHA an, der verwendet wird, wenn Kunden für einen Kauf mit [PayPal Payflow Pro](../../stores-purchase/paypal-payflow-pro.md) bezahlen. Optionen:<br/>**`No`**- (Standard) Prüft die Anforderung zum Zurücksetzen des Kennworts nicht.<br />**`reCAPTCHA v2 ("I am not a robot")`** - Erfordert, dass der Benutzer das Kontrollkästchen _Ich bin kein Roboter_ auswählt.<br />**`Invisible reCAPTCHA v2`**- Validiert das Benutzerverhalten im Hintergrund, ohne dass Interaktionen basierend auf dem Ergebnis erforderlich sind.<br/>**`Invisible reCAPTCHA v3`** - (Empfohlen) Validiert das Benutzerverhalten im Hintergrund basierend auf dem Interaktionsergebnis. |

{style="table-layout:auto"}
