---
title: Produktwarnungen
description: Erfahren Sie mehr über Produktwarnungen und wie Sie sie verwenden können, um Kunden über Aktienstatus und Preisänderungen bei Produkten zu informieren.
exl-id: c9f736c5-7bba-4e3e-804d-5b0fe52c8f9b
feature: Inventory, Configuration
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '631'
ht-degree: 0%

---

# Produktwarnungen

Kunden können zwei Arten von Warnungen per E-Mail abonnieren: Preisänderungswarnungen und Warnungen auf Lager. Für jeden Warnhinweistyp können Sie bestimmen, ob Kunden sich anmelden können, die verwendete E-Mail-Vorlage auswählen und den Absender der E-Mail identifizieren.

![Für eine Produktwarnung anmelden](assets/product-alert-setting.png){width="600" zoomable="yes"}

## Preisänderungswarnungen

Wenn Preisänderungswarnungen aktiviert sind, wird eine _Benachrichtigen Sie mich, wenn der Preis fällt_ -Link wird auf jeder Produktseite angezeigt. Kunden können auf den Link klicken, um Warnhinweise zum Produkt zu abonnieren. Die Gäste werden aufgefordert, ein Konto bei Ihrem Geschäft zu öffnen. Wenn sich der Preis ändert oder das Produkt Sonderangebote erhält jeder, der sich für den Warnhinweis angemeldet hat, eine E-Mail-Warnung.

## In-Stock-Warnhinweise

Der Warnhinweis auf Lager erstellt einen Link namens _Benachrichtigen Sie mich, wenn dieses Produkt vorrätig ist_ für jedes nicht vorrätige Produkt. Kunden können auf den Link klicken, um den Warnhinweis zu abonnieren. Wenn das Produkt wieder auf Lager ist, erhalten Kunden eine E-Mail-Benachrichtigung, dass das Produkt verfügbar ist. Produkte mit Warnhinweisen verfügen über eine _Produktwarnungen_ im Bereich Produktinformationen , in dem die Kunden aufgelistet werden, die sich für einen Warnhinweis angemeldet haben.

![Liste der Produkt- und Preiswarnanmeldungen](assets/inventory-product-alerts.png){width="600" zoomable="yes"}

## Produktwarnungen einrichten

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Catalog]** und wählen **[!UICONTROL Catalog]** darunter.

1. Klicken Sie auf , um die _[!UICONTROL Product Alerts]_und führen Sie folgende Schritte aus:

   ![Produktwarnungen](assets/config-catalog-product-alerts.png){width="600" zoomable="yes"}

   - Um Ihren Kunden Preisänderungswarnungen anzubieten, legen Sie **[!UICONTROL Allow Alert When Product Price Changes]** nach `Yes`.

   - Satz **[!UICONTROL Price Alert Email Template]** der Vorlage, die Sie für Preiswarnmeldungen verwenden möchten.

   - Um Warnhinweise anzubieten, wenn nicht vorrätige Produkte wieder verfügbar werden, legen Sie **[!UICONTROL Allow Alert When Product Comes Back in Stock]** nach `Yes`.

     >[!NOTE]
     >
     >Die _Benachrichtigen Sie mich, wenn dieses Produkt vorrätig ist_ Meldung wird nur angezeigt, wenn **[!UICONTROL Display Out of Stock Products]** auf `Yes` (in der Konfiguration unter [!UICONTROL Catalog] > [!UICONTROL Inventory]).

   - Satz **[!UICONTROL Stock Alert Email Template]** der Vorlage, die Sie für Produktvorräte verwenden möchten.

   - Satz **[!UICONTROL Alert Email Sender]** der [Store-Kontakt](../getting-started/store-details.md#store-email-addresses){target="_blank"} that you want to appear as the sender of the email alert. Learn more about [store email addresses](../configuration-reference/general/store-email-addresses.md){target="_blank"} im Benutzerhandbuch zu zentralen Themen.

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save Config]**.

## E-Mail-Vorlagen für Produktwarnungen konfigurieren

Konfigurieren, hinzufügen oder ändern Sie anschließend die E-Mail-Vorlage für Ihren Preiswarnhinweis. Sie können Ihre Preiswarnungs-Konfigurationen nach der Erstellung zusätzlicher Vorlagen bearbeiten.

Weitere Informationen zur Verwendung von E-Mail-Nachrichten finden Sie unter [Nachrichtenvorlagen](../systems/email-template-custom.md#message-templates) im _Administratorsystemanleitung_.

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Marketing]** > _[!UICONTROL Communications]_>**[!UICONTROL Email Templates]**.

1. Klicken **[!UICONTROL Add New Template]**.

1. under _Standardvorlage laden_, wählen Sie die **[!UICONTROL Template]** , die Sie anpassen möchten.

   Sie können die in Ihrem Design enthaltene Warnhinweisvorlage auswählen. Sie können auch die `Price Alert` oder `Stock Alert` Vorlagen unter _[!UICONTROL Magento_PriceAlert]_.

1. Klicken **[!UICONTROL Load Template]**.

1. Geben Sie einen **[!UICONTROL Template Name]**.

   Sie können diesen Namen im _Preiswarnungen_ Konfiguration.

1. Lesen Sie den vorhandenen Inhalt durch und nehmen Sie bei Bedarf Änderungen für Folgendes vor:

   | Feld | Beschreibung |
   | ----- | ----- |
   | [!UICONTROL Template Subject] | Dieser Text wird in der Betreffzeile einer E-Mail angezeigt. |
   | [!UICONTROL Template Content] | Dieser Text wird im vollständigen Inhalt der gesendeten E-Mail angezeigt. |

1. So fügen Sie generierte Informationen hinzu aus [!DNL Commerce] -Daten verwenden, verwenden Sie die **[!UICONTROL Insert Variable]** -Option, um eine Liste der verfügbaren Variablen zu verwenden.

1. Klicken **[!UICONTROL Save Template]**.

## Ausführungseinstellungen für Produktwarnungen

Mit diesen Einstellungen können Sie festlegen, wie oft [!DNL Commerce] überprüft, ob Änderungen vorgenommen werden, für die Warnhinweise gesendet werden müssen. Sie können auch Empfänger, Absender und Vorlagen für E-Mails auswählen, die gesendet werden, wenn das Senden von Warnungen fehlschlägt.

![Ausführungseinstellungen für Produktwarnungen](assets/config-catalog-product-alerts-run-settings.png){width="600" zoomable="yes"}

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Catalog]** und wählen **[!UICONTROL Catalog]** darunter.

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL Product Alerts Run Settings]** Abschnitt.

1. Um festzustellen, wie oft Produktanzeigen gesendet werden, legen Sie **[!UICONTROL Frequency]** auf einen der folgenden Werte zu:

   - `Daily`
   - `Weekly`
   - `Monthly`

1. Um die Tageszeit zu bestimmen, zu der Produktwarnungen gesendet werden, legen Sie **[!UICONTROL Start Time]** auf die Stunde, Minute und Sekunde.

   >[!NOTE]
   >
   >Produktwarnungen werden vom Verbraucher &quot;product_alert&quot;gesendet.

1. Für **[!UICONTROL Error Email Recipient]** eingeben, geben Sie die E-Mail der Person an, die kontaktiert werden soll, falls ein Fehler auftritt.

1. Für **[!UICONTROL Error Email Sender]** wählen Sie die Store-Identität aus, die als Absender der Fehlerbenachrichtigung angezeigt wird.

1. Satz **[!UICONTROL Error Email Template]** in die für die Fehlerbenachrichtigung zu verwendende Transaktions-E-Mail-Vorlage.

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save Config]**.
