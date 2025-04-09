---
title: Zwei-Faktor-Authentifizierungs-Setup für Benutzerkonten
description: Erfahren Sie, wie Sie während der ersten Admin-Anmeldung eine Zwei-Faktor-Authentifizierung einrichten und Ihre Identität mit einer unterstützten Geräte-App authentifizieren.
exl-id: 1ea7f09e-4753-40fa-b9d4-376ba5d8f58f
role: Admin, User
feature: Configuration, Security, User Account
source-git-commit: dc6e5fc7c0996af30bae6374cd7c9879902b9235
workflow-type: tm+mt
source-wordcount: '750'
ht-degree: 0%

---

# Zwei-Faktor-Authentifizierungs-Setup für Benutzerkonten

Diese Anweisungen zeigen, wie Sie während Ihrer ersten Anmeldung bei Adobe Commerce oder Magento Open Source eine Zwei-Faktor-Authentifizierung einrichten und Ihre Identität mit den folgenden Programmen und Geräten authentifizieren können.

Vollständige Anweisungen finden Sie unter [Admin-Anmeldung](../getting-started/admin-signin.md).

>[!NOTE]
>
>Bei Stores mit aktivierter [!DNL Adobe Identity Management Services]-Authentifizierung (IMS) sind die native Adobe Commerce und Magento Open Source 2FA deaktiviert. Admin-Benutzende, die mit ihren Adobe-Anmeldeinformationen bei ihrer Commerce-Instanz angemeldet sind, müssen sich für viele Admin-Aufgaben nicht erneut authentifizieren. Die Authentifizierung wird von Adobe IMS durchgeführt, wenn sich der Administrator bei seiner aktuellen Sitzung anmeldet. Siehe Übersicht über die [[!DNL Adobe Identity Management Service] (IMS)-Integration](../getting-started/adobe-ims-integration-overview.md).

## [!DNL Google Authenticator]

### Schritt 1: Einrichten von [!DNL Google Authenticator]

1. Geben Sie Ihre Kontoanmeldeinformationen ein und melden Sie sich bei &quot;_&quot;_. Ein neuer Authentifizierungsbildschirm wird mit einem QR-Code angezeigt.

1. Öffnen Sie die **[!UICONTROL Google Authenticator]** App auf Ihrem Mobilgerät.

1. Click the plus sign ( **+** ) to add an entry and line up the red box with the QR code to scan with the camera on your smart phone.

1. Wenn Ihr Telefon den QR-Code erkennt und einen Eintrag hinzufügt, geben Sie diesen 6-stelligen Code in das **[!UICONTROL Authenticator code]** _Admin_ ein.

1. Klicken Sie abschließend auf **[!UICONTROL Confirm]**.

   ![Google Authenticator QR code](./assets/storefront-2fa-google-qrcode.png){width="300"}

### Schritt 2: Mit [!DNL Google Authenticator] anmelden

1. Geben Sie Ihre Kontoanmeldeinformationen ein und melden Sie sich bei Commerce (_)_.

   ![Google Authenticator - Anmeldung](./assets/storefront-2fa-google-code.png){width="300"}

1. Öffnen Sie [!DNL Google Authenticator] auf Ihrem Mobilgerät.

1. When prompted, enter the six-digit authentication code.

1. To save the authentication for future logins, select the **[!UICONTROL Trust this device, do not ask again]** checkbox.

1. Klicken Sie abschließend auf **[!UICONTROL Confirm]**.

## [!DNL Duo Security]

[!DNL Duo] offers a free trial, and charges according to the number of users that are associated with the account. Folgen Sie den [Anweisungen, um Ihr Konto einzurichten und die App herunterzuladen](https://duo.com/product/multi-factor-authentication-mfa/duo-mobile-app).

### Schritt 1: Einrichten von [!DNL Duo Security]

1. Geben Sie Ihre Kontoanmeldeinformationen ein und melden Sie sich bei &quot;_&quot;_.

1. Wenn die Seite [!DNL Duo] Setup angezeigt wird, klicken Sie auf **[!UICONTROL Get Started]** und führen Sie folgende Schritte aus:

   ![Beispiel-Storefront - Duo-Setup](./assets/storefront-2fa-duo-setup-options.png){width="300"}

1. Wählen Sie Ihre Option aus. Sie können zwischen Touch ID, Duo Mobile, Sicherheitsschlüssel oder Telefonnummer wählen. Dieses Beispiel zeigt die Option Duo Mobile oder Telefonnummer .

1. Geben Sie bei Aufforderung Ihre Telefonnummer ein und klicken Sie auf **[!UICONTROL Continue]**.

   Bestätigen Sie den Besitz, indem Sie den Kenncode an die Telefonnummer senden und überprüfen.

1. When prompted to install [!DNL Duo Mobile] for your phone type, click **[!UICONTROL I have Duo Mobile]**.

1. Open [!DNL Duo Mobile] and scan the QR code to sync the authenticator with Adobe Commerce. A checkmark appears when the activation is complete.

1. Sie können weitere Geräte hinzufügen (falls erforderlich) oder überspringen. Your setup is now complete and you can log in with Duo.

   ![Duo verification actions](./assets/storefront-2fa-duo-setup-complete.png){width="300"}

### Schritt 2: Mit [!DNL Duo Security] anmelden

Das folgende Beispiel zeigt die Optionen für `Ask me to choose an authenticator method`:

1. Geben Sie bei Aufforderung Ihre _Admin_-Anmeldedaten ein, um sich anzumelden.

   ![Duo - Anmeldung](./assets/storefront-2fa-duo-auth.png){width="300"}

1. Wählen Sie Mit Duo anmelden , um eine Push-Benachrichtigung über die Duo Mobile App zu erhalten, melden Sie sich mit der Touch-ID an oder fahren Sie mit einer anderen Option fort, die Sie während des Setups konfiguriert haben.

1. Approve the request from Duo app/ Touch ID/ Text message and you will be successfully logged in.

   ![Duo - Anmeldung](./assets/storefront-2fa-duo-success.png){width="300"}

## [!DNL Authy]

[!DNL Authy] bietet seinen Nutzern ihre App und ihren Service kostenlos an. Follow their instructions to download and set up the app for your device or browser. Weitere Informationen finden Sie in der [[!DNL Authy] Dokumentation](https://authy.com/features/setup/).

### Schritt 1: Einrichten der Autorität

1. Geben Sie Ihre Kontoanmeldeinformationen ein und melden Sie sich bei &quot;_&quot;_.

   ![[!DNL Authy] Registrierung](./assets/storefront-2fa-authy-auth.png){width="300"}

1. Wenn Sie dazu aufgefordert werden, sich bei der Autorisierung zu registrieren, führen Sie die folgenden Schritte aus:

   - Land auswählen.

   - Enter your phone number.

   - Select the **[!UICONTROL Verification method]**: `SMS` or `Call Me`

   Klicken Sie auf **[!UICONTROL Continue]**. Eine Nachricht wird über SMS-Text oder einen Anruf an Ihr Telefon gesendet.

1. Geben Sie den Verifizierungs-Code ein, den Sie erhalten, und klicken Sie auf **[!UICONTROL Verify]**.

1. Klicken Sie abschließend auf **[!UICONTROL Confirm]**.

   ![[!DNL Authy] Verifizierungs-Code](./assets/storefront-2fa-authy-verify.png){width="300"}

### Schritt 2: Mit [!DNL Authy] anmelden

1. Geben Sie Ihre Kontoanmeldeinformationen ein und melden Sie sich bei &quot;_&quot;_.

   ![[!DNL Authy] - signin](./assets/storefront-2fa-authy-access.png){width="300"}

1. Choose one of the following methods to authenticate:

   - `Use one touch` - Sendet einen Warnhinweis an Ihre [!DNL Authy] App. Akzeptieren Sie in der App den Zugriff.
   - `Use authy token` - Fordert zur Eingabe eines Codes aus Ihrer [!DNL Authy] App auf.

1. Wenn Sie Probleme haben, sich anzumelden, wählen Sie die Methode aus, die Sie verwenden möchten, um den Code zu erhalten. Geben Sie dann den Code ein, den Sie für den Zugriff auf „Admin _erhalten_.

   Die App enthält diese zusätzlichen Notfallmethoden.

   - `Send me a code via SMS` - Eine SMS-Textnachricht wird an das konfigurierte Mobilgerät gesendet.
   - `Send me a code via phone call` - Der Benutzer erhält einen Anruf mit einem Code.

   Ihr Konto ist verifiziert und wird geöffnet.

## U2F ([!DNL Yubikey] und andere Geräte)

Befolgen Sie die Anweisungen des Lösungsanbieters, um Ihr U2F-Gerät zu konfigurieren. Weitere Informationen finden Sie in der Dokumentation des Anbieters, z. B. [[!DNL YubiKey]](https://support.yubico.com/hc/en-us/articles/360013790339-Getting-Started-with-Your-YubiKey) nach [!UICONTROL Yubico].

1. Geben Sie Ihre Kontoanmeldeinformationen ein und melden Sie sich bei &quot;_&quot;_.

   ![U2F-Schlüsselzugriff](./assets/storefront-2fa-u2f.png){width="300"}

1. Press the button on the key.

   Authentication immediately triggers and opens the _Admin_.

1. Stecken Sie den **[!UICONTROL U2F key]** in einen USB-Anschluss Ihres Computers.
