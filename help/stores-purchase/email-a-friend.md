---
title: Freund per E-Mail senden
description: Erfahren Sie, wie Sie einen E-Mail-Link bereitstellen, über den Ihre Kunden Links zu Produkten mit ihren Freunden teilen können.
exl-id: 46cf9994-6490-4cb4-85b7-9a7cab7783e0
feature: Storefront, Configuration
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '410'
ht-degree: 0%

---

# Freund per E-Mail senden

Über den Link E-Mail können Ihre Kunden Links zu Produkten mit ihren Freunden teilen. Im Demo-Luma-Store wird der E-Mail-Link als Umschlagsymbol angezeigt. Die Nachrichtenvorlage kann für Ihre Stimme und Marke angepasst werden. Um Spam zu verhindern, können Sie die Anzahl der Empfänger für jede E-Mail und die Anzahl der Produkte begrenzen, die über einen Zeitraum von einer Stunde freigegeben werden können.

![Beispiel-Storefront - E-Mail an einen Freund senden](./assets/storefront-email-a-friend.png){width="700" zoomable="yes"}

## E-Mail-a-Freund konfigurieren

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich den Wert **[!UICONTROL Catalog]** und wählen Sie **[!UICONTROL Email to a Friend]** aus.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Email Templates]** und legen Sie die Optionen fest:

   ![Katalogkonfiguration - E-Mail-Vorlagen](../configuration-reference/catalog/assets/email-to-a-friend-email-templates.png){width="600" zoomable="yes"}

   Eine ausführliche Beschreibung der einzelnen Konfigurationseinstellungen finden Sie unter [E-Mail-Vorlagen](../configuration-reference/catalog/email-to-a-friend.md) im _Konfigurationshandbuch_.

   Um die Standardeinstellung eines beliebigen Felds zu ändern, deaktivieren Sie das Kontrollkästchen **[!UICONTROL Use system value]** , damit das Feld bearbeitbar wird.

   - Setzen Sie **[!UICONTROL Enabled]** auf `Yes`.

   - Setzen Sie **[!UICONTROL Select Email Template]** auf die Vorlage, die Sie als Basis für die Nachrichten verwenden möchten.

   - Wenn Sie verlangen möchten, dass nur registrierte Kunden E-Mails an Freunde senden können, setzen Sie **[!UICONTROL Allow for Guests]** auf `No`.

   - Geben Sie für &quot;**[!UICONTROL Max Recipients]**&quot;die maximale Anzahl von Freunden an, die auf der Verteilungsliste für eine einzelne Nachricht stehen können.

   - Geben Sie für &quot;**[!UICONTROL Max Products Sent in 1 Hour]**&quot;die maximale Anzahl von Produkten ein, die von einem einzelnen Benutzer mit Freunden über einen Zeitraum von einer Stunde geteilt werden können.

   - Setzen Sie **[!UICONTROL Limit Sending By]** auf eine der folgenden Methoden, um den Absender von E-Mails zu identifizieren:

     `IP Address` - (Empfohlen) Identifiziert den Absender anhand der IP-Adresse des Computers, der zum Senden der E-Mails verwendet wird.

     `Cookie (unsafe)` - Identifiziert den Absender nach Browser-Cookie. Diese Methode ist weniger effektiv, da der Absender das Cookie löschen kann, um die Beschränkung zu umgehen.

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save Config]**.

## E-Mail an einen Freund im Storefront senden

Wenn diese Funktion konfiguriert ist, führen die Store-Kunden die folgenden Schritte aus, um Produktinformationen für Freunde freizugeben.

1. Auf einer Katalogseite klickt der Kunde auf den Link **[!UICONTROL Email]** .

1. Wenn die Funktion nur für registrierte Benutzer konfiguriert ist, führt einen der folgenden Schritte aus:

   - Melden Sie sich bei Ihrem Kundenkonto an.
   - Melden Sie sich für ein neues Konto an.

1. Schließt den **[!UICONTROL Message]** aus und gibt den Empfänger **[!UICONTROL Name]** und **[!UICONTROL Email Address]** ein.

   Bei Bedarf kann der Kunde weitere Empfänger hinzufügen:

   - Klicks **[!UICONTROL Add Invitee]**.

   - Fügt die **[!UICONTROL Name]** und **[!UICONTROL Email Address]** der zusätzlichen Person ein.

     Sie können die Nachricht an so viele zusätzliche Personen senden, wie die Konfiguration zulässt. Sie können die hinzugefügte Einladung entfernen, indem sie auf den Link **[!DNL Remove]** klicken.

1. Wenn die Nachricht gesendet werden kann, klickt auf **[!UICONTROL Send Email]**.

   ![Beispiel-Storefront - E-Mail an einen Freund](./assets/storefront-email-a-friend-form.png){width="700" zoomable="yes"}
