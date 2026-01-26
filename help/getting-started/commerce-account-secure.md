---
title: 'Konto  [!DNL Commerce] '
description: Erfahren Sie, wie Sie die Zwei-Faktor-Authentifizierung verwenden, um Ihr - [!DNL Commerce]  zu schützen.
exl-id: 4847b5cb-a93a-40d0-8c31-c30afa27c0ce
feature: User Account
source-git-commit: cace9d1de00955494d8bc607c017778ff7df4806
workflow-type: tm+mt
source-wordcount: '1677'
ht-degree: 0%

---

# Schützen [!DNL Commerce] Kontos

Die Zwei-Faktor-Authentifizierung (TFA oder 2FA) ist eine zusätzliche Sicherheitsebene, um Ihr [!DNL Commerce]-Konto besser vor unbefugtem Zugriff zu schützen. Um den Anmeldevorgang abzuschließen, erfordert der TFA _zweiten Faktor_ zusätzlich zu den standardmäßigen Benutzernamen- und Kennwortberechtigungen. Dieser zweite Faktor besteht aus temporären Verifizierungs-Codes, die kontinuierlich von einer auf Ihrem Mobilgerät installierten TFA-Anwendung generiert und mit Ihrem [!DNL Commerce]-Konto gepaart werden.

Wenn TFA aktiviert ist, ist Ihr Konto sicherer. Ein nicht autorisierter Benutzer kann sich nur anmelden, wenn er sowohl über Ihren Benutzernamen und Ihr Passwort (erster Faktor) als auch über einen gültigen Verifizierungs-Code der TFA-Anwendung auf Ihrem persönlichen Gerät (zweiter Faktor) verfügt.

>[!NOTE]
>
>Die Zwei-Faktor-Authentifizierung, die den _Administrator_ Ihres Stores schützt, verfügt über eine separate Einrichtung. Weitere Informationen finden Sie unter [Zwei-Faktor-Authentifizierung](../systems/security-two-factor-authentication.md).

## Bevor Sie beginnen

Um TFA verwenden zu können, muss auf Ihrem persönlichen Gerät (z. B. Smartphone, Tablet, Computer) eine TFA-Anwendung installiert sein. Es gibt viele verfügbare, aber einige beliebte und kostenlose Optionen sind:

- Google Authenticator (iOS, Android™, BlackBerry®)

- Autor (iOS, Android™)

- Microsoft® Authenticator (iOS, Android™, Windows Phone)

## Zwei-Faktor-Authentifizierung aktivieren

1. Melden Sie sich bei Ihrem [[!DNL Commerce] Konto](https://account.magento.com/customer/account/login){:target="_blank"} an.

1. Wählen Sie im linken Navigationsbereich **[!UICONTROL Account Settings]** und dann **[!UICONTROL Two-factor Authentication]** aus.

   ![TFA aktivieren](./assets/2fa-enable.png){width="600" zoomable="yes"}

1. Wählen Sie **[!UICONTROL Enable]** aus, um den Einrichtungsprozess der Zwei-Faktor-Authentifizierung zu starten.

1. Geben Sie die an Ihre E-Mail gesendeten **[!UICONTROL Verification Code]** ein und wählen Sie **[!UICONTROL Verify Code]** aus, um fortzufahren.

   ![Geben Sie den Verifizierungs-Code ein](./assets/2fA-verification-code-prompt.png){width="400"}

1. Öffnen Sie die Zwei-Faktor-Authentifizierungsanwendung, die Sie heruntergeladen und auf Ihrem persönlichen Gerät installiert haben.

1. Verwenden Sie im [!UICONTROL SETUP TWO-FACTOR AUTHENTICATION] Formular die **[!UICONTROL Setup Code]** , um Adobe Commerce zu Ihrer TFA-Anwendung hinzuzufügen.

   ![Adobe Commerce zur TFA-App hinzufügen](./assets/commerce-account-2fa-setup-app.png){width="400"}

   Sie können den Code hinzufügen, indem Sie den QR-Code mithilfe der TFA-Anwendung scannen oder manuell eingeben. Dieser Code paart Ihre TFA-Anwendung mit Ihrem [!DNL Commerce]-Konto und ermöglicht es den Berechtigungen, die TFA-Anwendung zu generieren, um Verifizierungs-Codes für den sicheren Kontozugriff zu generieren.

1. Schließen Sie die Einrichtung ab.

   - Geben Sie im [!UICONTROL SETUP TWO FACTOR-AUTHENTICATION]-Formular den Verifizierungs-Code aus Ihrer Zwei-Faktor-Authentifizierungsanwendung ein.

   - Wählen Sie **[!UICONTROL Verify Code]** aus.

   >[!NOTE]
   >
   >Aus Sicherheitsgründen laufen die Verifizierungs-Codes in Ihrer TFA-Anwendung kontinuierlich ab und werden neu generiert. **_Immer_** Verwenden Sie den aktuell angezeigten Code.

1. Speichern Sie die präsentierten **[!UICONTROL Recovery Codes]** an einem sicheren und zugänglichen Ort.

   ![Wiederherstellungs-Codes speichern](./assets/commerce-account-2fa-store-recovery-codes.png){width="400"}

   Wenn Sie bei Ihrem [!DNL Commerce]-Konto keinen Verifizierungs-Code angeben können, müssen Sie einen Wiederherstellungs-Code verwenden, um den Zugriff auf das Konto wiederzuerlangen.

   Jeder Wiederherstellungs-Code kann nur einmal verwendet werden, aber Sie können [ neue ](#generate-new-recovery-codes) generieren. Bei Wiederherstellungs-Codes wird zwischen Groß- und Kleinschreibung unterschieden.

1. Aktivieren Sie das Bestätigungs-Kontrollkästchen und klicken Sie auf **[!UICONTROL Submit]** , um fortzufahren.

1. Um sicherzustellen, dass Sie den Zugriff auf Ihr Konto wiederherstellen können, geben Sie eine **[!UICONTROL Recovery Email]** ein.

   Diese E-Mail-Adresse wird benötigt, wenn Sie keinen Verifizierungs-Code aus Ihrer Zwei-Faktor-Authentifizierungsanwendung generieren können und keinen Zugriff auf einen ungenutzten vorgenerierten Wiederherstellungs-Code haben.

   Alle 24 Stunden können Sie einen temporären Wiederherstellungs-Code generieren und an Ihre vorgesehene Wiederherstellungs-E-Mail-Adresse senden. Verwenden Sie diesen Code, um den Kontozugriff wiederzuerlangen.

   >[!IMPORTANT]
   >
   >Beibehaltung des Zugriffs auf Ihr Wiederherstellungs-E-Mail-Konto Andernfalls können Sie keine temporären Wiederherstellungs-Codes verwenden, die an dieses Konto gesendet wurden.

   ![Wiederherstellungs-E-Mail festlegen](./assets/commerce-account-2fa-set-recovery-email.png){width="400"}

1. Aktivieren Sie das Kontrollkästchen zur Bestätigung und wählen Sie **[!UICONTROL Submit]** aus, um den Einrichtungsprozess der Zwei-Faktor-Authentifizierung abzuschließen.

   - An die mit Ihrem [!DNL Commerce]-Konto verknüpfte E-Mail-Adresse wird eine Benachrichtigung gesendet, um zu bestätigen, dass Sie die Zwei-Faktor-Authentifizierung erfolgreich aktiviert haben.

   - Eine Benachrichtigung wird an Ihr Wiederherstellungs-E-Mail-Konto gesendet, um die Konfiguration zu bestätigen.

>[!TIP]
>
>Wenn Sie Ihr persönliches Gerät verlieren oder ein neues erhalten, können Sie [Ihre Zwei-Faktor-Authentifizierungs-App ändern](#change-your-two-factor-authentication-application) und neue Wiederherstellungs-Codes generieren.

## Melden Sie sich mit einem Verifizierungs-Code an

1. Navigieren Sie zum [!DNL Commerce] [Konto-Anmeldung](https://account.magento.com/customer/account/login){:target="_blank"}.

1. Geben Sie Ihren Benutzernamen und Ihr Passwort ein und wählen Sie dann **[!UICONTROL Login]** aus.

1. Geben Sie bei Aufforderung die **[!UICONTROL Verification Code]** ein, die in Ihrer Zwei-Faktor-Authentifizierungsanwendung angezeigt wird.

   ![Verifizierungs-Code eingeben](./assets/commerce-account-2fa-login-verification-code.png){width="600"}

1. Wählen Sie **[!UICONTROL Submit]** aus, um den Anmeldevorgang abzuschließen.

## Melden Sie sich mit einem Wiederherstellungs-Code an

1. Navigieren Sie zum [!DNL Commerce] [Konto-Anmeldung](https://account.magento.com/customer/account/login){:target="_blank"}.

1. Geben Sie Ihren Benutzernamen und Ihr Passwort ein und wählen Sie dann **[!UICONTROL Login]** aus.

1. Wählen Sie **[!UICONTROL Use recovery code]** aus, um die Eingabeaufforderung für den Verifizierungs-Code zu umgehen.

1. Geben Sie bei Aufforderung einen nicht verwendeten **[!UICONTROL Recovery Code]** ein.

   ![Wiederherstellungscode eingeben](./assets/2fa-recovery-code.png){width="600"}

1. Wählen Sie **[!UICONTROL Submit]** aus, um den Anmeldevorgang abzuschließen.

## Mit Wiederherstellungs-E-Mail anmelden

1. Melden Sie sich bei Ihrem [[!DNL Commerce] Konto](https://account.magento.com/customer/account/login){:target="_blank"} an.

1. Geben Sie Ihren Benutzernamen und Ihr Passwort ein und wählen Sie dann **[!UICONTROL Login]** aus.

1. Wählen Sie **[!UICONTROL Use recovery code]** aus, um die Eingabeaufforderung für den Verifizierungs-Code zu umgehen.

1. Um einen temporären Wiederherstellungs-Code per E-Mail zu erhalten, klicken Sie auf den Link **[!UICONTROL recovery email]** .

   ![Wiederherstellungs-E-Mail verwenden](./assets/2fa-recovery-email.png){width="600"}

1. Öffnen Sie Ihr Wiederherstellungs-E-Mail-Konto, um den temporären Code abzurufen, und geben Sie dann den Code in die vorgesehenen Felder ein.

1. Wählen Sie **[!UICONTROL Submit]** aus, um den Anmeldevorgang abzuschließen.

Nachdem Sie einen temporären Wiederherstellungs-Code für den Zugriff auf Ihr Konto verwendet haben[ generieren Sie neue Wiederherstellungs-Codes ](#generate-new-recovery-codes) speichern Sie sie, um weitere Probleme beim Zugriff auf das Konto zu vermeiden.

## Wiederherstellungs-Codes anzeigen

1. Navigieren Sie zum [!DNL Commerce] [Konto-Anmeldung](https://account.magento.com/customer/account/login){:target="_blank"}.

1. Geben Sie Ihren Benutzernamen und Ihr Passwort ein und wählen Sie dann **[!UICONTROL Login]** aus.

1. Schließen Sie den Anmeldevorgang mit einer der zuvor beschriebenen Zwei-Faktor-Authentifizierungsmethoden ab.

1. Wählen Sie im linken Navigationsbereich **[!UICONTROL Account Settings]** und dann **[!UICONTROL Two-factor Authentication]** aus.

   ![2FA-](./assets/commerce-account-2fa-manage.png){width="600" zoomable="yes"}

1. Um Ihre vorgenerierten Wiederherstellungscodes anzuzeigen, wählen Sie **Wiederherstellungscodes anzeigen**.

1. Geben Sie die an Ihre E-Mail gesendeten **[!UICONTROL Verification Code]** ein und wählen Sie **[!UICONTROL Verify Code]** aus, um fortzufahren.

   ![Verifizierungs-Code eingeben](./assets/2fA-verification-code-prompt.png){width="400"}

1. Speichern Sie die **Wiederherstellungscodes** an einem sicheren und zugänglichen Ort.

   Wenn Sie keinen Verifizierungs-Code für die Anmeldung bei Ihrem [!DNL Commerce]-Konto angeben können, ist die Verwendung eines Wiederherstellungs-Codes die einzige Möglichkeit, den Zugriff auf das Konto wiederzuerlangen.

   Jeder Wiederherstellungs-Code ist nur eine einmalige Verwendung, aber Sie können immer [ neue ](#generate-new-recovery-codes) generieren. Bei Wiederherstellungs-Codes wird zwischen Groß- und Kleinschreibung unterschieden.

   ![Wiederherstellungs-Codes anzeigen](./assets/2fa-view-recovery.png){width="400"}

1. Aktivieren Sie das Kontrollkästchen und klicken Sie auf **[!UICONTROL Submit]** , um das Dialogfeld zu schließen.

## Neue Wiederherstellungs-Codes generieren

1. Navigieren Sie zum [!DNL Commerce] [Konto-Anmeldung](https://account.magento.com/customer/account/login){:target="_blank"}.

1. Geben Sie Ihren Benutzernamen und Ihr Passwort ein und wählen Sie dann **[!UICONTROL Login]** aus.

1. Schließen Sie den Anmeldevorgang mit einer der zuvor beschriebenen Zwei-Faktor-Authentifizierungsmethoden ab.

1. Wählen Sie im linken Navigationsbereich **[!UICONTROL Account Settings]** und dann **[!UICONTROL Two-factor Authentication]** aus.

1. Um neue vorgenerierte Wiederherstellungscodes zu generieren, wählen Sie **Neue Wiederherstellungscodes generieren** aus.

1. Geben Sie die an Ihre E-Mail gesendeten **[!UICONTROL Verification Code]** ein und wählen Sie **[!UICONTROL Verify Code]** aus, um fortzufahren.

1. Speichern Sie die **Wiederherstellungscodes** an einem sicheren und zugänglichen Ort.

   Wenn Sie bei Ihrem [!DNL Commerce]-Konto keinen Verifizierungs-Code angeben können, ist die Verwendung eines Wiederherstellungs-Codes die einzige Möglichkeit, den Zugriff auf das Konto wiederzuerlangen.

   Alle zuvor generierten Wiederherstellungscodes werden jetzt ungültig gemacht und sollten verworfen werden (nur der aktuelle Satz generierter Wiederherstellungscodes ist funktionsfähig). Bei Wiederherstellungs-Codes wird zwischen Groß- und Kleinschreibung unterschieden.

1. Aktivieren Sie das Kontrollkästchen und klicken Sie auf **[!UICONTROL Submit]** , um das Dialogfeld zu schließen.

## Wiederherstellungs-E-Mail ändern

1. Navigieren Sie zum [!DNL Commerce] [Konto-Anmeldung](https://account.magento.com/customer/account/login){:target="_blank"}.

1. Geben Sie Ihren Benutzernamen und Ihr Passwort ein und wählen Sie dann **[!UICONTROL Login]** aus.

1. Schließen Sie den Anmeldevorgang mit einer der zuvor beschriebenen Zwei-Faktor-Authentifizierungsmethoden ab.

1. Wählen Sie im linken Navigationsbereich **[!UICONTROL Account Settings]** und dann **[!UICONTROL Two-factor Authentication]** aus.

1. Wählen Sie **Wiederherstellungs-E-Mail**, um die Wiederherstellungs-E-Mail in der Datei für Ihr Konto zu ändern.

1. Geben Sie die an Ihre E-Mail gesendeten **[!UICONTROL Verification Code]** ein und wählen Sie **[!UICONTROL Verify Code]** aus, um fortzufahren.

1. Um sicherzustellen, dass Sie den Zugriff auf Ihr Konto wiederherstellen können, geben Sie eine **Wiederherstellungs-E-Mail** ein.

   Diese E-Mail-Adresse wird benötigt, wenn Sie keinen Verifizierungs-Code aus Ihrer Zwei-Faktor-Authentifizierungsanwendung generieren können und keinen Zugriff auf einen ungenutzten vorgenerierten Wiederherstellungs-Code haben.

   Alle 24 Stunden können Sie einen temporären Wiederherstellungs-Code generieren und an Ihre vorgesehene Wiederherstellungs-E-Mail-Adresse senden. Sie können diesen Code verwenden, um den Kontozugriff wiederzuerlangen.

   >[!IMPORTANT]
   >
   >Beibehaltung des Zugriffs auf Ihr Wiederherstellungs-E-Mail-Konto Andernfalls können Sie keine temporären Wiederherstellungs-Codes verwenden, die an dieses Konto gesendet wurden.

1. Aktivieren Sie das Kontrollkästchen und klicken Sie auf **[!UICONTROL Submit]** , um das Dialogfeld zu schließen.

   Das System sendet eine E-Mail-Benachrichtigung an die Wiederherstellungs-E-Mail, die Sie angegeben haben, um zu bestätigen, dass eine bestimmte E-Mail-Adresse als Wiederherstellungs-E-Mail für den Empfang temporärer Wiederherstellungs-Codes gespeichert ist.

## Ändern der Zwei-Faktor-Authentifizierungsanwendung

1. Navigieren Sie zum [!DNL Commerce] [Konto-Anmeldung](https://account.magento.com/customer/account/login){:target="_blank"}.

1. Geben Sie Ihren Benutzernamen und Ihr Passwort ein und wählen Sie dann **[!UICONTROL Login]** aus.

1. Schließen Sie den Anmeldevorgang mit einer der zuvor beschriebenen Zwei-Faktor-Authentifizierungsmethoden ab.

1. Wählen Sie im linken Navigationsbereich **[!UICONTROL Account Settings]** und dann **[!UICONTROL Two-factor Authentication]** aus.

1. Wählen Sie **TFA-Anwendung ändern** aus, um eine andere TFA-Anwendung mit Ihrem magento.com -Konto zu verwenden.

1. Geben Sie die an Ihre E-Mail gesendeten **[!UICONTROL Verification Code]** ein und wählen Sie **[!UICONTROL Verify Code]** aus, um fortzufahren.

1. Öffnen Sie die Zwei-Faktor-Authentifizierungsanwendung auf Ihrem persönlichen Gerät.

1. Geben Sie **Setup-Code** in Ihr Zwei-Faktor-Authentifizierungsprogramm ein.

   Sie können den Code hinzufügen, indem Sie den QR-Code mithilfe der TFA-Anwendung scannen oder manuell eingeben. Dieser Code paart Ihre TFA-Anwendung mit Ihrem [!DNL Commerce]-Konto und ermöglicht es den Berechtigungen für die TFA-Anwendung, Verifizierungs-Codes für den sicheren Kontozugriff zu generieren.

   >[!NOTE]
   >
   >Aus Sicherheitsgründen laufen die Verifizierungs-Codes in Ihrer TFA-Anwendung kontinuierlich ab und werden neu generiert. **_Immer_** Verwenden Sie den aktuell angezeigten Code.

1. Wenn Ihre TFA-Anwendung jetzt mit Ihrem [!DNL Commerce]-Konto gepaart ist, geben Sie die in Ihrer TFA-Anwendung angezeigten **[!UICONTROL Verification Code]** ein und wählen Sie **[!UICONTROL Verify Code]** aus, um fortzufahren.

1. Speichern Sie die **Wiederherstellungscodes** an einem sicheren und zugänglichen Ort.

   Wenn Sie bei Ihrem [!DNL Commerce]-Konto keinen Verifizierungs-Code angeben können, können Sie den Zugriff auf das Konto nur mit einem Wiederherstellungs-Code zurückgewinnen.

   Jeder Wiederherstellungs-Code ist nur eine einmalige Verwendung, aber Sie können immer [ neue ](#generate-new-recovery-codes) generieren. Bei Wiederherstellungs-Codes wird zwischen Groß- und Kleinschreibung unterschieden. Bei Wiederherstellungs-Codes wird zwischen Groß- und Kleinschreibung unterschieden.

1. Aktivieren Sie das Kontrollkästchen zur Bestätigung und wählen Sie **[!UICONTROL Submit]** aus, um fortzufahren.

1. Um sicherzustellen, dass Sie den Zugriff auf Ihr Konto wiederherstellen können, geben Sie eine **Wiederherstellungs-E-Mail** ein.

   Diese E-Mail-Adresse wird benötigt, wenn Sie keinen Verifizierungs-Code aus Ihrer Zwei-Faktor-Authentifizierungsanwendung generieren können und keinen Zugriff auf einen ungenutzten vorgenerierten Wiederherstellungs-Code haben.

   Alle 24 Stunden können Sie einen temporären Wiederherstellungs-Code generieren und an Ihre vorgesehene Wiederherstellungs-E-Mail-Adresse senden. Verwenden Sie diesen Code, um den Kontozugriff wiederzuerlangen.

   >[!IMPORTANT]
   >
   >Beibehaltung des Zugriffs auf Ihr Wiederherstellungs-E-Mail-Konto Andernfalls können Sie keine temporären Wiederherstellungs-Codes verwenden, die an dieses Konto gesendet wurden.

1. Aktivieren Sie das Kontrollkästchen zur Bestätigung und wählen Sie **[!UICONTROL Submit]** aus, um den Einrichtungsprozess der Zwei-Faktor-Authentifizierung abzuschließen.

   An die von Ihnen angegebene Wiederherstellungs-E-Mail wird eine E-Mail-Benachrichtigung gesendet, um zu bestätigen, dass eine bestimmte E-Mail-Adresse als Wiederherstellungs-E-Mail für den Erhalt eines temporären Wiederherstellungs-Codes gespeichert ist.

## Zwei-Faktor-Authentifizierung deaktivieren

>[!IMPORTANT]
>
>Wenn die Sicherheitsrichtlinie Ihres Unternehmens eine Multi-Faktor-Authentifizierung für Adobe Commerce-Konten erfordert, können Sie die Zwei-Faktor-Authentifizierung nicht deaktivieren.

1. Navigieren Sie zum [!DNL Commerce] [Konto-Anmeldung](https://account.magento.com/customer/account/login){:target="_blank"}.

1. Geben Sie Ihren Benutzernamen und Ihr Passwort ein und wählen Sie dann **[!UICONTROL Login]** aus.

1. Schließen Sie den Anmeldevorgang mit einer der zuvor beschriebenen Zwei-Faktor-Authentifizierungsmethoden ab.

1. Wählen Sie im linken Navigationsbereich die Option **[!UICONTROL Account Settings]** und darunter **[!UICONTROL Two-factor Authentication]** aus.

1. Wählen Sie **[!UICONTROL Disable]** aus, um den TFA-Deaktivierungsprozess zu starten.

1. Geben Sie die an Ihre E-Mail gesendeten **[!UICONTROL Verification Code]** ein und wählen Sie **[!UICONTROL Verify Code]** aus, um fortzufahren.

1. Aktivieren Sie das Kontrollkästchen Bestätigung und wählen Sie **[!UICONTROL Submit]** aus, um die Deaktivierung für die Zwei-Faktor-Authentifizierung abzuschließen.

   Das System sendet eine E-Mail-Bestätigung, die angibt, dass TFA in Ihrem [!DNL Commerce]-Konto deaktiviert wurde.

   ![TFA deaktivieren](./assets/2fa-disable.png){width="400"}
