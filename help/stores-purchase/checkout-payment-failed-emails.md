---
title: Benachrichtigung über Zahlungsausfall
description: Erfahren Sie, wie Sie die E-Mail-Kommunikation für eine Zahlungsmethode konfigurieren, bei der eine Transaktion nicht abgeschlossen werden kann.
exl-id: c64a4463-64d5-4dad-a8ad-13bfb141b65f
feature: Payments, Communications
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '235'
ht-degree: 0%

---

# Benachrichtigung über Zahlungsausfall

Eine Benachrichtigung wird an den Store-Ansprechpartner oder einen Administrator gesendet, wenn die beim Checkout ausgewählte Zahlungsmethode die Transaktion nicht abschließen kann.

## Schritt 1: E-Mail-Vorlage aktualisieren

Stellen Sie sicher, dass Sie die benötigte E-Mail-Vorlage entsprechend Ihrer Marke aktualisiert haben. Eine vollständige Liste der Vorlagen finden Sie unter [E-Mail-Vorlagenliste](../systems/email-templates.md#email-template-list).

## Schritt 2: Konfigurieren Sie fehlgeschlagene E-Mails zur Zahlung.

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich den Wert **[!UICONTROL Sales]** und wählen Sie **[!UICONTROL Checkout]** aus.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) im Abschnitt **[!UICONTROL Payment Failed Emails]** .

   ![Zahlungsfehler bei E-Mails](../configuration-reference/sales/assets/checkout-payment-failed-emails.png){width="600" zoomable="yes"}

1. Legen Sie die Optionen für fehlgeschlagene E-Mails zum Bezahlen fest:

   - Setzen Sie **[!UICONTROL Payment Failed Email Sender]** auf den Store-Kontakt, der als Absender der Nachricht angezeigt wird.
   - Setzen Sie **[!UICONTROL Payment Failed Email Receiver]** auf den Store-Kontakt, der Benachrichtigungen über fehlgeschlagene E-Mail-Übertragungen erhält.
   - Setzen Sie **[!UICONTROL Payment Failed Template]** auf die Vorlage, die für die E-Mail verwendet wird, die gesendet wird, wenn die Zahlungsmethode beim Checkout fehlschlägt.

1. Geben Sie für &quot;**[!UICONTROL Send Payment Failed Email Copy To]**&quot; die E-Mail-Adresse eines jeden an, der eine Kopie der Benachrichtigung über einen Zahlungsfehler erhalten soll.

   Wenn Sie eine Kopie an mehrere Empfänger senden, trennen Sie jede Adresse durch ein Komma.

1. Setzen Sie **[!UICONTROL Payment Failed Copy Method]** auf einen der folgenden Werte:

   - `Bcc` - Sendet eine _Blinde höfliche Kopie_, indem der Empfänger in die Kopfzeile derselben E-Mail eingefügt wird, die an den Kunden gesendet wird. Der BCC-Empfänger ist für den Kunden nicht sichtbar.
   - `Separate Email` - Sendet die Kopie als separate E-Mail.

1. Klicken Sie auf **[!UICONTROL Save Config]**.
