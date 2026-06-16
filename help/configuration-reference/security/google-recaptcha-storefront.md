---
title: '[!UICONTROL Security] > [!UICONTROL Google reCAPTCHA Storefront]'
description: Überprüfen Sie die Konfigurationseinstellungen auf der Seite [!UICONTROL Security] > [!UICONTROL Google reCAPTCHA Storefront] des Commerce Admin.
exl-id: 6c03ee68-7421-4c74-bdc1-0855f088b7f9
feature: Configuration, Security
TQID: https://experienceleague.adobe.com/Hl5Ivzg-z8tu96TaZN45UFCMMJ4g05fU5t-Jwok1jZE
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
subfeature_v2:
  - id: f56d26ed-050b-4fb7-b29b-8e6e994e80a2
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 1480
ht-degree: 0%

---

# [!UICONTROL Security] > [!UICONTROL Google reCAPTCHA Storefront]

>[!IMPORTANT]
>
>Bevor Google reCAPTCHA konfiguriert werden kann, müssen Sie sicherstellen, dass Ihre `PHP.ini` die folgende Einstellung enthält: `allow_url_fopen = 1`. Dies erfordert möglicherweise die Unterstützung eines Entwicklers. Siehe [PHP Settings](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/php-settings.html?lang=de) im _Installationshandbuch_.

{{config}}

Weitere Informationen zur Verwendung von Google reCAPTCHA zum Schützen Ihres Stores finden Sie unter Google [reCAPTCHA](../../systems/security-google-recaptcha.md) im _Admin Systems Guide_.

## [!UICONTROL reCAPTCHA v2 ("I am not a robot")]

![reCAPTCHA v2 („Ich bin kein Roboter„)](./assets/recaptcha-storefront-v2-not-robot.png)<!-- zoom -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--|--|--|
| [!UICONTROL Google API Website Key] | Website | Der Website-Schlüssel, der bei der Registrierung Ihres Google reCAPTCHA-Kontos erstellt wird. |
| [!UICONTROL Google API Secret Key] | Website | Der geheime Schlüssel, der Ihrem Google reCAPTCHA-Konto zugeordnet ist. |
| [!UICONTROL Size] | Website | Die Größe des Google reCAPTCHA-Felds, das angezeigt wird, wenn sich eine Kundin oder ein Kunde bei ihrem Konto anmeldet. Optionen: `Normal` (Standard) / `Compact` |
| [!UICONTROL Theme] | Website | Bestimmt den Stil des Google reCAPTCHA-Felds. Optionen: `Light Theme` (Standard) / `Dark Theme` |
| [!UICONTROL Language Code] | Shop-Ansicht | Der [Code mit zwei Zeichen](https://developers.google.com/recaptcha/docs/language) der die Sprache angibt, die für Google reCAPTCHA-Text und -Messaging verwendet wird. |

{style="table-layout:auto"}

## [!UICONTROL reCAPTCHA v2 Invisible]

![reCAPTCHA v2 Invisible](./assets/recaptcha-storefront-v2-invisible.png)<!-- zoom -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--|--|--|
| [!UICONTROL Google API Website Key] | Website | Der Website-Schlüssel, der bei der Registrierung Ihres Google reCAPTCHA-Kontos erstellt wird. |
| [!UICONTROL Google API Secret Key] | Website | Der geheime Schlüssel, der Ihrem Google reCAPTCHA-Konto zugeordnet ist. |
| [!UICONTROL Invisible Badge Position] | Website | Die Position des unsichtbaren reCAPTCHA-Badges auf jeder Seite. Optionen: `Inline` / `Bottom Right` / `Bottom Left` |
| [!UICONTROL Theme] | Global | Bestimmt den Stil des Google reCAPTCHA-Felds. Optionen: `Light Theme` (Standard) / `Dark Theme` |
| [!UICONTROL Language Code] | Shop-Ansicht | Ein [Code mit zwei Zeichen](https://developers.google.com/recaptcha/docs/language) der die Sprache angibt, die für Google reCAPTCHA-Text und -Messaging verwendet wird. |

{style="table-layout:auto"}

## [!UICONTROL reCAPTCHA v3 Invisible]

![reCAPTCHA v3 unsichtbar](./assets/recaptcha-storefront-v3-invisible.png)<!-- zoom -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--|--|--|
| [!UICONTROL Google API Website Key] | Website | Der Website-Schlüssel, der bei der Registrierung Ihres Google reCAPTCHA-Kontos erstellt wird. |
| [!UICONTROL Google API Secret Key] | Website | Der geheime Schlüssel, der Ihrem Google reCAPTCHA-Konto zugeordnet ist. |
| [!UICONTROL Minimum Score Threshold] | Global | Der Mindestwert, der eine Benutzerinteraktion als potenzielles Risiko identifiziert, wobei 1,0 eine typische Benutzerinteraktion und 0,0 wahrscheinlich ein Bot ist. Standard: `0.5` |
| [!UICONTROL Invisible Badge Position] | Website | Die Position des unsichtbaren reCAPTCHA-Badges auf jeder Seite. Optionen: `Inline` / `Bottom Right` / `Bottom Left` |
| [!UICONTROL Theme] | Website | Bestimmt den Stil des Google reCAPTCHA-Felds. Optionen: `Light Theme` (Standard) / `Dark Theme` |
| [!UICONTROL Language Code] | Shop-Ansicht | Ein [Code mit zwei Zeichen](https://developers.google.com/recaptcha/docs/language) der die Sprache angibt, die für Google reCAPTCHA-Text und -Messaging verwendet wird. |

{style="table-layout:auto"}

## [!UICONTROL reCAPTCHA Enterprise]

[!BADGE nur SaaS]{type=Positive url="https://experienceleague.adobe.com/de/docs/commerce/user-guides/product-solutions" tooltip="Gilt nur für Adobe Commerce as a Cloud Service-Projekte (von Adobe verwaltete SaaS-Infrastruktur)."}

![reCAPTCHA v3 Enterprise](./assets/recaptcha-storefront-v3-enterprise.png)<!-- zoom -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--|--|--|
| [!UICONTROL Site Key] | Website | Der Site-Schlüssel, der bei der Registrierung Ihres Google reCAPTCHA Enterprise-Kontos erstellt wird. |
| [!UICONTROL Google Cloud Project ID] | Website | Die Projekt-ID wird im **Projektinfo** im Dashboard des Projekts angezeigt. |
| [!UICONTROL Service Account JSON] | Website | Laden Sie den Service-Kontoschlüssel von der Google Cloud-Konsole herunter und fügen Sie seinen Inhalt in dieses Feld ein. |
| [!UICONTROL Minimum Score Threshold] | Website | Der Mindestwert, der eine Benutzerinteraktion als potenzielles Risiko identifiziert, wobei 1,0 eine typische Benutzerinteraktion und 0,0 wahrscheinlich ein Bot ist. Standard: `0.5` |
| [!UICONTROL Badge Position] | Website | Die Position des unsichtbaren reCAPTCHA-Badges auf jeder Seite. Optionen: `Inline` / `Bottom Right` / `Bottom Left` |
| [!UICONTROL Theme] | Website | Bestimmt den Stil des Google reCAPTCHA-Felds. Optionen: `Light Theme` (Standard) / `Dark Theme` |
| [!UICONTROL Language Code] | Shop-Ansicht | Ein [Code mit zwei Zeichen](https://developers.google.com/recaptcha/docs/language) der die Sprache angibt, die für Google reCAPTCHA-Text und -Messaging verwendet wird. Lassen Sie das Feld leer, um die Standardsprache des Browsers des Benutzers zu verwenden. |
| [!UICONTROL Validation Failure Message] | Shop-Ansicht | Eine Meldung, die angezeigt wird, wenn die Validierung fehlschlägt. |

{style="table-layout:auto"}

## [!UICONTROL reCAPTCHA Failure Messages]

![Fehlermeldungen](./assets/recaptcha-storefront-failure-messages.png)<!-- zoom -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--|--|--|
| [!UICONTROL reCAPTCHA Validation Failure Message] | Shop-Ansicht | Die Nachricht, die im Schaufenster angezeigt wird, wenn die Verifizierung fehlschlägt. Standardtext: `reCAPTCHA verification failed.` |
| [!UICONTROL reCAPTCHA Technical Failure Message] | Shop-Ansicht | Die Meldung, die in der Storefront angezeigt wird, wenn reCAPTCHA kein Verifizierungsergebnis zurückgibt. Standardtext: `Something went wrong with reCAPTCHA. Please contact the store owner.` |

{style="table-layout:auto"}

## [!UICONTROL Storefront]

![Storefront](./assets/recaptcha-storefront.png)<!-- zoom -->

>[!NOTE]
>
>Der ausgewählte reCAPTCHA-Typ muss mit dem Typ übereinstimmen, der mit dem API-Schlüssel aus Ihrem Google reCAPTCHA-Konto verknüpft ist.

>[!WARNING]
>
>Bei Verwendung von reCAPTCHA Version 3 kann ein echter Benutzer mit niedrigem Score nicht fortfahren. Bei Version 2 erhält ein echter Benutzer mit einem niedrigen Punktestand eine Herausforderung. Überlegen Sie sorgfältig, ob echte Benutzer mit einem niedrigen Score die Möglichkeit haben sollten, eine Herausforderung zu lösen (Version 2) oder blockiert zu werden (Version 3).

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--|--|--|
| [!UICONTROL Enable for Customer Login] | Website | Gibt den reCAPTCHA-Typ an, der verwendet wird, wenn sich Kundinnen [&#x200B; Kunden bei &#x200B;](../../customers/customer-sign-in.md) Konten anmelden. Optionen: <br/>**`No`**- (Standard) Validiert die Anmeldeanfrage nicht.<br />**`reCAPTCHA v2 ("I am not a robot")`** - Erfordert, dass der Benutzer das Kontrollkästchen _Ich bin kein Roboter_ aktiviert.<br />**`Invisible reCAPTCHA v2`**- Validiert das Benutzerverhalten im Hintergrund, ohne dass Interaktionen auf der Grundlage der Punktzahl erforderlich sind.<br/>**`Invisible reCAPTCHA v3`** - (Empfohlen) Validiert das Benutzerverhalten im Hintergrund basierend auf dem Interaktionswert. |
| [!UICONTROL Enable for Forgot Password] | Website | Gibt den reCAPTCHA-Typ an, der verwendet wird, wenn Kundinnen und Kunden ein [Zurücksetzen des Kennworts“ &#x200B;](../../customers/password-reset.md). Optionen: <br/>**`No`**- (Standard) Validiert nicht die Anforderung zum Zurücksetzen des Kennworts.<br />**`reCAPTCHA v2 ("I am not a robot")`** - Erfordert, dass der Benutzer das Kontrollkästchen _Ich bin kein Roboter_ aktiviert.<br />**`Invisible reCAPTCHA v2`**- Validiert das Benutzerverhalten im Hintergrund, ohne dass Interaktionen auf der Grundlage der Punktzahl erforderlich sind.<br/>**`Invisible reCAPTCHA v3`** - (Empfohlen) Validiert das Benutzerverhalten im Hintergrund basierend auf dem Interaktionswert. |
| [!UICONTROL Enable for Create New Customer Account] | Website | Gibt den reCAPTCHA-Typ an, der verwendet wird, wenn sich ein Kunde für ein [neues Konto“ &#x200B;](../../customers/account-create.md). Optionen: <br/>**`No`**- (Standard) Validiert die Kontoanfrage nicht.<br />**`reCAPTCHA v2 ("I am not a robot")`** - Erfordert, dass der Benutzer das Kontrollkästchen _Ich bin kein Roboter_ aktiviert.<br />**`Invisible reCAPTCHA v2`**- Validiert das Benutzerverhalten im Hintergrund, ohne dass Interaktionen auf der Grundlage der Punktzahl erforderlich sind.<br/>**`Invisible reCAPTCHA v3`** - (Empfohlen) Validiert das Benutzerverhalten im Hintergrund basierend auf dem Interaktionswert. |
| [!UICONTROL Enable for Edit Customer Account] | Website | Gibt den reCAPTCHA-Typ an, der verwendet wird, wenn der Kunde seine [Kontoinformationen](../../customers/account-dashboard-account-information.md) ändert. Optionen: <br/>**`No`**- (Standard) Validiert die Kontoanfrage nicht.<br />**`reCAPTCHA v2 ("I am not a robot")`** - Erfordert, dass der Benutzer das Kontrollkästchen _Ich bin kein Roboter_ aktiviert.<br />**`Invisible reCAPTCHA v2`**- Validiert das Benutzerverhalten im Hintergrund, ohne dass Interaktionen auf der Grundlage der Punktzahl erforderlich sind.<br/>**`Invisible reCAPTCHA v3`** - (Empfohlen) Validiert das Benutzerverhalten im Hintergrund basierend auf dem Interaktionswert. |
| [!UICONTROL Enable for Create New Company Account] | Website | ![Adobe Commerce B2B](../../assets/b2b.svg) (nur für Adobe Commerce B2B verfügbar) Gibt den reCAPTCHA-Typ an, der verwendet wird, wenn ein neues [Unternehmenskonto](../../b2b/account-company-create.md) erstellt wird. Optionen: <br/>**`No`**- (Standard) Validiert die Kontoanfrage nicht.<br />**`reCAPTCHA v2 ("I am not a robot")`** - Erfordert, dass der Benutzer das Kontrollkästchen _Ich bin kein Roboter_ aktiviert.<br />**`Invisible reCAPTCHA v2`**- Validiert das Benutzerverhalten im Hintergrund, ohne dass Interaktionen auf der Grundlage der Punktzahl erforderlich sind.<br/>**`Invisible reCAPTCHA v3`** - (Empfohlen) Validiert das Benutzerverhalten im Hintergrund basierend auf dem Interaktionswert. |
| [!UICONTROL Enable for Contact Us] | Website | Gibt den reCAPTCHA-Typ an, der zum Senden einer Nachricht von der Seite [Kontakt](../../getting-started/store-details.md#contact-us-form) Ihres Stores verwendet wird. Optionen: <br/>**`No`**- (Standard) Validiert die Nachrichtenanfrage nicht.<br />**`reCAPTCHA v2 ("I am not a robot")`** - Erfordert, dass der Benutzer das Kontrollkästchen _Ich bin kein Roboter_ aktiviert.<br />**`Invisible reCAPTCHA v2`**- Validiert das Benutzerverhalten im Hintergrund, ohne dass Interaktionen auf der Grundlage der Punktzahl erforderlich sind.<br/>**`Invisible reCAPTCHA v3`** - (Empfohlen) Validiert das Benutzerverhalten im Hintergrund basierend auf dem Interaktionswert. |
| [!UICONTROL Enable for Product Review] | Website | Gibt den reCAPTCHA-Typ an, der verwendet wird, wenn Kundinnen und Kunden eine [Produktüberprüfung) &#x200B;](../../merchandising-promotions/product-reviews.md). Optionen: <br/>**`No`**- (Standard) Validiert die Produktüberprüfungsanfrage nicht.<br />**`reCAPTCHA v2 ("I am not a robot")`** - Erfordert, dass der Benutzer das Kontrollkästchen _Ich bin kein Roboter_ aktiviert.<br />**`Invisible reCAPTCHA v2`**- Validiert das Benutzerverhalten im Hintergrund, ohne dass Interaktionen auf der Grundlage der Punktzahl erforderlich sind.<br/>**`Invisible reCAPTCHA v3`** - (Empfohlen) Validiert das Benutzerverhalten im Hintergrund basierend auf dem Interaktionswert. |
| [!UICONTROL Enable for Newsletter Subscription] | Website | Gibt den Typ des unsichtbaren reCAPTCHA an, der verwendet wird, wenn sich Kundinnen und Kunden für ein [Newsletter-Abonnement“ &#x200B;](../../merchandising-promotions/newsletter-subscribers.md). Optionen: <br/>**`No`**- (Standard) Validiert die Newsletter-Abonnementanfrage nicht.<br />**`reCAPTCHA v2 ("I am not a robot")`** - Erfordert, dass der Benutzer das Kontrollkästchen _Ich bin kein Roboter_ aktiviert.<br />**`Invisible reCAPTCHA v2`**- Validiert das Benutzerverhalten im Hintergrund, ohne dass Interaktionen auf der Grundlage der Punktzahl erforderlich sind.<br/>**`Invisible reCAPTCHA v3`** - (Empfohlen) Validiert das Benutzerverhalten im Hintergrund basierend auf dem Interaktionswert. |
| [!UICONTROL Enable for Gift Card] | Website | ![Adobe Commerce](../../assets/adobe-logo.svg) (nur Adobe Commerce) Gibt den reCAPTCHA-Typ an, der verwendet wird, wenn Kundinnen und Kunden einen [Geschenkkartencode](../../catalog/product-gift-card-create.md) eingeben. Optionen: <br/>**`No`**- (Standard) Validiert die Übermittlung des Geschenkkartencodes nicht.<br />**`reCAPTCHA v2 ("I am not a robot")`** - Erfordert, dass der Benutzer das Kontrollkästchen _Ich bin kein Roboter_ aktiviert.<br />**`Invisible reCAPTCHA v2`**- Validiert das Benutzerverhalten im Hintergrund, ohne dass Interaktionen basierend auf der Bewertung erforderlich sind.<br/>**`Invisible reCAPTCHA v3`** - (Empfohlen) Validiert das Benutzerverhalten im Hintergrund basierend auf dem Interaktionswert. |
| [!UICONTROL Enable for Invitation Create Account] | Website | Gibt den reCAPTCHA-Typ an, der verwendet wird, wenn Kunden einen Code zur Kontoerstellung ([) &#x200B;](../../merchandising-promotions/invitations.md). Optionen: <br/>**`No`**- (Standard) Validiert nicht die Übermittlung der Einladungs-E-Mail.<br />**`reCAPTCHA v2 ("I am not a robot")`** - Erfordert, dass der Benutzer das Kontrollkästchen _Ich bin kein Roboter_ aktiviert.<br />**`Invisible reCAPTCHA v2`**- Validiert das Benutzerverhalten im Hintergrund, ohne dass Interaktionen basierend auf der Bewertung erforderlich sind.<br/>**`Invisible reCAPTCHA v3`** - (Empfohlen) Validiert das Benutzerverhalten im Hintergrund basierend auf dem Interaktionswert. |
| [!UICONTROL Enable for Send to Friend] | Website | Gibt den reCAPTCHA-Typ an, der verwendet wird, wenn Kunden [ein Produkt freigeben](../../stores-purchase/email-a-friend.md) mit einem Freund teilen. Optionen: <br/>**`No`**- (Standard) Validiert die E-Mail-Übermittlung nicht.<br />**`reCAPTCHA v2 ("I am not a robot")`** - Erfordert, dass der Benutzer das Kontrollkästchen _Ich bin kein Roboter_ aktiviert.<br />**`Invisible reCAPTCHA v2`**- Validiert das Benutzerverhalten im Hintergrund, ohne dass Interaktionen auf der Grundlage der Punktzahl erforderlich sind.<br/>**`Invisible reCAPTCHA v3`** - (Empfohlen) Validiert das Benutzerverhalten im Hintergrund basierend auf dem Interaktionswert. |
| [!UICONTROL Enable for Wishlist Sharing] | Website | Gibt den reCAPTCHA-Typ an, der verwendet wird, wenn Kunden [eine Wunschliste freigeben](../../stores-purchase/wishlist-storefront.md#share-the-wish-list). Optionen: <br/>**`No`**- (Standard) Validiert die Nachricht und die E-Mail-Übermittlung nicht.<br />**`reCAPTCHA v2 ("I am not a robot")`** - Erfordert, dass der Benutzer das Kontrollkästchen _Ich bin kein Roboter_ aktiviert.<br />**`Invisible reCAPTCHA v2`**- Validiert das Benutzerverhalten im Hintergrund, ohne dass Interaktionen basierend auf der Bewertung erforderlich sind.<br/>**`Invisible reCAPTCHA v3`** - (Empfohlen) Validiert das Benutzerverhalten im Hintergrund basierend auf dem Interaktionswert. |
| [!UICONTROL Enable for Coupon Codes] | Website | Gibt den reCAPTCHA-Typ an, der verwendet wird, wenn Kundinnen und Kunden einen [Couponcode“ &#x200B;](../../merchandising-promotions/price-rules-cart-coupon.md). Optionen: <br/>**`No`**- (Standard) Validiert die Übermittlung des Couponcodes nicht.<br />**`reCAPTCHA v2 ("I am not a robot")`** - Erfordert, dass der Benutzer das Kontrollkästchen _Ich bin kein Roboter_ aktiviert.<br />**`Invisible reCAPTCHA v2`**- Validiert das Benutzerverhalten im Hintergrund, ohne dass Interaktionen basierend auf der Bewertung erforderlich sind.<br/>**`Invisible reCAPTCHA v3`** - (Empfohlen) Validiert das Benutzerverhalten im Hintergrund basierend auf dem Interaktionswert. |
| [!UICONTROL Enable for PayPal Payflow Pro payment form] | Website | Gibt den reCAPTCHA-Typ an, der verwendet wird, wenn Kundinnen und Kunden für einen Kauf mit [PayPal Payflow Pro](../../stores-purchase/paypal-payflow-pro.md) zahlen. Optionen: <br/>**`No`**- (Standard) Validiert nicht die Anforderung zum Zurücksetzen des Kennworts.<br />**`reCAPTCHA v2 ("I am not a robot")`** - Erfordert, dass der Benutzer das Kontrollkästchen _Ich bin kein Roboter_ aktiviert.<br />**`Invisible reCAPTCHA v2`**- Validiert das Benutzerverhalten im Hintergrund, ohne dass Interaktionen auf der Grundlage der Punktzahl erforderlich sind.<br/>**`Invisible reCAPTCHA v3`** - (Empfohlen) Validiert das Benutzerverhalten im Hintergrund basierend auf dem Interaktionswert. |

{style="table-layout:auto"}
