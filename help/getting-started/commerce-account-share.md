---
title: Freigeben von [!DNL Commerce] account
description: Erfahren Sie, wie Sie eingeschränkten Zugriff auf [!DNL Commerce] andere [!DNL Commerce] Kontoinhaber.
exl-id: adc4fed4-89f4-4b0c-811c-fcf6f94dbc22
feature: User Account
source-git-commit: ec634ebedd43b8bbc6b4a3e5079035b055740f2d
workflow-type: tm+mt
source-wordcount: '805'
ht-degree: 0%

---

# Freigeben von [!DNL Commerce] account

Ihre [!DNL Commerce] -Konto enthält Informationen, die Sie vertrauenswürdigen Mitarbeitern und Dienstleistern zur Verfügung stellen können, die bei der Verwaltung Ihrer Site helfen. Als Inhaber des Primärkontos sind Sie berechtigt, anderen Benutzern eingeschränkten Zugriff zu gewähren [!DNL Commerce] Kontoinhaber. Der freigegebene Zugriff kann widerrufen, aber nicht von einem Benutzer an einen anderen übertragen werden.

Die [!DNL Commerce] Das Supportteam hat keinen Zugriff auf das Konto und kann keinen freigegebenen Zugriff für Sie einrichten. Nur der primäre Kontoinhaber mit entsprechenden Berechtigungen kann einen freigegebenen Zugriff einrichten. Beim Freigeben des Kontozugriffs bleiben alle sensiblen Informationen wie Ihr Rechnungsverlauf oder Ihre Kreditkarteninformationen geschützt und stehen anderen Benutzern nie zur Verfügung.

>[!NOTE]
>
>Alle Aktionen, die von Benutzern mit gemeinsamem Zugriff durchgeführt werden, fallen in die alleinige Verantwortung des Hauptkontoinhabers. Adobe ist nicht für Aktionen von Benutzern verantwortlich, die gemeinsam auf Ihr Konto zugreifen können.

![Einstellungen für freigegebenen Zugriff](./assets/shared-access.png){width="600" zoomable="yes"}

## Freigegebenes Konto einrichten

1. Bevor Sie beginnen, erhalten Sie die folgenden Informationen aus dem [!DNL Commerce] des **neue Zugriffsberechtigung**:

   - Der Benutzer muss sich bereits für ein Konto unter account.adobe.com registriert und über account.magento.com angemeldet haben.
   - Die `MAGE ID/Account ID (MAG00XXXXXXX)` wird in der oberen linken Ecke des _[!UICONTROL Magento]_Registerkarte direkt über dem **Abmelden**-Link.
   - Die `Email` -Adresse, die mit dem Konto verknüpft ist.

1. Melden Sie sich bei Ihrer [[!DNL Commerce] account](commerce-account-create.md).

1. Klicken Sie im linken Navigationsbereich auf **[!UICONTROL Shared Access]**.

1. Klicks **[!UICONTROL Add New User]**.

   ![Neuen Benutzer hinzufügen](./assets/shared-access-add.png){width="600" zoomable="yes"}

1. under [!UICONTROL _New User Information]_, führen Sie folgende Schritte aus:

   - Geben Sie die **[!UICONTROL Account ID]** aus dem [!DNL Commerce] -Konto.
   - Geben Sie die **[!UICONTROL Email]** -Adresse, die mit dem [!DNL Commerce] -Konto.

   ![Neue Benutzerinformationen](./assets/shared-new-user.png){width="600"}

1. under _[!UICONTROL Shared Information]_führen Sie folgende Schritte aus:

   - Um das freigegebene Konto zu identifizieren, geben Sie einen **[!UICONTROL Share Name]**. Dieser Name dient als interne Referenz und ist nur für Sie und die Person sichtbar, für die Sie Ihr Konto freigeben.

     Als Best Practice empfiehlt sich die Verwendung Ihres Organisationsnamens als [!UICONTROL Share Name]. Verwenden Sie keinen Namen, der mit `CLOUD SHARED ACCESS FROM MAG XYX`.
   - Wenn Sie Ihre persönlichen Kontaktinformationen für den neuen Benutzer freigeben möchten, geben Sie **[!UICONTROL Your Email]** und **[!UICONTROL Your Phone]**.

1. under _[!UICONTROL Grant Account Permissions]_, aktivieren Sie das Kontrollkästchen jedes [!DNL Commerce] Produkt und Service, die Sie freigeben möchten.

   ![Gewähren von Kontoberechtigungen](./assets/shared-permissions.png){width="600"}

1. Klicks **[!UICONTROL Create Shared Access]**.

   Die neuen Benutzerinformationen werden im _[!UICONTROL Manage Permissions]_und eine E-Mail-Einladung mit Anweisungen zum Zugriff auf das freigegebene Konto an den neuen Benutzer gesendet.

   ![Berechtigungen für freigegebenen Zugriff verwalten](./assets/shared-manage-permissions.png){width="600" zoomable="yes"}

>[!NOTE]
>
>Der Zugriff auf die _[!UICONTROL Security Tool]_- Jeder Benutzer mit einer MAGE-ID kann das Sicherheitsscan-Tool mit seinem eigenen Konto einrichten. Sie benötigen lediglich die erforderlichen Berechtigungen, um Änderungen an der Site vorzunehmen und mithilfe eines der [erforderliche Methoden](https://experienceleague.adobe.com/en/docs/commerce-admin/systems/security/security-scan)).

## Auf freigegebene Konten zugreifen

Die folgenden Anweisungen werden aus der Perspektive eines freigegebenen Benutzers geschrieben, der eine Einladung zu einem freigegebenen Konto erhält.

1. Wenn Sie eine Einladung zu einem freigegebenen Konto erhalten, befolgen Sie die Anweisungen in der E-Mail, um sich bei Ihrem eigenen anzumelden [!DNL Commerce] -Konto.

   Das linke Navigationsfenster Ihres Kontos enthält eine neue _[!UICONTROL Shared with me]_Registerkarte. Die_[!UICONTROL Switch Accounts]_ -Steuerelement in der oberen rechten Ecke verfügt über Optionen für `My Account` und den Namen des freigegebenen Kontos.

   ![Freigegeben für mich](./assets/shared-with-me.png){width="600" zoomable="yes"}

1. Um Zugriff auf das freigegebene Konto zu erhalten, legen Sie **[!UICONTROL Switch Accounts]** zum Namen des freigegebenen Kontos.

   ![Wechseln Sie zum freigegebenen Konto.](./assets/shared-switch.png){width="600" zoomable="yes"}

   Das freigegebene Konto zeigt eine Willkommensnachricht und Kontaktinformationen an. Das linke Navigationsfenster enthält nur die Elemente, die Sie verwenden dürfen.

1. Um das freigegebene Konto mit dem Hilfe-Center zu verbinden, klicken Sie auf **[!UICONTROL Support]** im linken Navigationsbereich des freigegebenen Kontos.

   ![Support](./assets/shared-support.png){width="600" zoomable="yes"}

   Sie können die [Adobe Commerce Help Center](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/overview.html) über das freigegebene Konto, um nach Artikeln und Informationen zur Fehlerbehebung zu suchen, Patches für bekannte Probleme zu finden und Support-Tickets zu erstellen.

   >[!NOTE]
   >
   >Nach Erhalt des freigegebenen Zugriffs muss sich der Benutzer bei der [[!DNL Commerce] account](https://account.magento.com/customer/account/login), navigieren Sie zu _Freigegebener Zugriff_ und klicken Sie auf **[!UICONTROL Support]** Registerkarte. Diese Aktion ist zum ersten Mal nur erforderlich, um sicherzustellen, dass die Variable [Wissensdatenbank zur Adobe Commerce-Unterstützung](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/overview.html) ordnungsgemäß konfiguriert wurde, über die `SSO` aufrufen.

1. Um zu Ihrem eigenen Konto zurückzukehren, klicken Sie auf **Zurück** in Ihren Browser-Steuerelementen und legen Sie **[!UICONTROL Switch Accounts]** nach `My Account`.

## Freigegebenen Zugriff sperren

1. Melden Sie sich bei Ihrem Commerce-Konto an.

1. Klicken Sie im linken Navigationsbereich auf **[!UICONTROL Shared Access]**.

1. Suchen Sie nach dem Konto, das unter widerrufen werden soll. _[!UICONTROL Managing Users & Permissions]_und klicken **[!UICONTROL Delete]**.

   >[!NOTE]
   >
   > Wenn  **[!UICONTROL Delete]** nicht angezeigt wird, überprüfen Sie, ob die **[!UICONTROL Share Name]** beginnt mit `Cloud Shared Access from MAG XYZ`. Konten mit dieser [Benennungsmuster](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide#remove-cloud-shared-access-users).
   > 
   > Wenn ja, bitten Sie den Kontoinhaber, das Konto für freigegebenen Zugriff zu ändern, um die Kontoberechtigungen zu löschen. Nach dieser Aktualisierung kann der Benutzer auf keine Kontoressourcen zugreifen.
   >
   > Stellen Sie außerdem sicher, dass die Benutzer aus dem Projekt entfernt werden, damit sie keine E-Mail-Benachrichtigungen mehr erhalten: [Ehemalige Teammitglieder erhalten Adobe Commerce-Cloud-Benachrichtigungs-E-Mails](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/troubleshooting/miscellaneous/former-teammembers-receive-cloud-notification-emails.html)


1. Klicken Sie bei Aufforderung zur Bestätigung auf **[!UICONTROL Delete User]**.

>[!NOTE]
>
>Sie können Benutzer mit dem Freigabenamen von nicht löschen _Freigegebener Cloud-Zugriff über MAG[XYZ]_ in dieser Schnittstelle. Siehe [Wie kann ich Benutzer löschen, denen der gemeinsame Zugriff über ein Cloud-Projekt gewährt wurde?](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide.html?lang=en#remove-cloud-shared-access-users).
