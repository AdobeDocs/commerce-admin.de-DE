---
title: Zwei-Faktor-Authentifizierungseinstellungen für Benutzerkonten
description: Erfahren Sie, wie Sie während der ersten Anmeldung mit dem Administrator eine Zwei-Faktor-Authentifizierung einrichten und Ihre Identität mithilfe einer unterstützten Geräte-App authentifizieren können.
exl-id: 1ea7f09e-4753-40fa-b9d4-376ba5d8f58f
role: Admin, User
feature: Configuration, Security, User Account
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '778'
ht-degree: 0%

---

# Zwei-Faktor-Authentifizierungseinstellungen für Benutzerkonten

Diese Anweisungen zeigen, wie Sie während der ersten Anmeldung bei Adobe Commerce oder Magento Open Source eine Zwei-Faktor-Authentifizierung einrichten und Ihre Identität mithilfe der folgenden Apps und Geräte authentifizieren können.

Eine vollständige Anleitung finden Sie unter [Administratoranmeldung](../getting-started/admin-signin.md).

>[!NOTE]
>
>Stores, die aktiviert wurden [!DNL Adobe Identity Management Services] (IMS)-Authentifizierung, bei der die native Adobe Commerce und Magento Open Source 2FA deaktiviert sind. Admin-Benutzer, die mit ihren Adobe-Anmeldedaten in ihrer Commerce-Instanz angemeldet sind, müssen sich nicht für viele Admin-Aufgaben erneut authentifizieren. Die Authentifizierung wird von Adobe IMS verarbeitet, wenn sich der Administrator in seiner aktuellen Sitzung anmeldet. Siehe [[!DNL Adobe Identity Management Service] (IMS) Integrationsübersicht](../getting-started/adobe-ims-integration-overview.md).

## [!DNL Google Authenticator]

### Schritt 1: Einrichten [!DNL Google Authenticator]

1. Geben Sie Ihre Kontoanmeldeinformationen ein und melden Sie sich bei der _Admin_. Ein neuer Authentifizierungsbildschirm mit QR-Code wird angezeigt.

1. Öffnen Sie die **[!UICONTROL Google Authenticator]** App auf Ihrem Mobilgerät verwenden.

1. Klicken Sie auf das Pluszeichen ( **+** ), um einen Eintrag hinzuzufügen und die rote Box mit dem QR-Code anzuordnen, der mit der Kamera auf Ihrem Smartphone gescannt werden soll.

1. Wenn Ihr Handy den QR-Code erkennt und einen Eintrag hinzufügt, geben Sie diesen 6-stelligen Code in den _Admin_ **[!UICONTROL Authenticator code]** -Feld.

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Confirm]**.

   ![Google Authenticator QR-Code](./assets/storefront-2fa-google-qrcode.png){width="300"}

### Schritt 2: Anmelden mit [!DNL Google Authenticator]

1. Geben Sie Ihre Kontoanmeldeinformationen ein und melden Sie sich beim Commerce an _Admin_.

   ![Google Authenticator - signation](./assets/storefront-2fa-google-code.png){width="300"}

1. Öffnen [!DNL Google Authenticator] auf Ihrem Mobilgerät.

1. Geben Sie bei Aufforderung den sechsstelligen Authentifizierungscode ein.

1. Um die Authentifizierung für künftige Anmeldungen zu speichern, wählen Sie die **[!UICONTROL Trust this device, do not ask again]** aktivieren.

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Confirm]**.

## [!DNL Duo Security]

[!DNL Duo] bietet eine kostenlose Testversion und Gebühren entsprechend der Anzahl der Benutzer, die mit dem Konto verknüpft sind. Folgen Sie den [Anweisungen zum Einrichten Ihres Kontos und Herunterladen der App](https://duo.com/product/multi-factor-authentication-mfa/duo-mobile-app).

### Schritt 1: Einrichten [!DNL Duo Security]

1. Geben Sie Ihre Kontoanmeldeinformationen ein und melden Sie sich bei der _Admin_.

1. Wenn die Variable [!DNL Duo] Die Seite Einrichtung wird angezeigt, klicken Sie auf **[!UICONTROL Start setup]** und gehen Sie wie folgt vor:

   ![Beispiel-Storefront - Duo-Setup](./assets/storefront-2fa-duo-user1.png){width="300"}

1. Wählen Sie Ihr Gerät aus.

1. Geben Sie bei Aufforderung Ihre Telefonnummer ein und klicken Sie auf **[!UICONTROL Continue]**.

   In diesem Beispiel wird Ihre Telefonnummer angefordert, da wir ein Mobilgerät verwenden.

1. Bei Aufforderung zur Installation [!DNL Duo Mobile] Klicken Sie für Ihren Telefontyp auf **[!UICONTROL I have Duo Mobile]**.

1. Öffnen [!DNL Duo Mobile] und scannen Sie den QR-Code, um den Authentifizierer mit Adobe Commerce zu synchronisieren. Nach Abschluss der Aktivierung wird ein Häkchen angezeigt.

1. Um die Einstellungen für das Gerät zu konfigurieren, wählen Sie die Aktion aus, die bei der Anmeldung durchgeführt werden soll.

   - `Ask me to choose an authenticator method` - Ermöglicht dem Benutzer die Auswahl bei der Anmeldung und Authentifizierung bei der _Admin_.
   - `Automatically send this device a Duo Push` — Sendet eine Nachricht an Ihr Gerät, um den Zugriff zu akzeptieren oder zu verweigern.
   - `Automatically call this device` — Ruft ein Passwort auf, das für den Zugriff eingegeben werden kann, und stellt es bereit.

   ![Duo - Verifizierungsmaßnahmen](./assets/storefront-2fa-duo-user7.png){width="300"}

### Schritt 2: Anmelden mit [!DNL Duo Security]

Das folgende Beispiel zeigt die Optionen für `Ask me to choose an authenticator method`:

1. Geben Sie bei Aufforderung Ihre _Admin_ Anmeldedaten zur Anmeldung.

   ![Duo - Anmeldung](./assets/storefront-2fa-duo-auth.png){width="300"}

1. Wählen Sie die Methode aus, die Sie für die Authentifizierung verwenden möchten:

   - `Send Me a Push` - Klicken Sie auf , um eine Push-Benachrichtigung zu erhalten. [!DNL Duo Mobile]. Akzeptieren zur Authentifizierung.
   - `Call Me` — Klicken Sie auf diese Option, erhalten Sie einen Aufruf mit einem Code und geben Sie den Pass-Code ein.
   - `Enter a Passcode` — Klicken Sie auf diese Option, um einen Pass-Code zu erhalten und einzugeben.

1. Schließen Sie den Push- oder Code ab, um sich vollständig bei der _Admin_.

## [!DNL Authy]

[!DNL Authy] bietet Benutzern ihre App und ihren Service kostenlos an. Befolgen Sie die Anweisungen zum Herunterladen und Einrichten der App für Ihr Gerät oder Ihren Browser. Weitere Informationen finden Sie unter [[!DNL Authy] Dokumentation](https://authy.com/features/setup/).

### Schritt 1: Einrichten der Autoreninstanz

1. Geben Sie Ihre Kontoanmeldeinformationen ein und melden Sie sich bei der _Admin_.

   ![[!DNL Authy] registrierung](./assets/storefront-2fa-authy-auth.png){width="300"}

1. Wenn Sie dazu aufgefordert werden, sich bei der Autoreninstanz zu registrieren, gehen Sie wie folgt vor:

   - Wählen Sie Ihr Land aus.

   - Geben Sie Ihre Telefonnummer ein.

   - Wählen Sie die **[!UICONTROL Verification method]**: `SMS` oder `Call Me`

   Klicken **[!UICONTROL Continue]**. Eine Nachricht wird über SMS-Text oder einen Anruf an Ihr Telefon gesendet.

1. Geben Sie den erhaltenen Verifizierungscode ein und klicken Sie auf **[!UICONTROL Verify]**.

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Confirm]**.

   ![[!DNL Authy] Verifizierungscode](./assets/storefront-2fa-authy-verify.png){width="300"}

### Schritt 2: Anmelden mit [!DNL Authy]

1. Geben Sie Ihre Kontoanmeldeinformationen ein und melden Sie sich bei der _Admin_.

   ![[!DNL Authy] - Anmeldung](./assets/storefront-2fa-authy-access.png){width="300"}

1. Wählen Sie eine der folgenden Authentifizierungsmethoden aus:

   - `Use one touch` — Sendet eine Warnung an Ihre [!DNL Authy] App. Akzeptieren Sie in der App den Zugriff.
   - `Use authy token` — Aufforderung zur Eingabe eines Codes aus Ihrem [!DNL Authy] App.

1. Wenn Sie Schwierigkeiten haben, sich anzumelden, wählen Sie die Methode aus, die Sie für den Empfang des Codes verwenden möchten. Geben Sie dann den Code ein, den Sie erhalten, um auf die _Admin_.

   Das Programm enthält diese zusätzlichen Notfallmethoden.

   - `Send me a code via SMS` — Eine SMS-Textnachricht wird an das konfigurierte Mobilgerät gesendet.
   - `Send me a code via phone call` — Der Benutzer erhält einen Telefonanruf mit Code.

   Ihr Konto wird geprüft und geöffnet.

## U2F[!DNL Yubikey] und andere Geräte)

Befolgen Sie die Anweisungen des Lösungsanbieters, um Ihr U2F-Gerät zu konfigurieren. Weitere Informationen finden Sie in der Dokumentation des Anbieters, z. B. [[!DNL YubiKey]](https://support.yubico.com/hc/en-us/articles/360013790339-Getting-Started-with-Your-YubiKey) von [!UICONTROL Yubico].

1. Geben Sie Ihre Kontoanmeldeinformationen ein und melden Sie sich bei der _Admin_.

   ![U2F-Schlüsselzugriff](./assets/storefront-2fa-u2f.png){width="300"}

1. Drücken Sie die Taste auf der Taste.

   Die Authentifizierung erfolgt sofort Trigger und öffnet die _Admin_.

1. Fügen Sie die **[!UICONTROL U2F key]** in einen USB-Anschluss auf Ihrem Computer.
