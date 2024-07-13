---
title: Zweifaktorauthentifizierung verwalten
description: Erfahren Sie, wie Sie die Authentifizierung mit zwei Faktoren verwalten und die Authentifizierer für Admin-Benutzer zurücksetzen.
exl-id: 68256214-2d50-4c42-846f-306ffc305f25
role: Admin
feature: Configuration, Security, User Account
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '295'
ht-degree: 0%

---

# Zweifaktorauthentifizierung verwalten

Benutzer, die sich nicht bei _Admin_ mit Zweifaktorauthentifizierung (2FA) anmelden können, können versuchen, das Problem zu synchronisieren oder zu beheben. Sie können auch die mit dem Konto verknüpften Authentifizierer zurücksetzen. Beim Zurücksetzen muss sich der Benutzer erneut anmelden und die erforderlichen Authentifizierer neu konfigurieren.

Wenn Sie Probleme haben, sich mit 2FA anzumelden, beachten Sie Folgendes:

- Einige mobile Apps enthalten Synchronisierungsoptionen. Diese Option verbindet die App und den Server neu und synchronisiert die Zeiteinstellungen auf Gerät und Server.
- Das Sperren eines Geräts oder das Zurücksetzen eines Authentifizierers kann Benutzern dabei helfen, eine Verbindung herzustellen.
- Das Löschen von Web-Cache und Cookies für die Installation von Adobe Commerce oder Magento Open Source kann ebenfalls hilfreich sein. Authentifizierer wie Google verwenden generierte Cookies, um Zugriff und Dauer zu sparen. Löschen Sie die Cookies für Ihren spezifischen Browser und Ihre spezifische Store-Domäne.
- Das Blockieren von Cookies verhindert, dass einige Authentifizierer, z. B. [!DNL Google Authenticator], den Verifizierungsprozess abschließen. Fügen Sie Ihrem Browser eine Regel hinzu, die Cookies für Ihre Adobe Commerce-Installation zulässt.

Informationen zum Zurücksetzen von Authentifizierern über die Befehlszeile und weiterführende Informationen zur Fehlerbehebung finden Sie unter [Zweifaktorauthentifizierung](https://developer.adobe.com/commerce/testing/functional-testing-framework/two-factor-authentication/) in der Entwicklerdokumentation.

**_Zurücksetzen der Authentifizierer für ein Benutzerkonto:_**

>[!NOTE]
>
>Um 2FA-Anbieter für andere Benutzer zurückzusetzen, müssen Sie ein _Administrator_ mit `All` -Berechtigungen sein oder `Custom` -Berechtigungen für Ihre Rolle besitzen, wobei [!UICONTROL System] > [!UICONTROL Permissions] > [!UICONTROL Two Factor Auth] und [!UICONTROL System] > [!UICONTROL Permissions] > [!UICONTROL All Users] ausgewählt sind. Weitere Informationen finden Sie unter [Benutzerrollen](permissions-user-roles.md).

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL System]** > _[!UICONTROL Permissions]_>**[!UICONTROL All Users]**.

1. Wählen Sie den Benutzer aus und öffnen Sie das Konto im Bearbeitungsmodus.

1. Scrollen Sie nach unten zum Abschnitt _[!UICONTROL Current User Identity Verification]_und geben Sie Ihr Kennwort ein.

1. Klicken Sie im linken Bereich auf **[!UICONTROL 2FA]**.

1. Klicken Sie im Abschnitt _[!UICONTROL Configuration reset]_zur Bestätigung auf **[!UICONTROL Reset]**und **[!UICONTROL OK]**.

   ![Benutzerkonto - 2FA](./assets/admin-2fa-config-reset-providers.png){width="600" zoomable="yes"} aktivieren

   Wenn der Benutzer die erforderlichen 2FA-Methoden in seinem Konto wiederherstellen möchte, muss er jede von der Seite _Anmelden_ aus neu konfigurieren.

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save User]**.
