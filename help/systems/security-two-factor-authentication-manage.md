---
title: Zwei-Faktor-Authentifizierung verwalten
description: Erfahren Sie, wie Sie die Zwei-Faktor-Authentifizierung verwalten und die Authentifizierer für Admin-Benutzer zurücksetzen.
exl-id: 68256214-2d50-4c42-846f-306ffc305f25
role: Admin
feature: Configuration, Security, User Account
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '295'
ht-degree: 0%

---

# Zwei-Faktor-Authentifizierung verwalten

Benutzende, die sich nicht mit der Zwei-Faktor _Authentifizierung (2FA) bei Admin_ anmelden können, können versuchen, das Problem zu synchronisieren oder zu beheben. Sie können auch die mit dem Konto verknüpften Authentifizierungen zurücksetzen. Beim Zurücksetzen muss sich der Benutzer erneut anmelden und die erforderlichen Authentifizierer neu konfigurieren.

Wenn Sie Probleme haben, sich bei 2FA anzumelden, beachten Sie Folgendes:

- Einige Mobile Apps verfügen über Synchronisierungsoptionen. Diese Option verbindet die App erneut mit dem Server und synchronisiert die Zeiteinstellungen auf dem Gerät und dem Server.
- Das Widerrufen eines Geräts oder das Zurücksetzen einer Authentifizierung kann Benutzern bei der Verbindung helfen.
- Das Löschen des Web-Cache und von Cookies für die Adobe Commerce- oder Magento Open Source-Installation kann ebenfalls hilfreich sein. Authentifizierer wie Google verwenden generierte Cookies, um Zugriff und Dauer zu sparen. Löschen Sie die Cookies für Ihren spezifischen Browser und Ihre Store-Domain.
- Das Blockieren von Cookies verhindert, dass einige Authentifizierer, z. B. [!DNL Google Authenticator], den Verifizierungsprozess abschließen. Fügen Sie Ihrem Browser eine Regel hinzu, die Cookies für Ihre Adobe Commerce-Installation zulässt.

Informationen zum Zurücksetzen von Authentifizierern über die Befehlszeile und zur erweiterten Fehlerbehebung finden Sie unter [Zwei-Faktor-Authentifizierung](https://developer.adobe.com/commerce/testing/functional-testing-framework/two-factor-authentication/) in der Entwicklerdokumentation.

**_So setzen Sie Authentifizierer für ein Benutzerkonto zurück:_**

>[!NOTE]
>
>Um 2FA-Provider für andere Benutzer zurückzusetzen, müssen Sie _Administrator_ mit `All` Berechtigungen sein oder über `Custom` Berechtigungen für Ihre Rolle verfügen, wobei [!UICONTROL System] > [!UICONTROL Permissions] > [!UICONTROL Two Factor Auth] und [!UICONTROL System] > [!UICONTROL Permissions] > [!UICONTROL All Users] ausgewählt ist. Weitere Informationen finden Sie unter [Benutzerrollen](permissions-user-roles.md).

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL System]** > _[!UICONTROL Permissions]_>**[!UICONTROL All Users]**.

1. Wählen Sie den Benutzer aus und öffnen Sie das Konto im Bearbeitungsmodus.

1. Scrollen Sie nach unten zum Abschnitt _[!UICONTROL Current User Identity Verification]_&#x200B;und geben Sie Ihr Kennwort ein.

1. Klicken Sie im linken Bedienfeld auf **[!UICONTROL 2FA]**.

1. Klicken Sie im Abschnitt _[!UICONTROL Configuration reset]_&#x200B;zur Bestätigung auf **[!UICONTROL Reset]**&#x200B;und **[!UICONTROL OK]**.

   ![Benutzerkonto - 2FA aktivieren](./assets/admin-2fa-config-reset-providers.png){width="600" zoomable="yes"}

   Wenn der/die Benutzende die erforderlichen 2FA-Methoden in seinem/ihrem Konto wiederherstellen möchte, muss er/sie jede auf der Seite _Anmelden_ neu konfigurieren.

1. Klicken Sie abschließend auf **[!UICONTROL Save User]**.
