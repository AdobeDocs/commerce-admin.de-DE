---
title: A [!DNL Commerce] Konto freigeben
description: Erfahren Sie, wie Sie anderen Kontoinhabern  [!DNL Commerce]  eingeschränkten Zugriff auf Ihr  [!DNL Commerce]  gewähren.
exl-id: adc4fed4-89f4-4b0c-811c-fcf6f94dbc22
feature: User Account
TQID: https://experienceleague.adobe.com/A98obp-6T8JgE0yCm0TmxpRslEq2Cb-5m53rBfxzfhg
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 1078
ht-degree: 0%

---

# [!DNL Commerce] freigeben

Ihr [!DNL Commerce]-Konto enthält Informationen, die Sie vertrauenswürdigen Mitarbeitern und Dienstleistern zur Verfügung stellen können, die Sie bei der Verwaltung Ihrer Site unterstützen. Wenn Sie den Kontozugriff freigeben, bleiben alle sensiblen Informationen, wie z. B. Ihr Rechnungsverlauf oder Kreditkarteninformationen, geschützt und stehen anderen Benutzern nie zur Verfügung.

Der primäre Kontoinhaber ist befugt, anderen [!DNL Commerce] Kontoinhabern eingeschränkten Zugang zu gewähren. Freigegebener Zugriff kann widerrufen, aber nicht übertragen werden. Bei ``Cloud Shared Access from MAG[XYZ]`` Einträgen kann der Benutzerdatensatz **hier nicht gelöscht werden** aber der Zugriff **weiterhin widerrufen werden**.

Nur der Inhaber des primären Kontos mit den entsprechenden Berechtigungen kann formell geteilten Zugriff gewähren. Wenn der Hauptkontoinhaber keinen Zugriff mehr hat oder das Unternehmen verlassen hat, sollte der Kunde den [Commerce-Kontoübertragungsprozess verwenden](https://experienceleague.adobe.com/en/docs/commerce-admin/start/commerce-account/commerce-account-transfer) um den Besitz an einen neuen Kontakt zu übertragen. Obwohl das Commerce-Supportteam möglicherweise in bestimmten Fällen stellvertretend für den Kunden agieren kann, sollte der freigegebene Zugriff vom Kunden konfiguriert werden, um das Sicherheits- und Haftungsrisiko zu reduzieren.


![Freigegebene Zugriffseinstellungen](./assets/shared-access.png){width="600" zoomable="yes"}

Im Abschnitt Abrechnungshistorie werden nur ältere Rechnungen angezeigt, die vor einer Änderung an unserem Abrechnungssystem erstellt wurden. Wenn keine neueren Rechnungen aufgelistet sind, wurden diese auf das neue System umgestellt und sind von dieser Ansicht aus nicht zugänglich.

>[!IMPORTANT]
>
>Alle Aktionen, die von Benutzern mit gemeinsamem Zugriff durchgeführt werden, liegen in der alleinigen Verantwortung des Inhabers des primären Kontos. Adobe übernimmt keine Verantwortung für Aktionen von Benutzenden, die gemeinsamen Zugriff auf Ihr Konto haben.

## Freigegebenes Konto einrichten

1. Bevor Sie beginnen, rufen Sie die folgenden Informationen vom [!DNL Commerce] Konto des **neuen Empfängers mit gemeinsamem Zugriff** ab:

   - Der Benutzer muss sich bereits unter account.adobe.com für ein Konto registriert haben und über account.magento.com angemeldet sein. Weitere [&#x200B; finden Sie unter „Erstellen &#x200B;](https://experienceleague.adobe.com/de/docs/commerce-admin/start/commerce-account/commerce-account-create#create-a-commerce-account) Commerce-Kontos“.
   - Der `MAGE ID/Account ID (MAG00XXXXXXX)` wird in der linken oberen Ecke der Registerkarte _[!UICONTROL Magento]_&#x200B;direkt über dem Link **Abmelden**&#x200B;angezeigt.
   - Die `Email`, die mit dem Konto verknüpft ist.

1. Melden Sie sich bei Ihrem [[!DNL Commerce] Konto](commerce-account-create.md) an.

1. Klicken Sie im linken Navigationsbereich auf **[!UICONTROL Shared Access]**.

1. Klicken Sie auf **[!UICONTROL Add New User]**.

   ![Neuen Benutzer hinzufügen](./assets/shared-access-add.png){width="600" zoomable="yes"}

1. Gehen Sie unter [!UICONTROL _New User Information]_ wie folgt vor:

   - Geben Sie die **[!UICONTROL Account ID]** aus dem [!DNL Commerce] Konto des neuen Benutzers ein.
   - Geben Sie die **[!UICONTROL Email]**-Adresse ein, die mit dem [!DNL Commerce] des neuen Benutzers verknüpft ist.

   ![Neue Benutzerinformationen](./assets/shared-new-user.png){width="600"}

1. Gehen Sie unter _[!UICONTROL Shared Information]_&#x200B;wie folgt vor:

   - Um das freigegebene Konto zu identifizieren, geben Sie einen **[!UICONTROL Share Name]** ein. Dieser Name dient als interne Referenz und ist nur für Sie und die Person sichtbar, für die Sie Ihr Konto freigeben.

     Es empfiehlt sich, den Namen Ihres Unternehmens als [!UICONTROL Share Name] zu verwenden. Verwenden Sie keinen Namen, der mit `CLOUD SHARED ACCESS FROM MAG XYX` beginnt.
   - Wenn Sie Ihre persönlichen Kontaktinformationen für den neuen Benutzer freigeben möchten, geben Sie **[!UICONTROL Your Email]** und **[!UICONTROL Your Phone]** ein.

1. Aktivieren Sie unter _[!UICONTROL Grant Account Permissions]_&#x200B;das Kontrollkästchen jedes [!DNL Commerce] Produkts und Services, das Sie freigeben möchten.

   ![Erteilen Sie die Kontoberechtigungen](./assets/shared-permissions.png){width="600"}

1. Klicken Sie auf **[!UICONTROL Create Shared Access]**.

   Die Informationen zum neuen Benutzer werden im Abschnitt _[!UICONTROL Manage Permissions]_&#x200B;der Seite Freigegebener Zugriff angezeigt, und dem neuen Benutzer wird eine E-Mail-Einladung mit Anweisungen für den Zugriff auf das freigegebene Konto gesendet.

   ![Berechtigungen für freigegebenen Zugriff verwalten](./assets/shared-manage-permissions.png){width="600" zoomable="yes"}

>[!NOTE]
>
>Es ist nicht erforderlich, den Zugriff auf die _[!UICONTROL Security Tool]_&#x200B;freizugeben. Jeder Benutzer mit einer MAGE-ID kann das Sicherheits-Scan-Tool mit seinem eigenen Konto einrichten. Sie benötigen lediglich die erforderlichen Berechtigungen, um Änderungen an der Site vorzunehmen und die Eigentümerschaft der Domain mit einer der [erforderlichen Methoden](https://experienceleague.adobe.com/de/docs/commerce-admin/systems/security/security-scan) zu überprüfen.

## Zugreifen auf ein freigegebenes Konto

Die folgenden Anweisungen sind aus der Sicht eines freigegebenen Benutzers geschrieben, der eine Einladung zu einem freigegebenen Konto erhält.

1. Wenn Sie eine Einladung zu einem freigegebenen Konto erhalten, befolgen Sie die Anweisungen in der E-Mail, um sich bei Ihrem eigenen [!DNL Commerce]-Konto anzumelden.

   Das linke Navigationsfenster Ihres Kontos weist eine neue Registerkarte _[!UICONTROL Shared with me]_&#x200B;auf. Das&#x200B;_[!UICONTROL Switch Accounts]_-Steuerelement in der oberen rechten Ecke verfügt über Optionen zum `My Account` und den Namen des freigegebenen Kontos.

   ![Für mich freigegeben](./assets/shared-with-me.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >   Wenn das _[!UICONTROL Switch Accounts]_&#x200B;nicht angezeigt wird, wenden Sie sich an den primären Kontoinhaber und bestätigen Sie, dass er Ihre richtigen [Kontoinformationen](#set-up-a-shared-account) eingegeben hat.


1. Um Zugriff auf das freigegebene Konto zu erhalten, legen Sie **[!UICONTROL Switch Accounts]** auf den Namen des freigegebenen Kontos fest.

   ![Wechseln Sie zum freigegebenen Konto](./assets/shared-switch.png){width="600" zoomable="yes"}

   Das freigegebene Konto zeigt eine Willkommensnachricht und Kontaktinformationen an. Der linke Navigationsbereich enthält nur die Elemente, die Sie verwenden dürfen.

1. Um das freigegebene Konto mit dem Hilfezentrum zu verbinden, klicken Sie im linken Navigationsbereich des freigegebenen Kontos auf **[!UICONTROL Support]** .

   ![Support](./assets/shared-support.png){width="600" zoomable="yes"}

   Sie können das [Adobe Commerce Help Center](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/overview) über das freigegebene Konto nach Artikeln und Informationen zur Fehlerbehebung suchen, Patches für bekannte Probleme suchen und Support-Tickets erstellen.

   >[!NOTE]
   >
   >Um nach Erhalt des gemeinsamen Zugriffs [einen Support-Fall senden](https://experienceleague.adobe.com/de/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide#support-case) auf Experience League zu aktivieren, müssen Sie zunächst den Organisationsnamen, der auf „([!DNL Commerce])“ endet, in der linken Spalte auswählen.

1. Um zu Ihrem eigenen Konto zurückzukehren, klicken Sie auf **Zurück** in Ihren Browser-Steuerelementen und legen Sie **[!UICONTROL Switch Accounts]** auf `My Account` fest.

## Freigegebenen Zugriff widerrufen

1. Melden Sie sich bei Ihrem Commerce-Konto an.

1. Klicken Sie im linken Navigationsbereich auf **[!UICONTROL Shared Access]**.

1. Suchen Sie unter _[!UICONTROL Managing Users & Permissions]_&#x200B;das zu widerrufende Konto und klicken Sie auf **[!UICONTROL Delete]**.

   >[!NOTE]
   >
   > Wenn **[!UICONTROL Delete]** nicht angezeigt wird, überprüfen Sie, ob die **[!UICONTROL Share Name]** das Namensmuster `Cloud Shared Access from MAG0XYZ` enthält. Wenn das Konto dieses [Namensmuster aufweist und nicht gelöscht werden kann](https://experienceleague.adobe.com/de/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide#remove-cloud-shared-access-users) liegt dies daran, dass der freigegebene Zugriff von einer API und nicht direkt aus dem [Commerce-Konto erstellt &#x200B;](https://account.magento.com/).
   > 
   > Wenn sie nicht gelöscht werden kann, lassen Sie einfach den Kontoinhaber das Konto mit gemeinsamem Zugriff ändern und unter Kontoberechtigungen erteilen jedes Element deaktivieren. Nach diesem Update kann der Benutzer nicht mehr auf Kontoressourcen zugreifen.
   > ![image](https://git.corp.adobe.com/AdobeDocs/commerce-admin.en/assets/38345/55f383e5-89c7-4832-bada-f765b522f4b5)
   >
   > Stellen Sie außerdem sicher, dass Benutzer aus dem Projekt entfernt werden, sodass sie keine E-Mail-Benachrichtigungen mehr erhalten: [Ehemalige Team-Mitglieder erhalten E-Mails zur Cloud-Benachrichtigung von Adobe Commerce](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/troubleshooting/miscellaneous/former-teammembers-receive-cloud-notification-emails)


1. Wenn Sie zum Bestätigen aufgefordert werden, klicken Sie auf **[!UICONTROL Delete User]**.

>[!NOTE]
>
>Sie können keine Benutzer mit dem Freigabenamen _Cloud Shared Access von MAG[XYZ)]_ dieser Benutzeroberfläche löschen. Siehe [Löschen von Benutzern, denen über ein Cloud-Projekt gemeinsamer Zugriff gewährt wurde?](https://experienceleague.adobe.com/de/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide#remove-cloud-shared-access-users).

## Verwandtes Lesen

[Fehlerbehebung bei freigegebenem Zugriff](https://experienceleague.adobe.com/de/docs/commerce-knowledge-base/kb/troubleshooting/miscellaneous/shared-access-troubleshooting)

