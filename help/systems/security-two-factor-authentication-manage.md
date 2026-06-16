---
title: Zwei-Faktor-Authentifizierung verwalten
description: Erfahren Sie, wie Sie die Zwei-Faktor-Authentifizierung verwalten und die Authentifizierer für Admin-Benutzer zurücksetzen.
exl-id: 68256214-2d50-4c42-846f-306ffc305f25
role: Admin
feature: Configuration, Security, User Account
badgePaas: label="Nur PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Gilt nur für Adobe Commerce in Cloud-Projekten (von Adobe verwaltete PaaS-Infrastruktur) und lokale Projekte."
TQID: https://experienceleague.adobe.com/aE-36667-f0E4GSXDjZZmFUkS3wa-xTLUMbVtjwS6qk
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
subfeature_v2:
  - id: b01a71b7-d17a-42b2-a9ac-af4b8d9d2ef5
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 336
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

**_Zurücksetzen von Authentifizierern für ein Benutzerkonto:_**

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
