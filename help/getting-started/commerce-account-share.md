---
title: Freigabe eines [!DNL Commerce] Kontos
description: Erfahren Sie, wie Sie anderen [!DNL Commerce] Kontoinhabern eingeschränkten Zugriff auf Ihr [!DNL Commerce] Konto gewähren.
exl-id: adc4fed4-89f4-4b0c-811c-fcf6f94dbc22
feature: User Account
source-git-commit: ec634ebedd43b8bbc6b4a3e5079035b055740f2d
workflow-type: tm+mt
source-wordcount: '805'
ht-degree: 0%

---

# Ein [!DNL Commerce]-Konto freigeben

Ihr [!DNL Commerce] -Konto enthält Informationen, die Sie vertrauenswürdigen Mitarbeitern und Dienstleistern zur Verfügung stellen können, die bei der Verwaltung Ihrer Site helfen. Als Inhaber des Primärkontos sind Sie berechtigt, anderen [!DNL Commerce] -Kontoinhabern eingeschränkten Zugriff zu gewähren. Der freigegebene Zugriff kann widerrufen, aber nicht von einem Benutzer an einen anderen übertragen werden.

Das Supportteam von [!DNL Commerce] hat keinen Zugriff auf das Konto und kann keinen freigegebenen Zugriff für Sie einrichten. Nur der primäre Kontoinhaber mit entsprechenden Berechtigungen kann einen freigegebenen Zugriff einrichten. Beim Freigeben des Kontozugriffs bleiben alle sensiblen Informationen wie Ihr Rechnungsverlauf oder Ihre Kreditkarteninformationen geschützt und stehen anderen Benutzern nie zur Verfügung.

>[!NOTE]
>
>Alle Aktionen, die von Benutzern mit gemeinsamem Zugriff durchgeführt werden, fallen in die alleinige Verantwortung des Hauptkontoinhabers. Adobe ist nicht für Aktionen von Benutzern verantwortlich, die gemeinsam auf Ihr Konto zugreifen können.

![Einstellungen für freigegebenen Zugriff](./assets/shared-access.png){width="600" zoomable="yes"}

## Freigegebenes Konto einrichten

1. Bevor Sie beginnen, erhalten Sie die folgenden Informationen aus dem [!DNL Commerce]-Konto der **neuen Zugriffsberechtigung für freigegebene Inhalte**:

   - Der Benutzer muss sich bereits für ein Konto unter account.adobe.com registriert und über account.magento.com angemeldet haben.
   - Der `MAGE ID/Account ID (MAG00XXXXXXX)` wird in der oberen linken Ecke der Registerkarte _[!UICONTROL Magento]_direkt über dem Link **Abmelden**angezeigt.
   - Die `Email` -Adresse, die mit dem Konto verknüpft ist.

1. Melden Sie sich bei Ihrem [[!DNL Commerce] Konto](commerce-account-create.md) an.

1. Klicken Sie im linken Navigationsfenster auf **[!UICONTROL Shared Access]**.

1. Klicken Sie auf **[!UICONTROL Add New User]**.

   ![Neuen Benutzer hinzufügen](./assets/shared-access-add.png){width="600" zoomable="yes"}

1. Führen Sie unter [!UICONTROL _New User Information]_ folgende Schritte aus:

   - Geben Sie die **[!UICONTROL Account ID]** aus dem [!DNL Commerce] -Konto des neuen Benutzers ein.
   - Geben Sie die **[!UICONTROL Email]** -Adresse ein, die mit dem [!DNL Commerce] -Konto des neuen Benutzers verknüpft ist.

   ![Neue Benutzerinformationen](./assets/shared-new-user.png){width="600"}

1. Führen Sie unter _[!UICONTROL Shared Information]_folgende Schritte aus:

   - Um das freigegebene Konto zu identifizieren, geben Sie einen **[!UICONTROL Share Name]** ein. Dieser Name dient als interne Referenz und ist nur für Sie und die Person sichtbar, für die Sie Ihr Konto freigeben.

     Als Best Practice wird empfohlen, den Namen Ihrer Organisation als [!UICONTROL Share Name] zu verwenden. Verwenden Sie keinen Namen, der mit `CLOUD SHARED ACCESS FROM MAG XYX` beginnt.
   - Wenn Sie Ihre persönlichen Kontaktinformationen für den neuen Benutzer freigeben möchten, geben Sie **[!UICONTROL Your Email]** und **[!UICONTROL Your Phone]** ein.

1. Aktivieren Sie unter &quot;_[!UICONTROL Grant Account Permissions]_&quot;das Kontrollkästchen jedes [!DNL Commerce]-Produkts und jeden Dienst, den/den Sie freigeben möchten.

   ![Erteilen der Kontoberechtigungen](./assets/shared-permissions.png){width="600"}

1. Klicken Sie auf **[!UICONTROL Create Shared Access]**.

   Die neuen Benutzerinformationen werden im Abschnitt &quot;_[!UICONTROL Manage Permissions]_&quot;der Seite &quot;Freigegebener Zugriff&quot;angezeigt und eine E-Mail-Einladung mit Anweisungen zum Zugriff auf das freigegebene Konto wird an den neuen Benutzer gesendet.

   ![Berechtigungen für freigegebenen Zugriff verwalten](./assets/shared-manage-permissions.png){width="600" zoomable="yes"}

>[!NOTE]
>
>Es ist nicht erforderlich, den Zugriff auf &quot;_[!UICONTROL Security Tool]_&quot;freizugeben. Jeder Benutzer mit einer MAGE-ID kann das Sicherheitsscan-Tool mit seinem eigenen Konto einrichten. Sie benötigen lediglich die erforderlichen Berechtigungen, um Änderungen an der Site vorzunehmen und das Eigentum an der Domäne mithilfe einer der [erforderlichen Methoden](https://experienceleague.adobe.com/en/docs/commerce-admin/systems/security/security-scan)) zu überprüfen.

## Auf freigegebene Konten zugreifen

Die folgenden Anweisungen werden aus der Perspektive eines freigegebenen Benutzers geschrieben, der eine Einladung zu einem freigegebenen Konto erhält.

1. Wenn Sie eine Einladung zu einem freigegebenen Konto erhalten, befolgen Sie die Anweisungen in der E-Mail, um sich bei Ihrem eigenen [!DNL Commerce]-Konto anzumelden.

   Das linke Navigationsfenster Ihres Kontos verfügt über eine neue Registerkarte _[!UICONTROL Shared with me]_. Das Steuerelement_[!UICONTROL Switch Accounts]_ in der oberen rechten Ecke verfügt über Optionen für `My Account` und den Namen des freigegebenen Kontos.

   ![Für mich freigegeben](./assets/shared-with-me.png){width="600" zoomable="yes"}

1. Um Zugriff auf das freigegebene Konto zu erhalten, setzen Sie **[!UICONTROL Switch Accounts]** auf den Namen des freigegebenen Kontos.

   ![Wechseln Sie zum freigegebenen Konto](./assets/shared-switch.png){width="600" zoomable="yes"}

   Das freigegebene Konto zeigt eine Willkommensnachricht und Kontaktinformationen an. Das linke Navigationsfenster enthält nur die Elemente, die Sie verwenden dürfen.

1. Um das freigegebene Konto mit dem Hilfe-Center zu verbinden, klicken Sie im linken Navigationsbereich des freigegebenen Kontos auf **[!UICONTROL Support]** .

   ![Support](./assets/shared-support.png){width="600" zoomable="yes"}

   Sie können das [Adobe Commerce Help Center](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/overview.html) aus dem freigegebenen Konto verwenden, um nach Artikeln und Informationen zur Fehlerbehebung zu suchen, Patches für bekannte Probleme zu finden und Support-Tickets zu erstellen.

   >[!NOTE]
   >
   >Nach Erhalt des freigegebenen Zugriffs muss sich der Benutzer bei seinem [[!DNL Commerce] Konto](https://account.magento.com/customer/account/login) anmelden, zu _Gemeinsamer Zugriff_ navigieren und auf die Registerkarte **[!UICONTROL Support]** klicken. Diese Aktion ist erstmalig erforderlich, um sicherzustellen, dass die [Wissensdatenbank des Adobe Commerce-Supports](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/overview.html) über den `SSO` -Aufruf ordnungsgemäß konfiguriert ist.

1. Um zu Ihrem eigenen Konto zurückzukehren, klicken Sie in Ihren Browsersteuerelementen auf **Zurück** und legen Sie **[!UICONTROL Switch Accounts]** auf `My Account` fest.

## Freigegebenen Zugriff sperren

1. Melden Sie sich bei Ihrem Commerce-Konto an.

1. Klicken Sie im linken Navigationsfenster auf **[!UICONTROL Shared Access]**.

1. Suchen Sie das Konto, das unter _[!UICONTROL Managing Users & Permissions]_gesperrt werden soll, und klicken Sie auf **[!UICONTROL Delete]**.

   >[!NOTE]
   >
   > Wenn **[!UICONTROL Delete]** nicht angezeigt wird, überprüfen Sie, ob die **[!UICONTROL Share Name]** mit `Cloud Shared Access from MAG XYZ` beginnt. Konten mit diesem [Namensmuster](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide#remove-cloud-shared-access-users) können nicht gelöscht werden.
   > 
   > Wenn ja, bitten Sie den Kontoinhaber, das Konto für freigegebenen Zugriff zu ändern, um die Kontoberechtigungen zu löschen. Nach dieser Aktualisierung kann der Benutzer auf keine Kontoressourcen zugreifen.
   >
   > Stellen Sie außerdem sicher, dass die Benutzer aus dem Projekt entfernt werden, damit sie keine E-Mail-Benachrichtigungen mehr erhalten: [Ehemalige Teammitglieder erhalten Adobe Commerce-Cloud-Benachrichtigungs-E-Mails ](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/troubleshooting/miscellaneous/former-teammembers-receive-cloud-notification-emails.html)


1. Klicken Sie bei Aufforderung zur Bestätigung auf **[!UICONTROL Delete User]**.

>[!NOTE]
>
>Sie können Benutzer mit dem Freigabenamen _Freigegebener Cloud-Zugriff nicht von MAG[XYZ]_ in dieser Benutzeroberfläche löschen. Siehe [Wie lösche ich Benutzer, denen freigegebener Zugriff über ein Cloud-Projekt gewährt wurde?](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide.html?lang=en#remove-cloud-shared-access-users).
