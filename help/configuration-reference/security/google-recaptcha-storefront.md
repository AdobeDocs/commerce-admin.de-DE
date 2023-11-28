---
title: '[!UICONTROL Security] &gt; [!UICONTROL Google reCAPTCHA Storefront]'
description: Überprüfen Sie die Konfigurationseinstellungen auf der [!UICONTROL Security] &gt; [!UICONTROL Google reCAPTCHA Storefront] Seite des Commerce-Administrators.
exl-id: 6c03ee68-7421-4c74-bdc1-0855f088b7f9
feature: Configuration, Security
source-git-commit: 76bd1b1af9b55d69bd98209d70fb5518f190a3e1
workflow-type: tm+mt
source-wordcount: '1314'
ht-degree: 0%

---

# [!UICONTROL Security] > [!UICONTROL Google reCAPTCHA Storefront]

>[!IMPORTANT]
>
>Bevor Google reCAPTCHA konfiguriert werden kann, müssen Sie sicherstellen, dass Ihre `PHP.ini` -Datei enthält die folgende Einstellung: `allow_url_fopen = 1`. Dies erfordert möglicherweise Hilfe von Entwicklern. Siehe [PHP-Einstellungen](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/php-settings.html) im _Installationsanleitung_.

{{config}}

Weitere Informationen zur Verwendung von Google reCAPTCHA zum Sichern Ihres Stores finden Sie unter Google [reCAPTCHA](../../systems/security-google-recaptcha.md) im _Administratorsystemanleitung_.

## [!UICONTROL reCAPTCHA v2 ("I am not a robot")]

![reCAPTCHA v2 (&quot;Ich bin kein Roboter&quot;)](./assets/recaptcha-storefront-v2-not-robot.png)<!-- zoom -->

| Feld | [Anwendungsbereich](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--|--|--|
| [!UICONTROL Google API Website Key] | Webseite | Der Website-Schlüssel, der bei der Registrierung Ihres Google reCAPTCHA-Kontos erstellt wird. |
| [!UICONTROL Google API Secret Key] | Webseite | Der geheime Schlüssel, der mit Ihrem Google reCAPTCHA-Konto verknüpft ist. |
| [!UICONTROL Size] | Webseite | Die Größe des Google reCAPTCHA-Felds, das angezeigt wird, wenn sich ein Kunde bei seinem Konto anmeldet. Optionen: `Normal` (Standard) / `Compact` |
| [!UICONTROL Theme] | Webseite | Bestimmt den Stil des Google reCAPTCHA-Felds. Optionen: `Light Theme` (Standard) / `Dark Theme` |
| [!UICONTROL Language Code] | Store-Ansicht | Die [Code mit zwei Zeichen](https://developers.google.com/recaptcha/docs/language) gibt die Sprache an, die für Google reCAPTCHA-Text und -Messaging verwendet wird. |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL reCAPTCHA v2 Invisible]

![reCAPTCHA v2 Invisible](./assets/recaptcha-storefront-v2-invisible.png)<!-- zoom -->

| Feld | [Anwendungsbereich](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--|--|--|
| [!UICONTROL Google API Website Key] | Webseite | Der Website-Schlüssel, der bei der Registrierung Ihres Google reCAPTCHA-Kontos erstellt wird. |
| [!UICONTROL Google API Secret Key] | Webseite | Der geheime Schlüssel, der mit Ihrem Google reCAPTCHA-Konto verknüpft ist. |
| [!UICONTROL Invisible Badge Position] | Webseite | Die Position des unsichtbaren reCAPTCHA-Badges auf jeder Seite. Optionen: `Inline` / `Bottom Right` / `Bottom Left` |
| [!UICONTROL Theme] | Global | Bestimmt den Stil des Google reCAPTCHA-Felds. Optionen: `Light Theme` (Standard) / `Dark Theme` |
| [!UICONTROL Language Code] | Store-Ansicht | A [Code mit zwei Zeichen](https://developers.google.com/recaptcha/docs/language) gibt die Sprache an, die für Google reCAPTCHA-Text und -Messaging verwendet wird. |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL reCAPTCHA v3 Invisible]

![reCAPTCHA v3 unsichtbar](./assets/recaptcha-storefront-v3-invisible.png)<!-- zoom -->

| Feld | [Anwendungsbereich](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--|--|--|
| [!UICONTROL Google API Website Key] | Webseite | Der Website-Schlüssel, der bei der Registrierung Ihres Google reCAPTCHA-Kontos erstellt wird. |
| [!UICONTROL Google API Secret Key] | Webseite | Der geheime Schlüssel, der mit Ihrem Google reCAPTCHA-Konto verknüpft ist. |
| [!UICONTROL Minimum Score Threshold] | Global | Der Mindestwert, der eine Benutzerinteraktion als potenzielles Risiko angibt, wobei 1.0 eine typische Benutzerinteraktion und 0.0 wahrscheinlich ein Bot ist. Standard: `0.5` |
| [!UICONTROL Invisible Badge Position] | Webseite | Die Position des unsichtbaren reCAPTCHA-Badges auf jeder Seite. Optionen: `Inline` / `Bottom Right` / `Bottom Left` |
| [!UICONTROL Theme] | Webseite | Bestimmt den Stil des Google reCAPTCHA-Felds. Optionen: `Light Theme` (Standard) / `Dark Theme` |
| [!UICONTROL Language Code] | Store-Ansicht | A [Code mit zwei Zeichen](https://developers.google.com/recaptcha/docs/language) gibt die Sprache an, die für Google reCAPTCHA-Text und -Messaging verwendet wird. |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL reCAPTCHA Failure Messages]

![Fehlermeldungen](./assets/recaptcha-storefront-failure-messages.png)<!-- zoom -->

| Feld | [Anwendungsbereich](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--|--|--|
| [!UICONTROL reCAPTCHA Validation Failure Message] | Store-Ansicht | Die Meldung, die in der Storefront angezeigt wird, wenn die Überprüfung fehlschlägt. Standardtext: `reCAPTCHA verification failed.` |
| [!UICONTROL reCAPTCHA Technical Failure Message] | Store-Ansicht | Die Meldung, die in der Storefront angezeigt wird, wenn reCAPTCHA kein Überprüfungsergebnis zurückgibt. Standardtext: `Something went wrong with reCAPTCHA. Please contact the store owner.` |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Storefront]

![Storefront](./assets/recaptcha-storefront.png)<!-- zoom -->

>[!NOTE]
>
>Der von Ihnen ausgewählte reCAPTCHA-Typ muss mit dem Typ übereinstimmen, der dem API-Schlüssel aus Ihrem Google reCAPTCHA-Konto zugeordnet ist.

>[!WARNING]
>
>Bei Verwendung von reCAPTCHA Version 3 kann ein echter Benutzer mit niedrigem Score nicht fortfahren. Für Version 2 erhält ein echter Benutzer mit einer niedrigen Punktzahl eine Herausforderung. Überlegen Sie genau, ob echte Benutzer mit einem niedrigen Score die Möglichkeit haben sollten, eine Herausforderung zu lösen (Version 2) oder blockiert zu werden (Version 3).

| Feld | [Anwendungsbereich](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--|--|--|
| [!UICONTROL Enable for Customer Login] | Webseite | Gibt den Typ von reCAPTCHA an, der verwendet wird, wenn Kunden [Anmelden](../../customers/customer-sign-in.md) auf ihre Konten. Optionen:<br/>**`No`**- (Standard) Die Anmeldeanforderung wird nicht validiert.<br />**`reCAPTCHA v2 ("I am not a robot")`** - Erfordert die Auswahl des _Ich bin kein Roboter_ aktivieren.<br />**`Invisible reCAPTCHA v2`**- Validiert das Benutzerverhalten im Hintergrund, ohne dass Interaktionen basierend auf dem Ergebnis erforderlich sind.<br/>**`Invisible reCAPTCHA v3`** - (Empfohlen) Validiert das Benutzerverhalten im Hintergrund basierend auf dem Interaktionswert. |
| [!UICONTROL Enable for Forgot Password] | Webseite | Gibt den Typ von reCAPTCHA an, der verwendet wird, wenn Kunden eine [Kennwortrücksetzung](../../customers/password-reset.md). Optionen:<br/>**`No`**- (Standard) Validiert die Anforderung zum Zurücksetzen des Kennworts nicht.<br />**`reCAPTCHA v2 ("I am not a robot")`** - Erfordert die Auswahl des _Ich bin kein Roboter_ aktivieren.<br />**`Invisible reCAPTCHA v2`**- Validiert das Benutzerverhalten im Hintergrund, ohne dass Interaktionen basierend auf dem Ergebnis erforderlich sind.<br/>**`Invisible reCAPTCHA v3`** - (Empfohlen) Validiert das Benutzerverhalten im Hintergrund basierend auf dem Interaktionswert. |
| [!UICONTROL Enable for Create New Customer Account] | Webseite | Gibt den Typ von reCAPTCHA an, der verwendet wird, wenn sich der Kunde für eine [neues Konto](../../customers/account-create.md). Optionen:<br/>**`No`**- (Standard) Die Kontoanforderung wird nicht validiert.<br />**`reCAPTCHA v2 ("I am not a robot")`** - Erfordert die Auswahl des _Ich bin kein Roboter_ aktivieren.<br />**`Invisible reCAPTCHA v2`**- Validiert das Benutzerverhalten im Hintergrund, ohne dass Interaktionen basierend auf dem Ergebnis erforderlich sind.<br/>**`Invisible reCAPTCHA v3`** - (Empfohlen) Validiert das Benutzerverhalten im Hintergrund basierend auf dem Interaktionswert. |
| [!UICONTROL Enable for Edit Customer Account] | Webseite | Gibt den Typ von reCAPTCHA an, der verwendet wird, wenn der Kunde seine [Kontoinformationen](../../customers/account-dashboard-account-information.md). Optionen:<br/>**`No`**- (Standard) Die Kontoanforderung wird nicht validiert.<br />**`reCAPTCHA v2 ("I am not a robot")`** - Erfordert die Auswahl des _Ich bin kein Roboter_ aktivieren.<br />**`Invisible reCAPTCHA v2`**- Validiert das Benutzerverhalten im Hintergrund, ohne dass Interaktionen basierend auf dem Ergebnis erforderlich sind.<br/>**`Invisible reCAPTCHA v3`** - (Empfohlen) Validiert das Benutzerverhalten im Hintergrund basierend auf dem Interaktionswert. |
| [!UICONTROL Enable for Create New Company Account] | Webseite | ![B2B für Adobe Commerce](../../assets/b2b.svg) (Nur bei B2B für Adobe Commerce verfügbar) Gibt den Typ von reCAPTCHA an, der bei einer neuen [Firmenkonto](../../b2b/account-company-create.md) erstellt wird. Optionen:<br/>**`No`**- (Standard) Die Kontoanforderung wird nicht validiert.<br />**`reCAPTCHA v2 ("I am not a robot")`** - Erfordert die Auswahl des _Ich bin kein Roboter_ aktivieren.<br />**`Invisible reCAPTCHA v2`**- Validiert das Benutzerverhalten im Hintergrund, ohne dass Interaktionen basierend auf dem Ergebnis erforderlich sind.<br/>**`Invisible reCAPTCHA v3`** - (Empfohlen) Validiert das Benutzerverhalten im Hintergrund basierend auf dem Interaktionswert. |
| [!UICONTROL Enable for Contact Us] | Webseite | Gibt den Typ von reCAPTCHA an, der zum Senden einer Nachricht von der [Kontakt](../../getting-started/store-details.md#contact-us-form) Seite Ihres Stores. Optionen:<br/>**`No`**- (Standard) Die Nachrichtenanforderung wird nicht validiert.<br />**`reCAPTCHA v2 ("I am not a robot")`** - Erfordert die Auswahl des _Ich bin kein Roboter_ aktivieren.<br />**`Invisible reCAPTCHA v2`**- Validiert das Benutzerverhalten im Hintergrund, ohne dass Interaktionen basierend auf dem Ergebnis erforderlich sind.<br/>**`Invisible reCAPTCHA v3`** - (Empfohlen) Validiert das Benutzerverhalten im Hintergrund basierend auf dem Interaktionswert. |
| [!UICONTROL Enable for Product Review] | Webseite | Gibt den Typ von reCAPTCHA an, der verwendet wird, wenn Kunden eine [Produktübersicht](../../merchandising-promotions/product-reviews.md). Optionen:<br/>**`No`**- (Standard) Prüft die Produktüberprüfungsanforderung nicht.<br />**`reCAPTCHA v2 ("I am not a robot")`** - Erfordert die Auswahl des _Ich bin kein Roboter_ aktivieren.<br />**`Invisible reCAPTCHA v2`**- Validiert das Benutzerverhalten im Hintergrund, ohne dass Interaktionen basierend auf dem Ergebnis erforderlich sind.<br/>**`Invisible reCAPTCHA v3`** - (Empfohlen) Validiert das Benutzerverhalten im Hintergrund basierend auf dem Interaktionswert. |
| [!UICONTROL Enable for Newsletter Subscription] | Webseite | Gibt den Typ des unsichtbaren reCAPTCHA an, der verwendet wird, wenn sich Kunden für eine [Newsletter-Abonnement](../../merchandising-promotions/newsletter-subscribers.md). Optionen:<br/>**`No`**- (Standard) Validiert die Newsletter-Abonnement-Anfrage nicht.<br />**`reCAPTCHA v2 ("I am not a robot")`** - Erfordert die Auswahl des _Ich bin kein Roboter_ aktivieren.<br />**`Invisible reCAPTCHA v2`**- Validiert das Benutzerverhalten im Hintergrund, ohne dass Interaktionen basierend auf dem Ergebnis erforderlich sind.<br/>**`Invisible reCAPTCHA v3`** - (Empfohlen) Validiert das Benutzerverhalten im Hintergrund basierend auf dem Interaktionswert. |
| [!UICONTROL Enable for Gift Card] | Webseite | ![Adobe Commerce](../../assets/adobe-logo.svg) (Nur Adobe Commerce) Gibt den Typ von reCAPTCHA an, der verwendet wird, wenn Kunden eine [Geschenkkarte](../../catalog/product-gift-card-create.md) Code. Optionen:<br/>**`No`**- (Standard) Die Übermittlung des Gutscheincodes wird nicht validiert.<br />**`reCAPTCHA v2 ("I am not a robot")`** - Erfordert die Auswahl des _Ich bin kein Roboter_ aktivieren.<br />**`Invisible reCAPTCHA v2`**- Validiert das Benutzerverhalten im Hintergrund, ohne dass Interaktionen basierend auf dem Ergebnis erforderlich sind.<br/>**`Invisible reCAPTCHA v3`** - (Empfohlen) Validiert das Benutzerverhalten im Hintergrund basierend auf dem Interaktionswert. |
| [!UICONTROL Enable for Invitation Create Account] | Webseite | Gibt den Typ von reCAPTCHA an, der verwendet wird, wenn Kunden ein Konto erstellen [Einladung](../../merchandising-promotions/invitations.md) Code. Optionen:<br/>**`No`**- (Standard) Die Einladungs-E-Mail-Übermittlung wird nicht validiert.<br />**`reCAPTCHA v2 ("I am not a robot")`** - Erfordert die Auswahl des _Ich bin kein Roboter_ aktivieren.<br />**`Invisible reCAPTCHA v2`**- Validiert das Benutzerverhalten im Hintergrund, ohne dass Interaktionen basierend auf dem Ergebnis erforderlich sind.<br/>**`Invisible reCAPTCHA v3`** - (Empfohlen) Validiert das Benutzerverhalten im Hintergrund basierend auf dem Interaktionswert. |
| [!UICONTROL Enable for Send to Friend] | Webseite | Gibt den Typ von reCAPTCHA an, der verwendet wird, wenn Kunden [Produkt freigeben](../../stores-purchase/email-a-friend.md) mit einem Freund. Optionen:<br/>**`No`**- (Standard) Die Übermittlung der E-Mail wird nicht validiert.<br />**`reCAPTCHA v2 ("I am not a robot")`** - Erfordert die Auswahl des _Ich bin kein Roboter_ aktivieren.<br />**`Invisible reCAPTCHA v2`**- Validiert das Benutzerverhalten im Hintergrund, ohne dass Interaktionen basierend auf dem Ergebnis erforderlich sind.<br/>**`Invisible reCAPTCHA v3`** - (Empfohlen) Validiert das Benutzerverhalten im Hintergrund basierend auf dem Interaktionswert. |
| [!UICONTROL Enable for Wishlist Sharing] | Webseite | Gibt den Typ von reCAPTCHA an, der verwendet wird, wenn Kunden [Wunschliste teilen](../../stores-purchase/wishlist-storefront.md#share-the-wish-list). Optionen:<br/>**`No`**- (Standard) Die Nachricht und die Übermittlung der E-Mail werden nicht validiert.<br />**`reCAPTCHA v2 ("I am not a robot")`** - Erfordert die Auswahl des _Ich bin kein Roboter_ aktivieren.<br />**`Invisible reCAPTCHA v2`**- Validiert das Benutzerverhalten im Hintergrund, ohne dass Interaktionen basierend auf dem Ergebnis erforderlich sind.<br/>**`Invisible reCAPTCHA v3`** - (Empfohlen) Validiert das Benutzerverhalten im Hintergrund basierend auf dem Interaktionswert. |
| [!UICONTROL Enable for Coupon Codes] | Webseite | Gibt den Typ von reCAPTCHA an, der verwendet wird, wenn Kunden eine [Coupon-Code](../../merchandising-promotions/price-rules-cart-coupon.md). Optionen:<br/>**`No`**- (Standard) Die Übermittlung des Gutscheincodes wird nicht validiert.<br />**`reCAPTCHA v2 ("I am not a robot")`** - Erfordert die Auswahl des _Ich bin kein Roboter_ aktivieren.<br />**`Invisible reCAPTCHA v2`**- Validiert das Benutzerverhalten im Hintergrund, ohne dass Interaktionen basierend auf dem Ergebnis erforderlich sind.<br/>**`Invisible reCAPTCHA v3`** - (Empfohlen) Validiert das Benutzerverhalten im Hintergrund basierend auf dem Interaktionswert. |
| [!UICONTROL Enable for PayPal Payflow Pro payment form] | Webseite | Gibt den Typ von reCAPTCHA an, der verwendet wird, wenn Kunden für einen Kauf mit [PayPal Payflow Pro](../../stores-purchase/paypal-payflow-pro.md). Optionen:<br/>**`No`**- (Standard) Validiert die Anforderung zum Zurücksetzen des Kennworts nicht.<br />**`reCAPTCHA v2 ("I am not a robot")`** - Erfordert die Auswahl des _Ich bin kein Roboter_ aktivieren.<br />**`Invisible reCAPTCHA v2`**- Validiert das Benutzerverhalten im Hintergrund, ohne dass Interaktionen basierend auf dem Ergebnis erforderlich sind.<br/>**`Invisible reCAPTCHA v3`** - (Empfohlen) Validiert das Benutzerverhalten im Hintergrund basierend auf dem Interaktionswert. |

{:style=&quot;table-layout:auto&quot;}
