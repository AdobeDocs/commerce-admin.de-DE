---
title: Google reCAPTCHA
description: Erfahren Sie, wie Sie Google reCAPTCHA für den Administratorzugriff und verschiedene Storefront-Aktionen konfigurieren, die von registrierten Kunden initiiert wurden.
exl-id: c3b53702-0882-4ac4-9cf5-39fefc90005e
role: Admin
feature: Configuration, Security
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '1046'
ht-degree: 0%

---

# Google reCAPTCHA

[Google reCAPTCHA](https://developers.google.com/recaptcha) stellt sicher, dass ein Mensch mit Ihrer Website interagiert, anstatt mit einem Computer (oder &quot;Bot&quot;). Im Gegensatz zum standardmäßigen Adobe Commerce und der Magento Open Source [CAPTCHA](security-captcha.md) bietet Google reCAPTCHA eine verbesserte Sicherheit mit verschiedenen Anzeigeoptionen und -methoden. Weitere Informationen zum Website-Traffic finden Sie im Dashboard Ihres Google reCAPTCHA-Kontos.

Google reCAPTCHA ist separat für Admin und Storefront konfiguriert.

- Für den Admin kann Google reCAPTCHA auf der Seite [Anmelden](../getting-started/admin-signin.md) und bei Anforderung eines Kennwortrücksetzens verwendet werden. Wenn die standardmäßige Commerce [CAPTCHA](security-captcha.md) ebenfalls aktiviert ist, kann Google reCAPTCHA ohne Probleme gleichzeitig verwendet werden.

- Für die Storefront kann Google reCAPTCHA verwendet werden, um sich bei einem [Kundenkonto](../customers/customer-sign-in.md) anzumelden, eine Nachricht von der Seite &quot;[Contact Us](../getting-started/store-details.md#contact-us-form)&quot;zu senden und an zahlreichen anderen Storefront-Standorten.

  ![Google reCAPTCHA - Kundenanmeldung](./assets/customer-account-login-recaptcha.png){width="700" zoomable="yes"}

Google reCAPTCHA kann auf verschiedene Weise implementiert werden:

- _reCAPTCHA v3 Invisible_ - Verwendet einen Algorithmus zum Messen von Benutzerinteraktionen und bestimmt die Wahrscheinlichkeit, dass der Benutzer basierend auf einem Ergebnis menschlich ist.

- _reCAPTCHA v2 Invisible_ - Führt eine Hintergrundüberprüfung ohne Benutzerinteraktion durch. Benutzer und Kunden werden automatisch verifiziert, müssen jedoch möglicherweise bestimmte Bilder auswählen, um eine Herausforderung abzuschließen.

- _reCAPTCHA v2 (&quot;Ich bin kein Roboter&quot;)_ — Prüft Anforderungen mit dem Kontrollkästchen _&quot;Ich bin kein Roboter&quot;_.

>[!IMPORTANT]
>
>Bevor Google reCAPTCHA konfiguriert werden kann, stellen Sie sicher, dass Ihre `PHP.ini` -Datei die folgende Einstellung enthält: `allow_url_fopen = 1`. Dies erfordert möglicherweise Hilfe von Entwicklern. Siehe [Erforderliche PHP-Einstellungen](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/php-settings.html){:target=&quot;_blank&quot;} im Installationshandbuch.

## Schritt 1: Generieren von Google reCAPTCHA-Schlüsseln

Google reCAPTCHA erfordert zur Aktivierung ein Paar API-Schlüssel. Sie können diese Schlüssel kostenlos über die reCAPTCHA-Website erhalten. Bevor Sie die Schlüssel generieren, müssen Sie den Typ von reCAPTCHA kennen, den Sie verwenden möchten.

1. Öffnen Sie die Google-reCAPTCHA-Seite und melden Sie sich bei Ihrem Konto an.

1. Geben Sie für **[!UICONTROL Label]** einen Namen ein, um die Schlüssel für die interne Referenz zu identifizieren.

   Sie benötigen einen Satz Schlüssel für jeden reCAPTCHA-Typ, der in Ihrer Adobe Commerce- oder Magento Open Source-Installation verwendet wird. Beispiel: `Commerce Invisible`

1. Wählen Sie für **[!UICONTROL reCAPTCHA type]** die Methode aus, die Sie verwenden möchten.

   - _reCAPTCHA v3 Invisible_
   - _reCAPTCHA v2 Invisible_
   - _reCAPTCHA v2 (&quot;Ich bin kein Roboter&quot;)_

1. Geben Sie für &quot;**[!UICONTROL Domain]**&quot;die Domäne Ihres Stores ein. Beispiel: mystore.com

   Wenn mehrere Stores mit unterschiedlichen Domänen vorhanden sind, geben Sie jede Domäne in einer separaten Zeile ein.

   - Fügen Sie Ihre Store-Domäne und alle Subdomänen hinzu.
   - Sie können nach Bedarf `localhost`, andere lokale VM-Domänen und Staging-Domänen zum Testen hinzufügen.

1. Aktivieren Sie das Kontrollkästchen auf &quot;**[!UICONTROL Accept the reCAPTCHA Terms of Service]**&quot;.

1. (Optional) Aktivieren Sie das Kontrollkästchen &quot;**[!UICONTROL Send alerts to owners]**&quot;, um eine Benachrichtigung zu senden, wenn Google Probleme oder verdächtigen Traffic erkennt.

1. Klicken Sie auf **[!UICONTROL Submit]** , um die Registrierung abzuschließen und Schlüssel zu erhalten.

   >[!IMPORTANT]
   >
   >Nicht alle Schlüssel gelten für alle Typen von reCAPTCHA, und eine falsche Anwendung kann zu unerwartetem Verhalten führen. Beispielsweise funktionieren Google reCAPTCHA-Schlüssel, die für reCAPTCHA v2 &quot;Ich bin kein Roboter&quot;generiert wurden, nicht mit _reCAPTCHA v2 Invisible_ und könnten Funktionen blockieren, bei denen reCAPTCHA aktiviert ist.

## Schritt 2: Konfigurieren von Google reCAPTCHA für den Administrator

1. Melden Sie sich bei Ihrem Admin-Konto an.

1. Wechseln Sie in der Admin-Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Setzen Sie oben rechts **[!UICONTROL Store View]** auf `Default Config`.

1. Erweitern Sie im linken Bereich den Eintrag **[!UICONTROL Security]** und klicken Sie auf **[!UICONTROL Google reCAPTCHA Admin Panel]**.

   >[!NOTE]
   >
   >Deaktivieren Sie das Kontrollkästchen **[!UICONTROL Use system value]** für jedes Feld, das Sie konfigurieren möchten.

1. Um _[!DNL reCAPTCHA v2 ("I am not a robot")]_zu verwenden, erweitern Sie den Abschnitt **[!UICONTROL reCAPTCHA v2 ("I am not a robot")]**und führen Sie die folgenden Schritte aus:

   - Geben Sie für &quot;**[!UICONTROL Google API Website Key]**&quot;den Website-Schlüssel ein, der für diesen reCAPTCHA-Typ erstellt wurde, als Sie Ihr Google reCAPTCHA-Konto registriert haben.

   - Geben Sie für &quot;**[!UICONTROL Google API Secret Key]**&quot;den geheimen Schlüssel ein, der Ihrem Google-reCAPTCHA-Konto zugeordnet ist.

   - Wählen Sie für &quot;**[!UICONTROL Size]**&quot;die Größe des Google reCAPTCHA-Felds aus, das angezeigt werden soll. Optionen: `Normal (default)` / `Compact`

   - Wählen Sie für &quot;**[!UICONTROL Theme]**&quot;das Design aus, das Sie verwenden möchten, um das Google-Feld &quot;reCAPTCHA&quot;zu formatieren. Optionen: `Light Theme (default)` / `Dark Theme`

   - Geben Sie für &quot;**[!UICONTROL Language Code]**&quot;den zweistelligen Code ein, um die [Sprache anzugeben, die für Google-reCAPTCHA-Text und -Messaging verwendet wird](https://developers.google.com/recaptcha/docs/language).

   ![reCAPTCHA v2 - &quot;Ich bin kein Roboter&quot;](../configuration-reference/security/assets/recaptcha-admin-v2-not-robot.png){width="600" zoomable="yes"}

1. Um _[!DNL reCAPTCHA v2 Invisible]_zu verwenden, erweitern Sie den Abschnitt **[!UICONTROL reCAPTCHA v2 Invisible]**und führen Sie die folgenden Schritte aus:

   - Geben Sie für &quot;**[!UICONTROL Google API Website Key]**&quot;den Website-Schlüssel ein, der für diesen reCAPTCHA-Typ erstellt wurde, als Sie Ihr Google reCAPTCHA-Konto registriert haben.

   - Geben Sie für &quot;**[!UICONTROL Google API Secret Key]**&quot;den geheimen Schlüssel ein, der Ihrem Google-reCAPTCHA-Konto zugeordnet ist.

   - Wählen Sie für **[!UICONTROL Invisible Badge Position]** die Badge-Position aus, die auf jeder Seite verwendet werden soll. Optionen: `Inline` / `Bottom Right` / `Bottom Left`

   - Wählen Sie für &quot;**[!UICONTROL Theme]**&quot;das Design aus, mit dem das Google-Feld reCAPTCHA formatiert werden soll. Optionen: `Light Theme (default)` / `Dark Theme`

   - Geben Sie für &quot;**[!UICONTROL Language Code]**&quot;einen Code mit zwei Zeichen ein, der die für Google-reCAPTCHA-Text und -Nachrichten verwendete Sprache [ angibt.](https://developers.google.com/recaptcha/docs/language)

   ![reCAPTCHA v2 Invisible](../configuration-reference/security/assets/recaptcha-admin-v2-invisible.png){width="600" zoomable="yes"}

1. Um _[!DNL reCAPTCHA v3 Invisible]_zu verwenden, erweitern Sie den Abschnitt **[!UICONTROL reCAPTCHA v3 Invisible]**und führen Sie die folgenden Schritte aus:

   - Geben Sie für &quot;**[!UICONTROL Google API Website Key]**&quot;den Website-Schlüssel ein, der für diesen reCAPTCHA-Typ erstellt wurde, als Sie Ihr Google reCAPTCHA-Konto registriert haben.

   - Geben Sie für &quot;**[!UICONTROL Google API Secret Key]**&quot;den geheimen Schlüssel ein, der Ihrem Google-reCAPTCHA-Konto zugeordnet ist.

   - Geben Sie den Wert **[!UICONTROL Minimum Score Threshold]** ein, um zu ermitteln, wann eine Benutzerinteraktion als potenzielles Risiko gekennzeichnet ist, wobei 1.0 eine typische Benutzerinteraktion und 0.0 wahrscheinlich ein Bot ist. Standard: `0.5`

   - Wählen Sie für **[!UICONTROL Invisible Badge Position]** die Position aus, die auf jeder Seite verwendet werden soll. Optionen: `Inline` / `Bottom Right` / `Bottom Left`

   - Wählen Sie für &quot;**[!UICONTROL Theme]**&quot;das Design aus, mit dem das Google-Feld reCAPTCHA formatiert werden soll. Optionen: `Light Theme (default)` / `Dark Theme`

   - Geben Sie für &quot;**[!UICONTROL Language Code]**&quot;einen Code mit zwei Zeichen ein, der die für Google-reCAPTCHA-Text und -Nachrichten verwendete Sprache [ angibt.](https://developers.google.com/recaptcha/docs/language)

   ![reCAPTCHA v3 Invisible](../configuration-reference/security/assets/recaptcha-admin-v3-invisible.png){width="600" zoomable="yes"}

1. Erweitern Sie **[!UICONTROL reCAPTCHA Validation Failure Messages]** und geben Sie die Meldungen ein, die im Admin angezeigt werden, wenn die Validierung fehlschlägt oder nicht abgeschlossen werden kann.

   ![reCAPTCHA-Fehlermeldungen](../configuration-reference/security/assets/recaptcha-admin-failure-messages.png){width="600" zoomable="yes"}

1. Erweitern Sie den Abschnitt **[!UICONTROL Admin Panel]** und konfigurieren Sie nach Bedarf Folgendes:

   - Setzen Sie **[!UICONTROL Enable for Login]** auf den reCAPTCHA-Typ, den Sie für die Admin-Anmeldeseite verwenden möchten.

   - Setzen Sie **[!UICONTROL Enable for Forgot Password]** auf den reCAPTCHA-Typ, den Sie für Anforderungen zum Zurücksetzen des Kennworts verwenden möchten.

   ![reCAPTCHA-Administratoroptionen](../configuration-reference/security/assets/recaptcha-admin-panel.png){width="600" zoomable="yes"}

## Schritt 3: Konfigurieren von Google reCAPTCHA für die Storefront

1. Wählen Sie im linken Bereich unter _[!UICONTROL Security]_die Option **[!UICONTROL Google reCAPTCHA Storefront]**.

1. Füllen Sie den Abschnitt für jeden reCAPTCHA-Typ aus, den Sie in der Storefront verwenden möchten.

   Weitere Informationen zu den Optionen für die einzelnen reCAPTCHA-Typen finden Sie in den Informationen unter _Schritt 2: Konfigurieren von Google reCAPTCHA für Admin_ .

1. Erweitern Sie **[!UICONTROL reCAPTCHA Validation Failure Messages]** und geben Sie die Meldungen ein, die in der Storefront angezeigt werden, wenn die Validierung fehlschlägt oder nicht abgeschlossen werden kann.

1. Erweitern Sie den Abschnitt **[!UICONTROL Storefront]** .

   >[!NOTE]
   >
   >Deaktivieren Sie das Kontrollkästchen **[!UICONTROL Use system value]** für jedes Feld, das Sie konfigurieren möchten.

1. Stellen Sie jedes Feld für den Speicherort der Storefront auf den Typ von reCAPTCHA ein, den Sie für die Verwendung konfiguriert haben.

   - [!UICONTROL Enable for Customer Login]
   - [!UICONTROL Enable for Forgot Password]
   - [!UICONTROL Enable for Create New Customer Account]
   - [!UICONTROL Enable for Edit Customer Account]
   - [!UICONTROL Enable for Create New Company Account] ![Adobe Commerce B2B](../assets/b2b.svg) (nur bei Adobe Commerce B2B verfügbar)
   - [!UICONTROL Enable for Contact Us]
   - [!UICONTROL Enable for Product Review]
   - [!UICONTROL Enable for Newsletter Subscription]
   - [!UICONTROL Enable for Gift Card] ![Adobe Commerce](../assets/adobe-logo.svg) (nur Adobe Commerce)
   - [!UICONTROL Enable for Invitation Create Account]
   - [!UICONTROL Enable for Send To Friend]
   - [!UICONTROL Enable for Checkout/Placing Order]
   - [!UICONTROL Enable for Wishlist Sharing]
   - [!UICONTROL Enable for Coupon Codes]
   - [!UICONTROL Enable for PayPal PayflowPro payment form]

   ![Konfiguration der Storefront-Optionen](../configuration-reference/security/assets/recaptcha-storefront.png){width="600" zoomable="yes"}

## Schritt 4: Konfiguration speichern

1. Wenn die Konfigurationseinstellungen abgeschlossen sind, klicken Sie auf **[!UICONTROL Save Config]**.

1. Klicken Sie in der Meldung oben im Arbeitsbereich auf **[!UICONTROL Cache Management]** und aktualisieren Sie jeden ungültigen Cache.
