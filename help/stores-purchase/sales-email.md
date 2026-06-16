---
title: Verkaufs-E-Mails
description: Erfahren Sie, wie Sie Verkaufs-E-Mails konfigurieren, um Kunden über ihre Bestellungen zu informieren.
exl-id: b205dc61-08cc-4783-810c-686ccf2ba300
feature: Communications, Orders
TQID: https://experienceleague.adobe.com/M9-GhmO0XeRC9sgZmQXpv759NN-5cM92Bd8ZxxM96yg
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 436
ht-degree: 0%

---

# Verkaufs-E-Mails

Mehrere E-Mail-Nachrichten werden durch die Ereignisse im Zusammenhang mit einer Bestellung ausgelöst und die Konfiguration ist ähnlich. Stellen Sie sicher, dass Sie den Store-Kontakt, der als Absender der Nachricht angezeigt wird, die zu verwendende E-Mail-Vorlage und alle anderen Personen, die eine Kopie der Nachricht erhalten sollen, identifizieren. Verkaufs-E-Mails können gesendet werden, wenn sie durch ein Ereignis ausgelöst werden, oder nach einem vorab festgelegten Intervall.

![Verkaufskonfiguration - Verkaufs-E-Mails](./assets/config-sales-sales-email-full.png){width="600" zoomable="yes"}

## Schritt 1. E-Mail-Vorlagen aktualisieren

Stellen Sie sicher, dass Sie die Vorlage [E-Mail](../systems/email-template-custom.md#header-template)Kopfzeile) aktualisieren, damit sie Ihre Marke und die anderen E-Mail-Vorlagen nach Bedarf widerspiegelt. Eine vollständige Liste der Vorlagen finden Sie unter [E-Mail-](../systems/email-templates.md).

## Schritt 2. Übertragungsart auswählen

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Sales]** und wählen Sie **[!UICONTROL Sales Emails]**.

1. Erweitern Sie bei Bedarf ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL General Settings]** .

   ![Verkaufskonfiguration - Allgemeine Einstellungen für Verkaufs-E-Mails](../configuration-reference/sales/assets/sales-emails-general-settings.png){width="600" zoomable="yes"}

   Standardmäßig ist für das asynchrone Senden `Disable` festgelegt. Deaktivieren Sie das Kontrollkästchen **[!UICONTROL Use system value]**, um die Systemeinstellung zu ändern, und legen Sie **[!UICONTROL Asynchronous sending]** auf einen der folgenden Werte fest:

   - `Disable` - Sendet eine Verkaufs-E-Mail, wenn sie durch ein Ereignis ausgelöst wird.
   - `Enable` - Sendet Verkaufs-E-Mails in vorab festgelegten, regelmäßigen Abständen.

   Der Adobe Commerce-Support empfiehlt die Aktivierung des asynchronen Versands, um die Leistung bei der Bestellplatzierung zu verbessern. Siehe [Best Practices für die Konfiguration der Auftragsverarbeitung](https://experienceleague.adobe.com/docs/commerce-operations/implementation-playbook/best-practices/maintenance/order-processing-configuration.html) in der Wissensdatenbank zum Adobe Commerce-Support.

## Schritt 3. Füllen Sie die Details für jede Verkaufs-E-Mail-Nachricht aus

1. Erweitern Sie bei Bedarf ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Order]** .

   ![Verkaufskonfiguration - E-Mail-Bestellung](../configuration-reference/sales/assets/sales-emails-order.png){width="600" zoomable="yes"}

1. Stellen Sie sicher, dass **[!UICONTROL Enabled]** auf `Yes` (Standard) gesetzt ist.

1. Legen Sie **[!UICONTROL New Order Confirmation Email]** auf den Store-Kontakt fest, der als Absender der Nachricht angezeigt wird.

1. Legen Sie **[!UICONTROL New Order Confirmation Template]** auf die Vorlage fest, die für die E-Mail verwendet wird, die an registrierte Kunden gesendet wird.

1. Legen Sie **[!UICONTROL New Order Confirmation Template for Guest]** auf die Vorlage fest, die für die E-Mail verwendet wird, die an Gäste gesendet wird, die kein Konto bei Ihrem Geschäft haben.

1. Geben Sie **[!UICONTROL Send Order Email Copy To]** die E-Mail-Adresse jeder Person ein, die eine Kopie der neuen E-Mail-Bestellung erhalten soll.

   Wenn Sie eine Kopie an mehrere Empfänger senden, trennen Sie jede Adresse durch ein Komma.

1. Legen Sie **[!UICONTROL Send Order Email Copy Method]** auf eine der folgenden Einstellungen fest:

   - `Bcc` - Sendet eine _Blinde Höflichkeitskopie_ indem der Empfänger in die Kopfzeile derselben E-Mail eingefügt wird, die an den Kunden gesendet wird. Der BCC-Empfänger ist für den Kunden nicht sichtbar.
   - `Separate Email` - Sendet die Kopie als separate E-Mail.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Order Comments]** und wiederholen Sie diese Schritte.

   ![Verkaufskonfiguration - E-Mail-Bestellkommentare für den Verkauf](../configuration-reference/sales/assets/sales-emails-order-comments.png){width="600" zoomable="yes"}

1. Schließen Sie die Konfiguration für die verbleibenden Verkaufs-E-Mail-Typen ab:

   - **[!UICONTROL Invoice]** / **[!UICONTROL Invoice Comments]**
   - **[!UICONTROL Shipment]** / **[!UICONTROL Shipment Comments]**
   - **[!UICONTROL Credit Memo]** / **[!UICONTROL Credit Memo Comments]**

1. Klicken Sie abschließend auf **[!UICONTROL Save Config]**.

   Wenn Sie dazu aufgefordert werden[&#x200B; klicken Sie auf den Link &#x200B;](../systems/cache-management.md)Cache-Verwaltung“ in der Nachricht oben im Arbeitsbereich und löschen Sie alle ungültigen Caches.
