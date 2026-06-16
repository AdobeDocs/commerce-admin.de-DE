---
title: Konfigurieren von Geschenkregistrierungen
description: Erfahren Sie, wie Sie Geschenkregistrierungen aktivieren und die zugehörigen E-Mail-Benachrichtigungen konfigurieren.
exl-id: 48193621-731d-4640-8ea8-5b201915cdf1
feature: Gift, Storefront, Configuration
TQID: https://experienceleague.adobe.com/a7DRiAPSkWhBIPdXPXnH3HB1uw9d4WY4vXOtfgg9kRY
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: bd989d82-1e15-4534-88db-f1f51dd77ffaid: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: b5520579-b31f-4df7-9281-f0d9f91e2edcid: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 358
ht-degree: 0%

---

# Konfigurieren von Geschenkregistrierungen

{{ee-feature}}

Bevor Sie Ihren Kunden Geschenkregistrierungen anbieten können, müssen Sie Geschenkregistrierungen aktivieren und die entsprechenden E-Mail-Benachrichtigungen konfigurieren. Adobe Commerce sendet die folgenden E-Mail-Benachrichtigungen als Reaktion auf Ereignisse im Workflow zur Geschenkregistrierung.

- Wenn eine neue Geschenkregistrierung erstellt wird, wird eine E-Mail mit einem Link zur Registrierung an den Besitzer gesendet, die freigegeben werden kann.
- Optional kann der Store eine Benachrichtigung mit einem Link zur Geschenkregistrierung an Freunde und Familie des Besitzers der Geschenkregistrierung senden.
- Der Besitzer wird benachrichtigt, wenn Artikel aus der Geschenkregistrierung gekauft werden, aber nicht den Käufer.

Adobe Commerce verfügt über vordefinierte Vorlagen für jede dieser E-Mail-Nachrichten, die für Ihre Marke angepasst werden können.

## Schritt 1. Aktivieren von Geschenkregistern

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Customers]** und wählen Sie **[!UICONTROL Gift Registry]**

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL General Options]** und führen Sie folgende Schritte aus:

   ![Kundenkonfiguration - Geschenkregistrierung allgemein](../configuration-reference/customers/assets/gift-registry-general-options.png){width="600" zoomable="yes"}

   - Die Geschenkregistrierung ist standardmäßig aktiviert. Falls erforderlich, setzen Sie **[!UICONTROL Enable Gift Registry]** auf `Yes`.

   - Geben Sie **[!UICONTROL Maximum Registrants]** die maximale Anzahl von Personen ein, die zur Teilnahme an einem Geschenkregistrierungs-Event eingeladen werden können.

## Schritt 2. Konfigurieren von E-Mail-Benachrichtigungen

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Owner Notification]** und führen Sie folgende Schritte aus:

   ![Kundenkonfiguration - Benachrichtigung zum Besitzer der Geschenkregistrierung](../configuration-reference/customers/assets/gift-registry-owner-notification.png){width="600" zoomable="yes"}

   - Wählen Sie die **[!UICONTROL Email Template]** aus, die Besitzer von Geschenkregistrierungen benachrichtigt, wenn ihre Registrierungen erstellt werden.

   - Wählen Sie den [Store-](../getting-started/store-details.md#store-email-addresses)), der als **[!UICONTROL Email Sender]** der Nachricht angezeigt wird.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Gift Registry Sharing]** und führen Sie folgende Schritte aus:

   ![Kundenkonfiguration - Freigabe der Geschenkregistrierung](../configuration-reference/customers/assets/gift-registry-gift-registry-sharing.png){width="600" zoomable="yes"}

   - Wählen Sie die **[!UICONTROL Email Template]** aus, die Empfänger von Geschenkregistrierungen benachrichtigt, wenn eine Registrierung für sie freigegeben wird.

   - Wählen Sie die Store-ID aus, die als **[!UICONTROL Email Sender]** der Nachricht angezeigt wird.

   - Geben Sie **[!UICONTROL Maximum Sent Emails Threshold]** die maximale Anzahl von E-Mails ein, die gleichzeitig gesendet werden können.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Gift Registry Update]** und führen Sie folgende Schritte aus:

   ![Kundenkonfiguration - Aktualisierung der Geschenkregistrierung](../configuration-reference/customers/assets/gift-registry-gift-registry-update.png){width="600" zoomable="yes"}

   - Wählen Sie die **[!UICONTROL Email Template]** aus, die Besitzer von Geschenkregistrierungen über Änderungen an der Registrierung benachrichtigt.

   - Wählen Sie die Store-ID aus, die als **[!UICONTROL Email Sender]** der Nachricht angezeigt wird.

1. Klicken Sie abschließend auf **[!UICONTROL Save Config]**.

1. Aktualisieren Sie den Cache, wenn Sie dazu aufgefordert werden.

   Nachdem der Cache aktualisiert wurde, wird die Geschenkregistrierung im Menü Stores unter Andere Einstellungen angezeigt und wird in Kundenkonten verfügbar.
