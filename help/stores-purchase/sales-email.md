---
title: Verkaufs-E-Mails
description: Erfahren Sie, wie Sie E-Mails für den Vertrieb konfigurieren, um Kunden Mitteilungen über ihre Bestellungen zu ermöglichen.
exl-id: b205dc61-08cc-4783-810c-686ccf2ba300
feature: Communications, Orders
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '424'
ht-degree: 0%

---

# Verkaufs-E-Mails

Mehrere E-Mail-Nachrichten werden durch die Ereignisse ausgelöst, die sich auf eine Bestellung beziehen, und die Konfiguration ist ähnlich. Stellen Sie sicher, dass Sie den Store-Kontakt identifizieren, der als Absender der Nachricht erscheint, die zu verwendende E-Mail-Vorlage und alle anderen Personen, die eine Kopie der Nachricht erhalten sollen. Verkaufs-E-Mails können gesendet werden, wenn sie durch ein Ereignis oder ein vordefiniertes Intervall ausgelöst werden.

![Verkaufskonfiguration - E-Mails zum Vertrieb](./assets/config-sales-sales-email-full.png){width="600" zoomable="yes"}

## Schritt 1. E-Mail-Vorlagen aktualisieren

Aktualisieren Sie unbedingt die Vorlage [E-Mail-Header](../systems/email-template-custom.md#header-template) , damit sie Ihrer Marke und den anderen E-Mail-Vorlagen entspricht. Eine vollständige Liste der Vorlagen finden Sie unter [E-Mail-Vorlagen](../systems/email-templates.md).

## Schritt 2. Übertragungsart auswählen

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich den Wert **[!UICONTROL Sales]** und wählen Sie **[!UICONTROL Sales Emails]** aus.

1. Erweitern Sie ggf. den Abschnitt ![Erweiterungsauswahl](../assets/icon-display-expand.png) um den Abschnitt **[!UICONTROL General Settings]**.

   ![Verkaufskonfiguration - Allgemeine E-Mail-Einstellungen für Vertrieb](../configuration-reference/sales/assets/sales-emails-general-settings.png){width="600" zoomable="yes"}

   Standardmäßig ist der asynchrone Versand auf `Disable` eingestellt. Um die Systemeinstellung zu ändern, deaktivieren Sie das Kontrollkästchen **[!UICONTROL Use system value]** und legen Sie **[!UICONTROL Asynchronous sending]** auf einen der folgenden Werte fest:

   - `Disable` - Sendet eine Verkaufs-E-Mail, wenn diese durch ein Ereignis ausgelöst wird.
   - `Enable` - Sendet Verkaufs-E-Mails in vorbestimmten, regelmäßigen Abständen.

   Der Adobe Commerce-Support empfiehlt die Aktivierung des asynchronen Versands, um die Bestellplatzierungsleistung zu verbessern. Siehe [Best Practices für die Konfiguration der Auftragsverarbeitung](https://experienceleague.adobe.com/docs/commerce-operations/implementation-playbook/best-practices/maintenance/order-processing-configuration.html) in der Knowledge Base des Adobe Commerce-Supports.

## Schritt 3. Detaillierte Angaben zu den einzelnen E-Mail-Verkaufsnachrichten

1. Erweitern Sie ggf. den Abschnitt ![Erweiterungsauswahl](../assets/icon-display-expand.png) um den Abschnitt **[!UICONTROL Order]**.

   ![Verkaufskonfiguration - E-Mail-Bestellung für Vertrieb](../configuration-reference/sales/assets/sales-emails-order.png){width="600" zoomable="yes"}

1. Stellen Sie sicher, dass **[!UICONTROL Enabled]** auf `Yes` gesetzt ist (Standard).

1. Setzen Sie **[!UICONTROL New Order Confirmation Email]** auf den Store-Kontakt, der als Absender der Nachricht angezeigt wird.

1. Setzen Sie **[!UICONTROL New Order Confirmation Template]** auf die Vorlage, die für die E-Mail verwendet wird, die an registrierte Kunden gesendet wird.

1. Setzen Sie **[!UICONTROL New Order Confirmation Template for Guest]** auf die Vorlage, die für die E-Mail verwendet wird, die an Gäste gesendet wird, die kein Konto bei Ihrem Geschäft haben.

1. Geben Sie für &quot;**[!UICONTROL Send Order Email Copy To]**&quot;die E-Mail-Adresse eines jeden an, der eine Kopie der neuen Bestell-E-Mail erhalten soll.

   Wenn Sie eine Kopie an mehrere Empfänger senden, trennen Sie jede Adresse durch ein Komma.

1. Setzen Sie **[!UICONTROL Send Order Email Copy Method]** auf einen der folgenden Werte:

   - `Bcc` - Sendet eine _Blinde höfliche Kopie_, indem der Empfänger in die Kopfzeile derselben E-Mail eingefügt wird, die an den Kunden gesendet wird. Der BCC-Empfänger ist für den Kunden nicht sichtbar.
   - `Separate Email` - Sendet die Kopie als separate E-Mail.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) im Abschnitt **[!UICONTROL Order Comments]** und wiederholen Sie diese Schritte.

   ![Verkaufskonfiguration - Kommentare zu E-Mail-Bestellungen für Vertrieb](../configuration-reference/sales/assets/sales-emails-order-comments.png){width="600" zoomable="yes"}

1. Konfigurieren Sie die restlichen E-Mail-Typen für den Vertrieb:

   - **[!UICONTROL Invoice]** / **[!UICONTROL Invoice Comments]**
   - **[!UICONTROL Shipment]** / **[!UICONTROL Shipment Comments]**
   - **[!UICONTROL Credit Memo]** / **[!UICONTROL Credit Memo Comments]**

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save Config]**.

   Wenn Sie dazu aufgefordert werden, klicken Sie in der Meldung oben im Arbeitsbereich auf den Link [Cache-Verwaltung](../systems/cache-management.md) und löschen Sie alle ungültigen Caches.
