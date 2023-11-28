---
title: Konfigurieren von Geschenkgutscheinen
description: Erfahren Sie, wie Sie Geschenkregistern aktivieren und die entsprechenden E-Mail-Benachrichtigungen konfigurieren.
exl-id: 48193621-731d-4640-8ea8-5b201915cdf1
feature: Gift, Storefront, Configuration
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '356'
ht-degree: 0%

---

# Konfigurieren von Geschenkgutscheinen

{{ee-feature}}

Bevor Sie Ihren Kunden Geschenkgutscheine anbieten können, müssen Sie Geschenkregistern aktivieren und die entsprechenden E-Mail-Benachrichtigungen konfigurieren. Adobe Commerce sendet die folgenden E-Mail-Benachrichtigungen als Reaktion auf Ereignisse im Workflow für die Registrierung von Geschenkgutscheinen.

- Wenn eine neue Geschenkregistrierung erstellt wird, wird eine E-Mail an den Eigentümer mit einem Link zur Registrierung gesendet, der freigegeben werden kann.
- Optional kann der Laden eine Benachrichtigung mit einem Link zur Geschenkregistrierung an Freunde und Familie des Eigentümers der Geschenkregistrierung senden.
- Der Eigentümer wird benachrichtigt, wenn Artikel in der Geschenkregistrierung erworben werden, gibt jedoch nicht den Käufer an.

Adobe Commerce verfügt über vordefinierte Vorlagen für jede dieser E-Mail-Nachrichten, die für Ihre Marke angepasst werden können.

## Schritt 1. Geschenkregister aktivieren

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Customers]** und wählen **[!UICONTROL Gift Registry]**

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL General Options]** und führen Sie folgende Schritte aus:

   ![Kundenkonfiguration - Geschenkregistrierung - Allgemein](../configuration-reference/customers/assets/gift-registry-general-options.png){width="600" zoomable="yes"}

   - Die Gift Registry ist standardmäßig aktiviert. Legen Sie bei Bedarf **[!UICONTROL Enable Gift Registry]** nach `Yes`.

   - Für **[!UICONTROL Maximum Registrants]**, geben Sie die maximale Anzahl von Personen an, die zur Teilnahme an einer Geschenkregistrierung eingeladen werden können.

## Schritt 2. E-Mail-Benachrichtigungen konfigurieren

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL Owner Notification]** und führen Sie folgende Schritte aus:

   ![Kundenkonfiguration - Benachrichtigung des Eigentümers der Geschenkregistrierung](../configuration-reference/customers/assets/gift-registry-owner-notification.png){width="600" zoomable="yes"}

   - Wählen Sie die **[!UICONTROL Email Template]** , die die Eigentümer der Geschenkregistrierung bei der Erstellung ihrer Register informiert.

   - Wählen Sie die [Store-Kontakt](../getting-started/store-details.md#store-email-addresses) , der als **[!UICONTROL Email Sender]** der Nachricht.

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL Gift Registry Sharing]** und führen Sie folgende Schritte aus:

   ![Kundenkonfiguration - Freigabe von Geschenkregistern](../configuration-reference/customers/assets/gift-registry-gift-registry-sharing.png){width="600" zoomable="yes"}

   - Wählen Sie die **[!UICONTROL Email Template]** , die Empfänger der Geschenkregistrierung benachrichtigt, wenn eine Registrierung für sie freigegeben ist.

   - Wählen Sie die Store-Kennung aus, die als **[!UICONTROL Email Sender]** der Nachricht.

   - Für **[!UICONTROL Maximum Sent Emails Threshold]** geben Sie die maximale Anzahl an E-Mails an, die gleichzeitig gesendet werden können.

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL Gift Registry Update]** und führen Sie folgende Schritte aus:

   ![Kundenkonfiguration - Aktualisierung der Geschenkregistrierung](../configuration-reference/customers/assets/gift-registry-gift-registry-update.png){width="600" zoomable="yes"}

   - Wählen Sie die **[!UICONTROL Email Template]** , der die Eigentümer der Geschenkregistrierung über Änderungen an der Registrierung informiert.

   - Wählen Sie die Store-Kennung aus, die als **[!UICONTROL Email Sender]** der Nachricht.

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save Config]**.

1. Wenn Sie dazu aufgefordert werden, aktualisieren Sie den Cache.

   Nachdem der Cache aktualisiert wurde, wird die Geschenkregistrierung im Menü Geschäfte unter Andere Einstellungen angezeigt und ist in Kundenkonten verfügbar.
