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

Kunden haben von jeder Seite in Ihrem Geschäft aus einfachen Zugriff auf ihre Konten. Abhängig von der [Konfiguration](../customers/account-options-new.md) können Kunden zu ihrem Konto-Dashboard weitergeleitet werden oder nach der Anmeldung bei ihren Konten mit dem Einkaufen fortfahren.

Wenn [CAPTCHA](../systems/security-captcha.md) in der Konfiguration aktiviert ist, muss die Person einen Test ordnungsgemäß durchführen, um sicherzustellen, dass sie menschlich ist, bevor sie Zugriff auf ihre Konten erhält.

Wenn Kunden ihr Passwort vergessen, wird ein Link zum Zurücksetzen an die E-Mail-Adresse gesendet, die dem Konto zugeordnet ist. Die Konfiguration [Kennwortoptionen](../customers/password-options.md) steuert das Kundenerlebnis bei Anmeldeversuchen:

- Die Häufigkeit, mit der ein Kunde versuchen kann, ein Kennwort einzugeben
- Die Anzahl von Minuten zwischen Versuchen
- Die Anzahl aller Versuche, bevor das Konto gesperrt wird
- Die Länge des Sperrvorgangs

![Anmelde-Link auf der Storefront-Kopfzeile](assets/storefront-sign-in-create-account.png){width="700" zoomable="yes"}

## Bei einem Kundenkonto anmelden

1. In der Kopfzeile des Stores klickt der Kunde auf **[!UICONTROL Sign in]**.

   ![Kundenanmeldung](assets/login.png){width="700" zoomable="yes"}

1. Fügt ihre **[!UICONTROL Email]** -Adresse und ihre **[!UICONTROL Password]** ein.

1. Klicks **[!UICONTROL Sign in]**.

   >[!IMPORTANT]
   >
   >Wenn er sich sein Kennwort nicht merken kann, kann der Kunde auf **[!UICONTROL Forgot Your Password?]** klicken und den [Anweisungen](../customers/password-reset.md) folgen, um das Kennwort zurückzusetzen.

## Stellen Sie die Umleitung auf das Konto-Dashboard ein, nachdem Sie sich beim Kunden angemeldet haben

Sie können den Store so konfigurieren, dass Kunden nach der Anmeldung zum Konto-Dashboard weitergeleitet werden oder dass sie weiterhin einkaufen können.

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich den Wert **[!UICONTROL Customers]** und wählen Sie **[!UICONTROL Customer Configuration]** aus.

1. Erweitern Sie den Abschnitt **[!UICONTROL Login Options]** .

1. Setzen Sie **[!UICONTROL Redirect Customer to Account Dashboard after Logging in]** auf einen der folgenden Werte:

   - `Yes` - Das Konto-Dashboard wird angezeigt, wenn sich Kunden bei ihren Konten anmelden.
   - `No` - Kunden können nach dem Anmelden bei ihren Konten weiterhin einkaufen.

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save Config]**.

## Mit Amazon anmelden

Bei Stores mit konfigurierter Integration von [!DNL Amazon Pay] und [!DNL Login with Amazon] können sich Kunden bei ihrem Amazon-Käuferkonto anmelden.

1. In der Kopfzeile des Stores klickt der Kunde auf **[!UICONTROL Sign in]**.

1. Klicks **[!UICONTROL Login with Amazon]**.

   ![Anmeldung bei Amazon](assets/amazon-pay.png){width="700" zoomable="yes"}

1. Wenn der Kunde dazu aufgefordert wird, sich anzumelden, gibt er für sein Amazon-Käuferkonto den Wert **[!UICONTROL email address]** und den Wert **[!UICONTROL password]** ein.

   ![Amazon-Anmeldedaten eingeben](assets/amazon-popup1.png){width="700" zoomable="yes"}

1. Um Amazon die Berechtigung zu erteilen, die folgenden Informationen aus ihrem Konto beim Verarbeiten von Käufen für den Store freizugeben, klicken Sie auf **OK**.

   - Name
   - Email-Adresse
   - Versandadressen

   ![Erteilen der Berechtigung zum Freigeben von Daten](assets/amazon-popup2.png){width="700" zoomable="yes"}

## Abmelden von einem Kundenkonto

1. In der oberen rechten Ecke neben _[!UICONTROL Welcome, Customer Name!]_klickt der Kunde auf die Menüauswahl **[!UICONTROL v]**.

1. Wählen Sie **[!UICONTROL Sign Out]** aus.

Nach dem Abmelden wird der Kunde auf die Startseite umgeleitet.
