---
title: Kundenanmeldung
description: Die Benutzeranmeldefunktion in der Storefront ermöglicht einen einfachen Zugriff auf die Kundenkonten.
exl-id: eadcc15a-a052-4213-a818-d5b248d974d2
feature: Customers, Storefront
source-git-commit: 7de285d4cd1e25ec890f1efff9ea7bdf2f0a9144
workflow-type: tm+mt
source-wordcount: '381'
ht-degree: 0%

---

# Kundenanmeldung

Kunden haben von jeder Seite in Ihrem Geschäft aus einfachen Zugriff auf ihre Konten. Je nach [Konfiguration](../customers/account-options-new.md)können Kunden zu ihrem Konto-Dashboard weitergeleitet werden oder nach der Anmeldung bei ihren Konten mit dem Einkauf fortfahren.

Wenn [CAPTCHA](../systems/security-captcha.md) in der Konfiguration aktiviert ist, muss die Person einen Test, der überprüft, ob sie menschlich ist, ordnungsgemäß durchführen, bevor sie Zugriff auf ihre Konten erhält.

Wenn Kunden ihr Passwort vergessen, wird ein Link zum Zurücksetzen an die E-Mail-Adresse gesendet, die dem Konto zugeordnet ist. Die [Kennwortoptionen](../customers/password-options.md) -Konfiguration steuert das Kundenerlebnis bei Anmeldeversuchen:

- Die Häufigkeit, mit der ein Kunde versuchen kann, ein Kennwort einzugeben
- Die Anzahl von Minuten zwischen Versuchen
- Die Anzahl aller Versuche, bevor das Konto gesperrt wird
- Die Länge des Sperrvorgangs

![Anmelde-Link auf der Storefront-Kopfzeile](assets/storefront-sign-in-create-account.png){width="700" zoomable="yes"}

## Bei einem Kundenkonto anmelden

1. In der Kopfzeile des Stores klickt der Kunde auf **[!UICONTROL Sign in]**.

   ![Kundenanmeldung](assets/login.png){width="700" zoomable="yes"}

1. Endet ihre **[!UICONTROL Email]** Adresse und **[!UICONTROL Password]**.

1. Klicks **[!UICONTROL Sign in]**.

   >[!IMPORTANT]
   >
   >Wenn der Kunde sein Kennwort nicht speichern kann, kann er auf **[!UICONTROL Forgot Your Password?]** und folgen Sie dem [instructions](../customers/password-reset.md) , um das Kennwort zurückzusetzen.

## Stellen Sie die Umleitung auf das Konto-Dashboard ein, nachdem Sie sich beim Kunden angemeldet haben

Sie können den Store so konfigurieren, dass Kunden nach der Anmeldung zum Konto-Dashboard weitergeleitet werden oder dass sie weiterhin einkaufen können.

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Customers]** und wählen **[!UICONTROL Customer Configuration]**.

1. Erweitern Sie die **[!UICONTROL Login Options]** Abschnitt.

1. Satz **[!UICONTROL Redirect Customer to Account Dashboard after Logging in]** auf einen der folgenden Werte zu:

   - `Yes` - Das Konto-Dashboard wird angezeigt, wenn sich Kunden bei ihren Konten anmelden.
   - `No` - Kunden können nach der Anmeldung bei ihren Konten weiterhin einkaufen.

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save Config]**.

## Mit Amazon anmelden

Für Stores mit konfigurierten [!DNL Amazon Pay] und [!DNL Login with Amazon] -Integration, können sich Kunden bei ihrem Amazon-Käuferkonto anmelden.

1. In der Kopfzeile des Stores klickt der Kunde auf **[!UICONTROL Sign in]**.

1. Klicks **[!UICONTROL Login with Amazon]**.

   ![Mit Amazon anmelden](assets/amazon-pay.png){width="700" zoomable="yes"}

1. Wenn der Kunde aufgefordert wird, sich anzumelden, gibt er die **[!UICONTROL email address]** und **[!UICONTROL password]** für ihr Amazon-Käuferkonto.

   ![Amazon-Anmeldedaten eingeben](assets/amazon-popup1.png){width="700" zoomable="yes"}

1. Um Amazon die Berechtigung zu erteilen, die folgenden Informationen aus ihrem Konto für den Store freizugeben, wenn Käufe verarbeitet werden, klicken Sie auf **Okay**.

   - Name
   - Email-Adresse
   - Versandadressen

   ![Berechtigung zum Freigeben von Daten gewähren](assets/amazon-popup2.png){width="700" zoomable="yes"}

## Abmelden von einem Kundenkonto

1. In der oberen rechten Ecke neben  _[!UICONTROL Welcome, Customer Name!]_, klickt der Kunde auf die **[!UICONTROL v]**Menüauswahl.

1. Auswählen **[!UICONTROL Sign Out]**.

Nach dem Abmelden wird der Kunde auf die Startseite umgeleitet.
