---
title: Ihr Admin-Benutzerkonto
description: Erfahren Sie mehr über Ihr Admin-Konto und wie Sie sich mit einer Zwei-Faktor-Authentifizierung beim Admin anmelden können.
exl-id: ad576533-5914-49d1-8e73-3f59c55543a5
feature: Admin Workspace, User Account
source-git-commit: fff3464c9da50927bbe9773a17b0f6858360d788
workflow-type: tm+mt
source-wordcount: '958'
ht-degree: 0%

---

# Ihr Admin-Konto

Das primäre Administratorkonto wurde während der Installation eingerichtet und kann anfängliche Platzhalterinformationen oder Beispieldateninformationen enthalten. Der vorgesehene Inhaber dieses Kontos kann den Benutzernamen und das Kennwort personalisieren und den Vornamen, Nachnamen und die E-Mail-Adresse jederzeit aktualisieren. Dieses Konto, ein _Superuser_ mit allen Berechtigungen standardmäßig, erstellt in der Regel die für das Unternehmen erforderlichen Admin-Benutzerkonten.

- Informationen zum Hinzufügen oder Bearbeiten von Benutzern finden Sie unter [Erstellen eines Benutzers](../systems/permissions-users-all.md#create-a-user) .

- Informationen zu Admin- und Benutzerrollen finden Sie unter [Berechtigungen](../systems/permissions.md) und [Benutzerrollen](../systems/permissions-user-roles.md) .

{{ims-admin-note}}

## Admin-Anmeldung

Der [!DNL Commerce] _Administrator_ ist durch mehrere Ebenen von Sicherheitsmaßnahmen geschützt, um den unbefugten Zugriff auf Ihre Store-, Bestell- und Kundendaten zu verhindern. Wenn Sie sich zum ersten Mal bei _Admin_ anmelden, müssen Sie Ihren Benutzernamen und Ihr Passwort eingeben und [Zweifaktorauthentifizierung](../systems/security-two-factor-authentication.md) (2FA) einrichten.

Abhängig von der Konfiguration Ihres Stores kann es eine [CAPTCHA](../systems/security-google-recaptcha.md)-Herausforderung geben, die gelöst werden muss, z. B. die Eingabe einer Reihe von Tastaturzeichen, das Lösen eines Puzzles oder das Klicken auf eine Reihe von Bildern mit einem gemeinsamen Design. Mit diesen Tests können Sie anstelle eines automatisierten Bots als Mensch identifiziert werden.

Für zusätzliche Sicherheit können Sie festlegen, welche Teile des _Administrators_ jeder Benutzer über [Zugriffsberechtigung](../systems/permissions.md) verfügt, und auch die Anzahl der [Anmeldeversuche](../configuration-reference/advanced/admin.md) begrenzen. Standardmäßig ist das Konto nach sechs Versuchen gesperrt. Der Benutzer muss einige Minuten warten, bevor er es erneut versucht. [Gesperrte Konten](../systems/permissions-users-all.md#locked-users) können auch vom _Administrator_ zurückgesetzt werden.

>[!NOTE]
>
>Wenn Sie sich zum ersten Mal bei _Admin_ anmelden, werden Sie aufgefordert, _Datenerfassung zur Admin-Nutzung zulassen_. Weitere Informationen finden Sie unter [Datenerfassung durch Nutzung](admin.md#usage-data-collection) .

![Administratoranmeldung in](./assets/admin-login.png){width="400"}

### Schritt 1: Zweifaktorauthentifizierung einrichten

Bevor Sie sich bei _Admin_ Ihres Stores anmelden können, muss eine Zwei-Faktor-Authentifizierungslösung eingerichtet sein, die einsatzbereit ist. Weitere Informationen zum Authentifizierungsprozess, der von den einzelnen Lösungen verwendet wird, finden Sie unter [Verwenden der Zwei-Faktor-Authentifizierung](../systems/security-two-factor-authentication-use.md). Standardmäßig unterstützt [!DNL Commerce] [Google Authenticator][1].

Fragen Sie Ihren [!DNL Commerce] -Systemadministrator, welche 2FA-Lösungen für den Store unterstützt werden. Schließen Sie dann die Einrichtung Ihrer bevorzugten 2FA-Lösung gemäß den Anweisungen des Providers ab.

### Schritt 2: Anmelden bei Admin

1. Geben Sie die URL _Admin_ ein, die während der Installation von [!DNL Commerce] angegeben wurde.

   Die standardmäßige URL _Admin_ sieht in etwa wie `https://www.yourdomain.com/your-custom-admin-domain` aus.

   >[!NOTE]
   >
   >Obwohl in dieser Dokumentation in den meisten Beispielen `admin` als Basis-URL verwendet wird, wird empfohlen, eine eindeutige und schwer zu erratende [benutzerdefinierte URL](../stores-purchase/store-urls.md) für den _Administrator_ Ihres Stores zu wählen.

   Sie können ein Lesezeichen für die Seite hinzufügen oder einen Tastaturbefehl auf Ihrem Desktop speichern, um einfachen Zugriff zu erhalten.

1. Geben Sie Ihren _Admin_ **[!UICONTROL Username]** und Ihren **[!UICONTROL Password]** ein.

1. (Optional) Wenn ein CAPTCHA für Ihren Store aktiviert ist, befolgen Sie die Anweisungen auf dem Bildschirm, um das Problem zu lösen.

   Weitere Informationen finden Sie unter [CAPTCHA](../systems/security-captcha.md) und [reCAPTCHA](../systems/security-google-recaptcha.md).

1. Klicken Sie auf **[!UICONTROL Sign in]**.

   Wenn Sie sich zum ersten Mal vom Konto bei _Admin_ angemeldet haben, erhalten Sie eine E-Mail mit einem Link zu den Konfigurationsanweisungen.

### Schritt 3: Abschließen der 2FA-Konfiguration

Das folgende Beispiel zeigt, wie Sie Ihr _Admin_-Konto mit dem Google Authenticator verbinden.

1. Wenn der QR-Code angezeigt wird, verwenden Sie eine der folgenden Methoden, um den Code zu erfassen und den Google Authenticator mit Ihrem _Admin_ -Konto zu verbinden.

   ![Einrichten des Google Authenticators](./assets/admin-login-google-auth-setup.png){width="400"}

   - Erfassen von QR-Code mit einem Smartphone

     Starten Sie auf Ihrem Smartphone den Google Authenticator. Tippen Sie oben rechts in der App auf das Pluszeichen _(+)._ Tippen Sie dann unten auf dem Bildschirm auf **[!UICONTROL Scan Barcode]** und fotografieren Sie den QR-Code.

   - Erfassen von QR-Code aus dem Browser

     Wenn der Google Authenticator als Erweiterung in Ihrem Browser installiert ist, klicken Sie in der Symbolleiste auf das Symbol **Authenticator** und erfassen Sie die Seite.

   - Manuelles Eingeben von QR-Code

     Kopieren Sie die Textzeichenfolge unterhalb des QR-Codes. Starten Sie Google Authenticator entweder mit Ihrem Smartphone oder Browser und klicken Sie auf das Pluszeichen (+). Wählen Sie dann **[!UICONTROL Manual Entry]** aus. Geben Sie unter &quot;**[!UICONTROL Account]**&quot;die E-Mail-Adresse ein, die Ihrem _Admin_ -Konto zugeordnet ist, und fügen Sie die QR-Code-Zeichenfolge in das Feld **[!UICONTROL Key]** ein.

1. Um sich bei _Admin_ mit Zweifaktorauthentifizierung anzumelden, geben Sie den sechsstelligen Code, der vom Google Authenticator generiert wurde, in das Feld **[!UICONTROL Authenticator code]** ein und klicken Sie dann auf **[!UICONTROL Confirm]**.

   ![Geben Sie den Authentifizierungscode ein](./assets/admin-login-2fa-google.png){width="400"}

## Passwort zurücksetzen

Die Wiederverwendung der vier letzten Passwörter, die dem Konto zugewiesen wurden, ist nicht zulässig.

1. Geben Sie den **[!UICONTROL Email Address]** ein, der mit dem _Admin_ -Konto verknüpft ist.

   ![Vergessenes Passwort](./assets/admin-sign-in-forgot-password.png){width="400"}

1. Klicken Sie auf **[!UICONTROL Retrieve Password]**.

   Wenn ein Konto mit der E-Mail-Adresse verknüpft ist, wird eine E-Mail gesendet, um Ihr Passwort zurückzusetzen.

   >[!NOTE]
   >
   >Ein _Admin_-Kennwort muss mindestens sieben Zeichen lang sein und sowohl Buchstaben als auch Zahlen enthalten. Informationen zu den Kennwortoptionen finden Sie unter [Konfigurieren von _Admin_ Sicherheit](../systems/security-admin.md) .

## Abmelden vom Administrator

1. Klicken Sie oben rechts auf das Symbol _Konto_ (![Konto](../assets/icon-admin-user.png)).

1. Klicken Sie auf **[!UICONTROL Sign Out]**.

   ![Abmelden](./assets/admin-sign-out.png){width="700" zoomable="yes"}

Auf der Seite _[!UICONTROL Sign In]_wird eine Meldung angezeigt, dass Sie abgemeldet sind. Melden Sie sich bei_ Admin _ab, wenn Sie Ihren Computer unbeaufsichtigt lassen.

## Kontoinformationen bearbeiten

1. Klicken Sie auf das Symbol _Konto_ (![Konto-Symbol](../assets/icon-admin-user.png)).

1. Klicken Sie auf **[!UICONTROL Account Setting]**.

   ![Kontoinformationen](./assets/admin-account-information.png){width="700" zoomable="yes"}

1. Nehmen Sie die erforderlichen Änderungen an Ihren Kontoinformationen vor.

   Wenn Sie Ihre Anmeldedaten ändern, stellen Sie sicher, dass Sie sie an einem sicheren Ort speichern.

1. Geben Sie Ihr aktuelles Kontokennwort ein.

1. Klicken Sie auf **[!UICONTROL Save Account]**.

## Mehrere Administratoranmeldungen zulassen

Der Administrator bietet Zugriff auf die Verwaltung der Funktionen für Bestellungen, Kunden, Produkte, Versand und Zahlungen. Die Standardkonfiguration ist so eingestellt, dass mehrere Anmeldungen für ein Admin-Benutzerkonto als Best Practice für die Sicherheit deaktiviert werden. Sie können diese Einstellung jedoch ändern, damit Admin-Benutzer von mehreren Geräten aus angemeldet werden können, um Ihre geschäftlichen Workflows aufzunehmen.

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Navigationsbereich den Eintrag **[!UICONTROL Advanced]** und wählen Sie **[!UICONTROL Admin]**.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) im Abschnitt **[!UICONTROL Security]** .

1. Wählen Sie für **Kontofreigabe durch Administratoren** `Yes` aus.

   ![Zulassen der Kontofreigabe durch Administratoren](./assets/multiple-admin-login.png){width="700" zoomable="yes"}

1. Klicken Sie auf **[!UICONTROL Save Config]**.

## Legen Sie die Anmeldenamen der Admin-Benutzer so fest, dass zwischen Groß- und Kleinschreibung unterschieden wird

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Navigationsbereich den Eintrag **[!UICONTROL Advanced]** und wählen Sie **[!UICONTROL Admin]**.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) im Abschnitt **[!UICONTROL Security]** .

1. Setzen Sie das Feld **[!UICONTROL Login is Case Sensitive]** auf `Yes`.

1. Klicken Sie auf **[!UICONTROL Save Config]**.

[1]: https://play.google.com/store/apps/details?id=com.google.android.apps.authenticator2&amp;hl=en_US
