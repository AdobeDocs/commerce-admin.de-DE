---
title: Benachrichtigung über Zahlungsausfall
description: Erfahren Sie, wie Sie die E-Mail-Kommunikation für eine Zahlungsmethode konfigurieren, bei der eine Transaktion nicht abgeschlossen werden kann.
exl-id: c64a4463-64d5-4dad-a8ad-13bfb141b65f
feature: Payments, Communications
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '233'
ht-degree: 0%

---

# Benachrichtigung über Zahlungsausfall

Eine Benachrichtigung wird an den Store-Ansprechpartner oder einen Administrator gesendet, wenn die beim Checkout ausgewählte Zahlungsmethode die Transaktion nicht abschließen kann.

## Schritt 1: E-Mail-Vorlage aktualisieren

Stellen Sie sicher, dass Sie die benötigte E-Mail-Vorlage entsprechend Ihrer Marke aktualisiert haben. Eine vollständige Liste der Vorlagen finden Sie unter [E-Mail-Vorlagenliste](../systems/email-templates.md#email-template-list).

## Schritt 2: Konfigurieren Sie fehlgeschlagene E-Mails zur Zahlung.

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Sales]** und wählen **[!UICONTROL Checkout]**.

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL Payment Failed Emails]** Abschnitt.

   ![Zahlung fehlgeschlagener E-Mails](../configuration-reference/sales/assets/checkout-payment-failed-emails.png){width="600" zoomable="yes"}

1. Legen Sie die Optionen für fehlgeschlagene E-Mails zum Bezahlen fest:

   - Satz **[!UICONTROL Payment Failed Email Sender]** an den Store-Kontakt, der als Absender der Nachricht angezeigt wird.
   - Satz **[!UICONTROL Payment Failed Email Receiver]** an den Store-Kontakt, der Benachrichtigungen über fehlgeschlagene E-Mail-Übertragungen erhalten soll.
   - Satz **[!UICONTROL Payment Failed Template]** an die Vorlage weitergeleitet werden, die für die E-Mail verwendet wird, die gesendet wird, wenn die Zahlungsmethode während des Auscheckens fehlschlägt.

1. Für **[!UICONTROL Send Payment Failed Email Copy To]** Geben Sie die E-Mail-Adresse eines Empfängers an, der eine Kopie der Benachrichtigung über den Zahlungsausfall erhalten soll.

   Wenn Sie eine Kopie an mehrere Empfänger senden, trennen Sie jede Adresse durch ein Komma.

1. Satz **[!UICONTROL Payment Failed Copy Method]** auf einen der folgenden Werte zu:

   - `Bcc` - Sendet eine _Blind Höflichkeitskopie_ indem der Empfänger in die Kopfzeile derselben E-Mail eingefügt wird, die an den Kunden gesendet wird. Der BCC-Empfänger ist für den Kunden nicht sichtbar.
   - `Separate Email` - Sendet die Kopie als separate E-Mail.

1. Klicken **[!UICONTROL Save Config]**.
