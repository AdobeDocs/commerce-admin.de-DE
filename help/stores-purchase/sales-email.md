---
title: Verkaufs-E-Mails
description: Erfahren Sie, wie Sie E-Mails für den Vertrieb konfigurieren, um Kunden Mitteilungen über ihre Bestellungen zu ermöglichen.
exl-id: b205dc61-08cc-4783-810c-686ccf2ba300
feature: Communications, Orders
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '428'
ht-degree: 0%

---

# Verkaufs-E-Mails

Mehrere E-Mail-Nachrichten werden durch die Ereignisse ausgelöst, die sich auf eine Bestellung beziehen, und die Konfiguration ist ähnlich. Stellen Sie sicher, dass Sie den Store-Kontakt identifizieren, der als Absender der Nachricht erscheint, die zu verwendende E-Mail-Vorlage und alle anderen Personen, die eine Kopie der Nachricht erhalten sollen. Verkaufs-E-Mails können gesendet werden, wenn sie durch ein Ereignis oder ein vordefiniertes Intervall ausgelöst werden.

![Vertriebskonfiguration - Verkaufs-E-Mails](./assets/config-sales-sales-email-full.png){width="600" zoomable="yes"}

## Schritt 1. E-Mail-Vorlagen aktualisieren

Aktualisieren Sie unbedingt die [E-Mail-Header](../systems/email-template-custom.md#header-template) -Vorlage verwenden, um Ihre Marke und die anderen E-Mail-Vorlagen nach Bedarf widerzuspiegeln. Eine vollständige Liste der Vorlagen finden Sie unter [E-Mail-Vorlagen](../systems/email-templates.md).

## Schritt 2. Übertragungsart auswählen

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Sales]** und wählen **[!UICONTROL Sales Emails]**.

1. Erweitern Sie ggf. ![Erweiterungsauswahl](../assets/icon-display-expand.png) die  **[!UICONTROL General Settings]** Abschnitt.

   ![Vertriebskonfiguration - Allgemeine Einstellungen für Verkaufs-E-Mail](../configuration-reference/sales/assets/sales-emails-general-settings.png){width="600" zoomable="yes"}

   Standardmäßig ist der asynchrone Versand auf `Disable`. Um die Systemeinstellung zu ändern, löschen Sie die **[!UICONTROL Use system value]** Kontrollkästchen und festlegen **[!UICONTROL Asynchronous sending]** auf einen der folgenden Werte zu:

   - `Disable` - Sendet Verkaufs-E-Mails, wenn diese durch ein Ereignis ausgelöst werden.
   - `Enable` - Sendet Verkaufs-E-Mails in vordefinierten, regelmäßigen Abständen.

   Der Adobe Commerce-Support empfiehlt die Aktivierung des asynchronen Versands, um die Bestellplatzierungsleistung zu verbessern. Siehe [Best Practices für die Auftragsverarbeitung konfigurieren](https://experienceleague.adobe.com/docs/commerce-operations/implementation-playbook/best-practices/maintenance/order-processing-configuration.html) in der Knowledge Base zur Adobe Commerce-Unterstützung.

## Schritt 3. Detaillierte Angaben zu den einzelnen E-Mail-Verkaufsnachrichten

1. Erweitern Sie ggf. ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL Order]** Abschnitt.

   ![Vertriebskonfiguration - E-Mail-Bestellung für Vertrieb](../configuration-reference/sales/assets/sales-emails-order.png){width="600" zoomable="yes"}

1. Stellen Sie sicher, dass **[!UICONTROL Enabled]** auf `Yes` (Standard).

1. Satz **[!UICONTROL New Order Confirmation Email]** an den Store-Kontakt, der als Absender der Nachricht angezeigt wird.

1. Satz **[!UICONTROL New Order Confirmation Template]** der Vorlage, die für die E-Mail verwendet wird, die an registrierte Kunden gesendet wird.

1. Satz **[!UICONTROL New Order Confirmation Template for Guest]** der Vorlage, die für die E-Mail verwendet wird, die an Gäste gesendet wird, die kein Konto bei Ihrem Geschäft haben.

1. Für **[!UICONTROL Send Order Email Copy To]** Geben Sie die E-Mail-Adresse eines jeden Empfängers ein, der eine Kopie der neuen Bestell-E-Mail erhalten soll.

   Wenn Sie eine Kopie an mehrere Empfänger senden, trennen Sie jede Adresse durch ein Komma.

1. Satz **[!UICONTROL Send Order Email Copy Method]** auf einen der folgenden Werte zu:

   - `Bcc` - Sendet eine _Blind Höflichkeitskopie_ indem der Empfänger in die Kopfzeile derselben E-Mail eingefügt wird, die an den Kunden gesendet wird. Der BCC-Empfänger ist für den Kunden nicht sichtbar.
   - `Separate Email` - Sendet die Kopie als separate E-Mail.

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL Order Comments]** und wiederholen Sie diese Schritte.

   ![Vertriebskonfiguration - Kommentare zu E-Mails mit Bestellbestätigungen](../configuration-reference/sales/assets/sales-emails-order-comments.png){width="600" zoomable="yes"}

1. Konfigurieren Sie die restlichen E-Mail-Typen für den Vertrieb:

   - **[!UICONTROL Invoice]** / **[!UICONTROL Invoice Comments]**
   - **[!UICONTROL Shipment]** / **[!UICONTROL Shipment Comments]**
   - **[!UICONTROL Credit Memo]** / **[!UICONTROL Credit Memo Comments]**

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save Config]**.

   Klicken Sie bei Aufforderung auf das [Cacheverwaltung](../systems/cache-management.md) in der Nachricht am oberen Rand des Arbeitsbereichs klicken und alle ungültigen Caches löschen.
