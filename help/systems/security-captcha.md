---
title: CAPTCHA
description: Erfahren Sie, wie Sie CAPTCHA für den Administratorzugriff und verschiedene Storefront-Aktionen konfigurieren, die von registrierten Kunden initiiert wurden.
exl-id: b2867ad5-7d48-4e9f-b84e-3cf0a14ec16f
role: Admin
feature: Configuration, Security
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '942'
ht-degree: 0%

---

# CAPTCHA

Ein CAPTCHA ist ein visuelles Gerät, das sicherstellt, dass ein Mensch und nicht ein Computer (oder &quot;Bot&quot;) mit der Site interagiert. CAPTCHA ist ein Akronym für den _vollautomatisierten öffentlichen Turing-Test, der Computer und Menschen voneinander trennt_. Sie kann sowohl für den Admin-Zugriff als auch für verschiedene Storefront-Aktionen verwendet werden, die von registrierten Kunden initiiert werden. Adobe Commerce und Magento Open Source unterstützen das in diesem Thema beschriebene Standard-CAPTCHA und [Google reCAPTCHA](security-google-recaptcha.md).

Sie können das CAPTCHA so oft wie nötig neu laden, indem Sie oben rechts im Bild auf das Symbol Neu laden klicken. Das CAPTCHA ist vollständig konfigurierbar und kann jedes Mal oder erst nach einer bestimmten Anzahl fehlgeschlagener Anmeldeversuche angezeigt werden.

![Mit CAPTCHA anmelden](./assets/customer-account-login-captcha.png){width="700" zoomable="yes"}

## CAPTCHA für den Administrator konfigurieren

Für eine zusätzliche Sicherheitsstufe können Sie der Seite &quot;Admin Sign-In&quot;und &quot;Kennwort vergessen&quot;ein CAPTCHA hinzufügen. Administratoren können das angezeigte CAPTCHA neu laden, indem sie auf das Symbol _Neu laden_ ![ Neuladungssymbol](./assets/CAPTCHA-icon-reload.png) oben rechts im Bild klicken. Die Anzahl der Neuladungen ist unbegrenzt.

![Admin - Mit CAPTCHA anmelden](./assets/security-captcha-admin.png){width="300"}

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich den Wert **[!UICONTROL Advanced]** und wählen Sie **[!UICONTROL Admin]** aus.

1. Setzen Sie oben rechts **[!UICONTROL Store View]** auf `Default`.

   Wenn der [Perimeter](../getting-started/websites-stores-views.md#scope-settings) Ihrer Commerce-Installation mehrere Websites umfasst, wählen Sie die Websites aus, auf die die CAPTCHA-Konfiguration angewendet werden soll.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) im Abschnitt **[!UICONTROL CAPTCHA]** .

1. Setzen Sie **[!UICONTROL Enable CAPTCHA in Admin]** auf `Yes`. Führen Sie dann die restlichen Optionen wie folgt aus:

   ![Admin - CAPTCHA-Konfiguration](../configuration-reference/advanced/assets/admin-captcha.png){width="600" zoomable="yes"}

   - Geben Sie den Namen des für CAPTCHA-Symbole zu verwendenden **[!UICONTROL Font]** ein (Standard: `LinLibertine`).

     Um eine eigene Schriftart hinzuzufügen, muss sich die Schriftartendatei im selben Ordner wie Ihre Commerce-Installation befinden und in der Datei &quot;`config.xml`&quot; des Captcha-Moduls unter &quot;`app/code/Magento/Captcha/etc`&quot; deklariert sein.

   - Wählen Sie einen der folgenden **[!UICONTROL Forms]** aus, in denen das CAPTCHA verwendet werden soll. Um mehrere Formulare auszuwählen, halten Sie die Strg-Taste (PC) oder Befehlstaste (Mac) gedrückt.

      - `Admin Login`
      - `Admin Forgot Password`

   - Setzen Sie **[!UICONTROL Displaying Modes]** auf einen der folgenden Werte:

      - `Always` - CAPTCHA ist immer erforderlich, um sich beim Administrator anzumelden.
      - `After number of attempts to login` - Diese Option gilt nur für das Formular &quot;Admin-Anmeldung&quot;. Wenn diese Option aktiviert ist, wird das Feld _[!UICONTROL Number of Unsuccessful Attempts to Login]_angezeigt. Geben Sie die Anzahl der Anmeldeversuche ein, die Sie zulassen möchten. Der Wert 0 (null) ähnelt dem Festlegen des Anzeigemodus auf `Always`.

     Um die Anzahl der fehlgeschlagenen Anmeldeversuche zu verfolgen, wird jeder Versuch, sich unter einer E-Mail-Adresse und von einer IP-Adresse aus anzumelden, gezählt. Die maximal zulässige Anzahl von Anmeldeversuchen für dieselbe IP-Adresse beträgt 1.000. Diese Einschränkung gilt nur, wenn CAPTCHA aktiviert ist.

   - Geben Sie für &quot;**[!UICONTROL Number of Unsuccessful Attempts to Login]**&quot;an, wie oft sich der Administrator anmelden kann, bevor das CAPTCHA angezeigt wird. Wenn der Wert auf null (`0`) festgelegt ist, ist CAPTCHA immer erforderlich.

   - Geben Sie für &quot;**[!UICONTROL CAPTCHA Timeout (minutes)]**&quot;die Anzahl der Minuten ein, bevor das CAPTCHA abläuft. Wenn das CAPTCHA abläuft, muss der Administrator die Seite neu laden.

   - Geben Sie den **[!UICONTROL Number of Symbols]** ein, der im CAPTCHA angezeigt werden soll. Es können bis zu acht (`8`) Symbole verwendet werden. Geben Sie für eine variable Anzahl von Symbolen, die sich mit jedem CAPTCHA ändert, einen Bereich ein (z. B. `5-8`).

   - Geben Sie für &quot;**[!UICONTROL Symbols Used in CAPTCHA]**&quot;die Buchstaben (a-z und A-Z) und die Zahlen (0-9) ein, die zufällig im CAPTCHA angezeigt werden sollen. Symbole, die sich schwer von anderen Symbolen wie `i`, `l` oder `1` unterscheiden lassen, sind nicht im Standardsatz der CAPTCHA-Symbole enthalten.

   - Setzen Sie **[!UICONTROL Case Sensitive]** auf `Yes` , wenn Sie von Administratoren verlangen möchten, die Zeichen in Groß- oder Kleinschreibung genau so einzugeben, wie in CAPTCHA gezeigt.

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save Config]**.

## CAPTCHA für die Storefront konfigurieren

Kunden können aufgefordert werden, bei jeder Anmeldung bei ihren Konten oder nach mehreren erfolglosen Anmeldeversuchen eine CAPTCHA einzugeben. Darüber hinaus können zahlreiche Formulare, die im gesamten Storefront verwendet werden, so konfiguriert werden, dass sie von CAPTCHA überprüft werden müssen.

![CAPTCHA beim Checkout](./assets/storefront-checkout-payment-captcha.png){width="700" zoomable="yes"}

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich den Wert **[!UICONTROL Customers]** und wählen Sie **[!UICONTROL Customer Configuration]** aus.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) im Abschnitt **[!UICONTROL CAPTCHA]** .

![CAPTCHA-Konfiguration des Kunden](../configuration-reference/customers/assets/customer-configuration-captcha.png){width="600" zoomable="yes"}

1. Setzen Sie **[!UICONTROL Enable CAPTCHA on Storefront]** auf `Yes`. Führen Sie dann die restlichen Optionen wie folgt aus:

   - Geben Sie den Namen des **[!UICONTROL Font]** ein, der für die CAPTCHA-Symbole verwendet werden soll (Standard: `LinLibertine`).

     Um eine eigene Schriftart hinzuzufügen, muss sich die Schriftartdatei im selben Ordner wie Ihre Commerce-Installation befinden und in der Datei &quot;`config.xml`&quot; des CAPTCHA-Moduls deklariert sein.

   - Wählen Sie einen der folgenden **[!UICONTROL Forms]** aus, in denen das CAPTCHA verwendet werden soll. Um mehrere Formulare auszuwählen, halten Sie die Strg-Taste (PC) oder Befehlstaste (Mac) gedrückt.

      - `Applying coupon code`
      - `Checkout/Placing Order`
      - `Create user`
      - `Login`
      - `Forgot password`
      - `Contact Us`
      - `Change password`
      - `Share Wishlist Form`
      - `Payflow Pro` (siehe Artikel [Sicherheits-Patch](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/payments/paypal-payflow-pro-active-carding-activity.html) _Wissensdatenbank_ )
      - `Send to Friend Form` ![Magento Open Source](../assets/open-source.svg) (nur Magento Open Source)
      - `Add Gift Card Code` ![Adobe Commerce](../assets/adobe-logo.svg) (nur Adobe Commerce)
      - `Create company` ![Adobe Commerce B2B](../assets/b2b.svg) (nur bei Adobe Commerce B2B verfügbar)

   - Setzen Sie **[!UICONTROL Displaying Mode]** auf einen der folgenden Werte:

      - `Always` - CAPTCHA ist immer erforderlich, um auf die ausgewählten Formulare zuzugreifen.
      - `After number of attempts to login` - Geben Sie die Anzahl der Anmeldeversuche ein, bevor das CAPTCHA angezeigt wird. Der Wert 0 (null) ähnelt &quot;Immer&quot;. Wenn diese Option aktiviert ist, wird die Anzahl der fehlgeschlagenen Anmeldeversuche angezeigt. Diese Option gilt nicht für das Formular &quot;Kennwort vergessen&quot;, das bei Aktivierung immer CAPTCHA anzeigt.

   - Geben Sie für &quot;**[!UICONTROL Number of Unsuccessful Attempts to Login]**&quot;an, wie oft sich ein Kunde nicht erfolgreich anmelden kann, bevor das CAPTCHA angezeigt wird. Wenn auf null (`0`) gesetzt, wird CAPTCHA immer verwendet.

   - Geben Sie für &quot;**[!UICONTROL CAPTCHA Timeout (minutes)]**&quot;die Anzahl der Minuten ein, bevor das CAPTCHA abläuft. Wenn das CAPTCHA abläuft, muss der Kunde die Seite neu laden, um ein neues CAPTCHA zu generieren.

   - Geben Sie den **[!UICONTROL Number of Symbols]** ein, der im CAPTCHA angezeigt werden soll. Es können bis zu acht (`8`) Symbole verwendet werden. Geben Sie für eine variable Anzahl von Symbolen, die sich mit jedem CAPTCHA ändert, einen Bereich ein (z. B. `5-8`).

   - Geben Sie für &quot;**[!UICONTROL Symbols Used in CAPTCHA]**&quot;die Buchstaben (a-z und A-Z) und die Zahlen (0-9) ein, die zufällig im CAPTCHA angezeigt werden sollen. Der Standardsatz von Zeichen enthält keine ähnlichen Symbole wie `I` oder `1`. Verwenden Sie für optimale Ergebnisse Symbole, die Benutzer leicht identifizieren können.

   - Setzen Sie **[!UICONTROL Case Sensitive]** auf `Yes` , wenn Sie möchten, dass Kunden die Zeichen in Groß- oder Kleinschreibung genau wie in CAPTCHA eingeben müssen.

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save Config]**.
