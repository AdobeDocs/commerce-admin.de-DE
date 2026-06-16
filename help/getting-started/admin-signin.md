---
title: Ihr Admin-Benutzerkonto
description: Erfahren Sie mehr über Ihr Admin-Konto und wie Sie mit der Zwei-Faktor-Authentifizierung sich beim Admin anmelden können.
exl-id: ad576533-5914-49d1-8e73-3f59c55543a5
feature: Admin Workspace, User Account
TQID: https://experienceleague.adobe.com/p40Sr3TPKp2QrTiMdwzmGL04lO6f8xK8fCLcbOebV7M
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: b5f00040-57a0-4a6d-a39e-383b1936c2c9id: ba9e5be9-7de1-4f71-a5d2-baead0e425eeid: bd989d82-1e15-4534-88db-f1f51dd77ffaid: c1256247-af4b-46d8-9dca-0c654ecfa157id: dac87252-6066-4d6e-a9d2-f6d84c323de7
subfeature_v2: id: b01a71b7-d17a-42b2-a9ac-af4b8d9d2ef5
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: d095671a-1355-40aa-8b5f-06c33c68080bid: d3cdead0-685a-4489-9250-4bb709942f66id: eddd9b14-83bd-4ff4-9072-54a4a484abb7id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 1214
ht-degree: 0%

---

# Ihr Admin-Konto

Das primäre Admin-Konto wurde ursprünglich während der Installation eingerichtet und kann anfängliche Platzhalterinformationen oder Beispieldateninformationen enthalten. Der festgelegte Besitzer dieses Kontos kann den Benutzernamen und das Kennwort personalisieren und den Vornamen, Nachnamen und die E-Mail-Adresse jederzeit aktualisieren. Dieses Konto, _Superuser_ mit standardmäßig allen Berechtigungen, erstellt in der Regel die für das Unternehmen erforderlichen Admin-Benutzerkonten.

- Informationen [ Hinzufügen oder Bearbeiten von Benutzern finden ](../systems/permissions-users-all.md#create-a-user) unter „Benutzer erstellen“.

- Informationen [ Admin](../systems/permissions.md) und Benutzerrollen finden [ unter ](../systems/permissions-user-roles.md)Berechtigungen“.

{{ims-admin-note}}

## Admin-Anmeldung

Der [!DNL Commerce] _Admin_ ist durch mehrere Sicherheitsmaßnahmen geschützt, um einen unbefugten Zugriff auf Ihre Store-, Auftrags- und Kundendaten zu verhindern. Bei der ersten Anmeldung bei _Admin_ müssen Sie Ihren Benutzernamen und Ihr Kennwort eingeben und die [Zwei-Faktor-Authentifizierung](../systems/security-two-factor-authentication.md) (2FA) einrichten.

Je nach Konfiguration Ihres Stores kann eine [CAPTCHA](../systems/security-google-recaptcha.md)-Herausforderung gelöst werden, z. B. das Eingeben einer Reihe von Tastaturzeichen, das Lösen eines Puzzles oder das Klicken auf eine Reihe von Bildern mit einem gemeinsamen Thema. Diese Tests sind so konzipiert, dass Sie als Mensch identifiziert werden, und nicht als automatisierter Bot.

Aus Sicherheitsgründen können Sie festlegen, auf welche Teile des _Admin_ jeder Benutzer [Berechtigung](../systems/permissions.md) zugreifen kann, und auch die Anzahl der [Anmeldeversuche](../configuration-reference/advanced/admin.md) begrenzen. Standardmäßig wird das Konto nach sechs Versuchen gesperrt und der/die Benutzende muss einige Minuten warten, bevor er/sie es erneut versucht. [Gesperrte Konten](../systems/permissions-users-all.md#locked-users) können auch über die _Admin_ zurückgesetzt werden.

>[!NOTE]
>
>Wenn Sie sich zum ersten Mal bei _Admin_ anmelden, werden Sie aufgefordert, die Datenerfassung _Admin-Nutzung zulassen_. Weitere Informationen [ Sie unter ](admin.md#usage-data-collection)Nutzungsdatenerfassung“.

![Admin-Anmeldung](./assets/admin-login.png){width="400"}

### Schritt 1: Einrichten der Zwei-Faktor-Authentifizierung

Bevor Sie sich beim _Administrator_ Ihres Geschäfts anmelden können, müssen Sie eine Zwei-Faktor-Authentifizierungslösung eingerichtet haben, die einsatzbereit ist. Weitere Informationen zum Authentifizierungsprozess, der von den einzelnen Lösungen verwendet wird, finden Sie unter [Verwenden der Zwei-Faktor-Authentifizierung](../systems/security-two-factor-authentication-use.md). Standardmäßig unterstützt [!DNL Commerce] [Google Authenticator](https://play.google.com/store/apps/details?id=com.google.android.apps.authenticator2&hl=en_US).

Fragen Sie Ihren [!DNL Commerce] Systemadministrator, welche 2FA-Lösungen für den Store unterstützt werden. Schließen Sie dann die Einrichtung Ihrer bevorzugten 2FA-Lösung gemäß den Anweisungen des Anbieters ab.

### Schritt 2: Beim Administrator anmelden

1. Geben Sie die _Admin_-URL ein, die während der [!DNL Commerce]-Installation angegeben wurde.

   Die standardmäßige _Admin_-URL sieht in etwa wie `https://www.yourdomain.com/your-custom-admin-domain` aus.

   >[!NOTE]
   >
   >Obwohl diese Dokumentation in den meisten Beispielen `admin` als Basis-URL verwendet, wird empfohlen, eine eindeutige und schwer zu erratende [benutzerdefinierte URL](../stores-purchase/store-urls.md) für den _Administrator_ Ihres Stores auszuwählen.

   Sie können ein Lesezeichen für die Seite hinzufügen oder eine Verknüpfung auf Ihrem Desktop speichern, um den Zugriff zu erleichtern.

1. Geben Sie Ihre _Admin_-**[!UICONTROL Username]** und -**[!UICONTROL Password]** ein.

1. (Optional) Wenn ein CAPTCHA für Ihren Store aktiviert ist, befolgen Sie die Anweisungen auf dem Bildschirm, um die Herausforderung zu lösen.

   Weitere Informationen finden Sie unter [CAPTCHA](../systems/security-captcha.md) und [reCAPTCHA](../systems/security-google-recaptcha.md).

1. Klicken Sie auf **[!UICONTROL Sign in]**.

   Wenn Sie sich zum ersten Mal über das Konto bei _Admin_ anmelden, sollten Sie eine E-Mail mit einem Link zu Konfigurationsanweisungen erhalten.

### Schritt 3: Abschließen der 2FA-Konfiguration

Das folgende Beispiel zeigt, wie Sie Ihr _Admin“-_ mit Google Authenticator koppeln.

1. Wenn der QR-Code angezeigt wird, verwenden Sie eine der folgenden Methoden, um den Code zu erfassen und Google Authenticator mit Ihrem _Admin_-Konto zu verbinden.

   ![Einrichten von Google Authenticator](./assets/admin-login-google-auth-setup.png){width="400"}

   - Erfassen von QR-Code mit einem Smartphone

     Starten Sie auf Ihrem Smartphone Google Authenticator. Tippen Sie auf _Pluszeichen_ (+) in der oberen rechten Ecke der App. Tippen Sie dann unten auf dem Bildschirm auf **[!UICONTROL Scan Barcode]** und machen Sie ein Foto des QR-Codes.

   - QR-Code vom Browser erfassen

     Wenn Google Authenticator als Erweiterung in Ihrem Browser installiert ist, klicken Sie auf das Symbol **Authenticator** in der Symbolleiste und erfassen Sie die Seite.

   - QR-Code manuell eingeben

     Kopieren Sie die Zeichenfolge unter den QR-Code. Starten Sie Google Authenticator entweder mit Ihrem Smartphone oder Browser und klicken Sie auf das Pluszeichen (+). Wählen Sie dann **[!UICONTROL Manual Entry]**. Geben Sie unter **[!UICONTROL Account]** die E-Mail-Adresse ein, die mit Ihrem _Admin_-Konto verknüpft ist, und fügen Sie die QR-Code-Zeichenfolge in das Feld **[!UICONTROL Key]** ein.

1. Um sich bei _Admin_ mit Zwei-Faktor-Authentifizierung anzumelden, geben Sie den sechsstelligen Code, der von Google Authenticator generiert wurde, in das Feld **[!UICONTROL Authenticator code]** ein und klicken Sie dann auf **[!UICONTROL Confirm]**.

   ![Geben Sie den Authentifizierungs-Code ein](./assets/admin-login-2fa-google.png){width="400"}

## Passwort zurücksetzen

Die Wiederverwendung der letzten vier Kennwörter, die dem Konto zugewiesen wurden, ist nicht zulässig.

1. Geben Sie die **[!UICONTROL Email Address]** ein, die mit dem Konto _admin_ verknüpft ist.

   ![Kennwort vergessen](./assets/admin-sign-in-forgot-password.png){width="400"}

1. Klicken Sie auf **[!UICONTROL Retrieve Password]**.

   Wenn der E-Mail-Adresse ein Konto zugeordnet ist, wird eine E-Mail gesendet, um Ihr Kennwort zurückzusetzen.

   >[!NOTE]
   >
   >Ein _Admin_-Kennwort muss (standardmäßig) mindestens sieben Zeichen lang sein und sowohl Buchstaben als auch Zahlen enthalten. Die minimale Kennwortlänge kann in den Admin-Sicherheitseinstellungen konfiguriert werden. Informationen [ Kennwortoptionen finden Sie unter _Admin_-](../systems/security-admin.md) konfigurieren.

## Melden Sie sich bei Admin ab

1. Klicken Sie oben rechts auf das Symbol _Konto_ (![Konto](../assets/icon-admin-user.png)).

1. Klicken Sie auf **[!UICONTROL Sign Out]**.

   ![Abmelden](./assets/admin-sign-out.png){width="700" zoomable="yes"}

Auf der Seite _[!UICONTROL Sign In]_wird eine Meldung angezeigt, dass Sie abgemeldet sind. Melden Sie sich von der_ Admin _ab, wenn Sie Ihren Computer unbeaufsichtigt lassen.

## Kontoinformationen bearbeiten

1. Klicken Sie auf _Symbol_ Konto![ (](../assets/icon-admin-user.png)).

1. Klicken Sie auf **[!UICONTROL Account Setting]**.

   ![Kontoinformationen](./assets/admin-account-information.png){width="700" zoomable="yes"}

1. Nehmen Sie die erforderlichen Änderungen an Ihren Kontoinformationen vor.

   Wenn Sie Ihre Anmeldedaten ändern, stellen Sie sicher, dass Sie sie an einem sicheren Ort speichern.

1. Geben Sie Ihr aktuelles Kontokennwort ein.

1. Klicken Sie auf **[!UICONTROL Save Account]**.

## Mehrere Admin-Anmeldungen zulassen

Der Administrator bietet Zugriff zur Verwaltung der Funktionen für Bestellungen, Kunden, Produkte, Versand und Zahlungen. Als Best Practice für die Sicherheit wird in der Standardkonfiguration festgelegt, dass mehrere Anmeldungen für ein Admin-Benutzerkonto nicht zulässig sind. Sie können diese Einstellung jedoch ändern, damit sich Admin-Benutzer von mehreren Geräten aus anmelden können, um Ihre Unternehmens-Workflows zu unterstützen.

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Navigationsbereich **[!UICONTROL Advanced]** und wählen Sie **[!UICONTROL Admin]**.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Security]** .

1. Wählen Sie **Admin-Kontofreigabe** die Option `Yes` aus.

   ![Admin-Kontofreigabe zulassen](./assets/multiple-admin-login.png){width="700" zoomable="yes"}

1. Klicken Sie auf **[!UICONTROL Save Config]**.

## Admin-Benutzernamen unter Berücksichtigung der Groß-/Kleinschreibung festlegen

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Navigationsbereich **[!UICONTROL Advanced]** und wählen Sie **[!UICONTROL Admin]**.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Security]** .

1. Legen Sie das Feld **[!UICONTROL Login is Case Sensitive]** auf `Yes` fest.

1. Klicken Sie auf **[!UICONTROL Save Config]**.


## Gewährleistung eines sicheren Zugriffs auf den Administrator

Um die Sicherheit Ihres Administrators zu gewährleisten, führen Sie regelmäßige Audits von Benutzern und Rollen mit Administratorzugriff durch.

Darüber hinaus sollten Sie [die Konfiguration der Admin-Basis](https://experienceleague.adobe.com/en/docs/commerce-admin/config/advanced/admin#admin-base-url)URL aktualisieren, um den standardmäßigen `/admin`-Endpunkt in einen benutzerdefinierten Pfad zu ändern. Die Konfiguration eines benutzerdefinierten Pfads bietet die folgenden Sicherheitsvorteile:

**Erweiterte Sicherheit**: Der standardmäßige „Admin“-Pfad ist weithin bekannt und wird oft von böswilligen Akteuren verwendet, die Brute-Force-Angriffe durchführen. Durch die Änderung in einen eindeutigen, benutzerdefinierten Wert verringern Sie das Risiko nicht autorisierter Zugriffsversuche erheblich.

**Geringere Sicherheitslücken**: Automatisierte Bots suchen häufig nach allgemeinen Pfaden wie „admin“, um Sicherheitslücken auszunutzen. Ein benutzerdefinierter Pfad erschwert es diesen Bots, Ihre Admin-Anmeldeseite zu finden, wodurch die Wahrscheinlichkeit von Angriffen reduziert wird.

**Verbesserter Datenschutz**: Ein benutzerdefinierter Admin-Pfad fügt eine zusätzliche Ebene der Unklarheit hinzu, wodurch es potenziellen Angreifern erschwert wird, Ihre Admin-Anmeldeseite zu identifizieren und anzusprechen.

**Einhaltung von Best Practices**: Die Befolgung von Best Practices für die Sicherheit, wie z. B. die Anpassung des Administratorpfads, zeigt einen proaktiven Ansatz zum Schutz Ihrer E-Commerce-Site und Kundendaten.

>[!NOTE]
>
>Wenn ein Verstoß vermutet wird, entfernen Sie alle unbekannten Admin-Benutzer und setzen Sie alle Admin-Kennwörter zurück. Überprüfen Sie [Sicherheits-Aktionsplan](https://experienceleague.adobe.com/en/docs/commerce-admin/systems/security/security) auf weitere Schritte.
