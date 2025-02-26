---
title: A [!DNL Commerce] Konto freigeben
description: Erfahren Sie, wie Sie anderen Kontoinhabern  [!DNL Commerce]  eingeschränkten Zugriff auf Ihr  [!DNL Commerce]  gewähren.
exl-id: adc4fed4-89f4-4b0c-811c-fcf6f94dbc22
feature: User Account
source-git-commit: e7d76a7fa9ba8d8b8ee1ce122f7ca61e2aa317c6
workflow-type: tm+mt
source-wordcount: '836'
ht-degree: 0%

---

# [!DNL Commerce] freigeben

Ihr [!DNL Commerce]-Konto enthält Informationen, die Sie vertrauenswürdigen Mitarbeitern und Dienstleistern zur Verfügung stellen können, die Sie bei der Verwaltung Ihrer Site unterstützen. Als primärer Kontoinhaber sind Sie berechtigt, anderen [!DNL Commerce] Kontoinhabern eingeschränkten Zugriff zu gewähren. Freigegebener Zugriff kann widerrufen, aber nicht von einem Benutzer auf einen anderen übertragen werden.

Das [!DNL Commerce] Support-Team hat keinen Zugriff auf das Konto und kann keinen gemeinsamen Zugriff für Sie einrichten. Nur der Inhaber des primären Kontos mit entsprechenden Berechtigungen kann freigegebenen Zugriff einrichten. Wenn Sie den Kontozugriff freigeben, bleiben alle sensiblen Informationen, wie z. B. Ihr Rechnungsverlauf oder Kreditkarteninformationen, geschützt und stehen anderen Benutzern nie zur Verfügung.

>[!NOTE]
>
>Alle Aktionen, die von Benutzern mit gemeinsamem Zugriff durchgeführt werden, liegen in der alleinigen Verantwortung des Inhabers des primären Kontos. Adobe übernimmt keine Verantwortung für Aktionen von Benutzenden, die gemeinsamen Zugriff auf Ihr Konto haben.

![Freigegebene Zugriffseinstellungen](./assets/shared-access.png){width="600" zoomable="yes"}

## Freigegebenes Konto einrichten

1. Bevor Sie beginnen, rufen Sie die folgenden Informationen vom [!DNL Commerce] Konto des **neuen Empfängers mit gemeinsamem Zugriff** ab:

   - Der Benutzer muss sich bereits unter account.adobe.com für ein Konto registriert haben und über account.magento.com angemeldet sein. Weitere [ finden Sie unter „Erstellen ](https://experienceleague.adobe.com/en/docs/commerce-admin/start/commerce-account/commerce-account-create#create-a-commerce-account) Commerce-Kontos“.
   - Der `MAGE ID/Account ID (MAG00XXXXXXX)` wird in der linken oberen Ecke der Registerkarte _[!UICONTROL Magento]_direkt über dem Link **Abmelden**angezeigt.
   - Die `Email`, die mit dem Konto verknüpft ist.

1. Melden Sie sich bei Ihrem [[!DNL Commerce] Konto](commerce-account-create.md) an.

1. Klicken Sie im linken Navigationsbereich auf **[!UICONTROL Shared Access]**.

1. Klicken Sie auf **[!UICONTROL Add New User]**.

   ![Neuen Benutzer hinzufügen](./assets/shared-access-add.png){width="600" zoomable="yes"}

1. Gehen Sie unter [!UICONTROL _New User Information]_ wie folgt vor:

   - Geben Sie die **[!UICONTROL Account ID]** aus dem [!DNL Commerce] Konto des neuen Benutzers ein.
   - Geben Sie die **[!UICONTROL Email]**-Adresse ein, die mit dem [!DNL Commerce] des neuen Benutzers verknüpft ist.

   ![Neue Benutzerinformationen](./assets/shared-new-user.png){width="600"}

1. Gehen Sie unter _[!UICONTROL Shared Information]_wie folgt vor:

   - Um das freigegebene Konto zu identifizieren, geben Sie einen **[!UICONTROL Share Name]** ein. Dieser Name dient als interne Referenz und ist nur für Sie und die Person sichtbar, für die Sie Ihr Konto freigeben.

     Es empfiehlt sich, den Namen Ihres Unternehmens als [!UICONTROL Share Name] zu verwenden. Verwenden Sie keinen Namen, der mit `CLOUD SHARED ACCESS FROM MAG XYX` beginnt.
   - Wenn Sie Ihre persönlichen Kontaktinformationen für den neuen Benutzer freigeben möchten, geben Sie **[!UICONTROL Your Email]** und **[!UICONTROL Your Phone]** ein.

1. Aktivieren Sie unter _[!UICONTROL Grant Account Permissions]_das Kontrollkästchen jedes [!DNL Commerce] Produkts und Services, das Sie freigeben möchten.

   ![Erteilen Sie die Kontoberechtigungen](./assets/shared-permissions.png){width="600"}

1. Klicken Sie auf **[!UICONTROL Create Shared Access]**.

   Die Informationen zum neuen Benutzer werden im Abschnitt _[!UICONTROL Manage Permissions]_der Seite Freigegebener Zugriff angezeigt, und dem neuen Benutzer wird eine E-Mail-Einladung mit Anweisungen für den Zugriff auf das freigegebene Konto gesendet.

   ![Berechtigungen für freigegebenen Zugriff verwalten](./assets/shared-manage-permissions.png){width="600" zoomable="yes"}

>[!NOTE]
>
>Es ist nicht erforderlich, den Zugriff auf die _[!UICONTROL Security Tool]_freizugeben. Jeder Benutzer mit einer MAGE-ID kann das Sicherheits-Scan-Tool mit seinem eigenen Konto einrichten. Sie benötigen lediglich die erforderlichen Berechtigungen, um Änderungen an der Site vorzunehmen und die Eigentümerschaft der Domain mit einer der [erforderlichen Methoden](https://experienceleague.adobe.com/en/docs/commerce-admin/systems/security/security-scan) zu überprüfen.

## Zugreifen auf ein freigegebenes Konto

Die folgenden Anweisungen sind aus der Sicht eines freigegebenen Benutzers geschrieben, der eine Einladung zu einem freigegebenen Konto erhält.

1. Wenn Sie eine Einladung zu einem freigegebenen Konto erhalten, befolgen Sie die Anweisungen in der E-Mail, um sich bei Ihrem eigenen [!DNL Commerce]-Konto anzumelden.

   Das linke Navigationsfenster Ihres Kontos weist eine neue Registerkarte _[!UICONTROL Shared with me]_auf. Das_[!UICONTROL Switch Accounts]_-Steuerelement in der oberen rechten Ecke verfügt über Optionen zum `My Account` und den Namen des freigegebenen Kontos.

   ![Für mich freigegeben](./assets/shared-with-me.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >   Wenn das _[!UICONTROL Switch Accounts]_nicht angezeigt wird, wenden Sie sich an den primären Kontoinhaber und bestätigen Sie, dass er Ihre richtigen [Kontoinformationen](#set-up-a-shared-account) eingegeben hat.


1. Um Zugriff auf das freigegebene Konto zu erhalten, legen Sie **[!UICONTROL Switch Accounts]** auf den Namen des freigegebenen Kontos fest.

   ![Wechseln Sie zum freigegebenen Konto](./assets/shared-switch.png){width="600" zoomable="yes"}

   Das freigegebene Konto zeigt eine Willkommensnachricht und Kontaktinformationen an. Der linke Navigationsbereich enthält nur die Elemente, die Sie verwenden dürfen.

1. Um das freigegebene Konto mit dem Hilfezentrum zu verbinden, klicken Sie im linken Navigationsbereich des freigegebenen Kontos auf **[!UICONTROL Support]** .

   ![Support](./assets/shared-support.png){width="600" zoomable="yes"}

   Sie können das [Adobe Commerce Help Center](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/overview) über das freigegebene Konto nach Artikeln und Informationen zur Fehlerbehebung suchen, Patches für bekannte Probleme suchen und Support-Tickets erstellen.

   >[!NOTE]
   >
   >Nach Erhalt des freigegebenen Zugriffs muss sich der Benutzer bei seinem [[!DNL Commerce] Konto](https://account.magento.com/customer/account/login) anmelden, zu _Freigegebener Zugriff_ navigieren und auf die Registerkarte **[!UICONTROL Support]** klicken. Diese Aktion ist nur erforderlich, um sicherzustellen, dass die [Adobe Commerce Support Knowledge Base](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/overview) über den `SSO`-Aufruf ordnungsgemäß konfiguriert ist.

1. Um zu Ihrem eigenen Konto zurückzukehren, klicken Sie auf **Zurück** in Ihren Browser-Steuerelementen und legen Sie **[!UICONTROL Switch Accounts]** auf `My Account` fest.

## Freigegebenen Zugriff widerrufen

1. Melden Sie sich bei Ihrem Commerce-Konto an.

1. Klicken Sie im linken Navigationsbereich auf **[!UICONTROL Shared Access]**.

1. Suchen Sie unter _[!UICONTROL Managing Users & Permissions]_das zu widerrufende Konto und klicken Sie auf **[!UICONTROL Delete]**.

   >[!NOTE]
   >
   > Wenn **[!UICONTROL Delete]** nicht angezeigt wird, überprüfen Sie, ob die **[!UICONTROL Share Name]** mit `Cloud Shared Access from MAG XYZ` beginnt. Konten mit diesem [ können nicht gelöscht ](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide#remove-cloud-shared-access-users).
   > 
   > Wenn ja, bitten Sie den Kontoinhaber, das Konto mit gemeinsamem Zugriff zu ändern, um die Kontoberechtigungen zu löschen. Nach dieser Aktualisierung kann der Benutzer nicht mehr auf Kontoressourcen zugreifen.
   >
   > Stellen Sie außerdem sicher, dass Benutzer aus dem Projekt entfernt werden, sodass sie keine E-Mail-Benachrichtigungen mehr erhalten: [Ehemalige Team-Mitglieder erhalten E-Mails zu Adobe Commerce Cloud-Benachrichtigungen](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/troubleshooting/miscellaneous/former-teammembers-receive-cloud-notification-emails)


1. Wenn Sie zum Bestätigen aufgefordert werden, klicken Sie auf **[!UICONTROL Delete User]**.

>[!NOTE]
>
>Sie können keine Benutzer mit dem Freigabenamen _Cloud Shared Access von MAG[XYZ)]_ dieser Benutzeroberfläche löschen. Siehe [Löschen von Benutzern, denen über ein Cloud-Projekt gemeinsamer Zugriff gewährt wurde?](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/troubleshooting/miscellaneous/shared-access-troubleshooting).
