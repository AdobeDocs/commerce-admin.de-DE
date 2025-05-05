---
title: Warnhinweise für Produkte
description: Erfahren Sie mehr über Produktwarnungen und deren Verwendung, um Kunden über den Lagerstatus und Preisänderungen für Produkte zu informieren.
exl-id: c9f736c5-7bba-4e3e-804d-5b0fe52c8f9b
feature: Inventory, Configuration
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '648'
ht-degree: 0%

---

# Warnhinweise für Produkte

Kunden können zwei Arten von Warnhinweisen per E-Mail abonnieren: Warnhinweise zu Preisänderungen und Warnhinweise auf Lager. Für jeden Warnhinweistyp können Sie festlegen, ob sich Kunden anmelden können, die verwendete E-Mail-Vorlage auswählen und den Absender der E-Mail identifizieren.

![Produktbenachrichtigung abonnieren](assets/product-alert-setting.png){width="600" zoomable="yes"}

## Warnhinweise bei Preisänderungen

Wenn Warnhinweise zu Preisänderungen aktiviert sind, wird auf jeder Produktseite ein _Bei Preisverfall benachrichtigen_ angezeigt. Kunden können auf den Link klicken, um Warnhinweise zum Produkt zu abonnieren. Die Gäste werden aufgefordert, ein Konto bei Ihrem Geschäft zu eröffnen. Wenn sich der Preis ändert oder das Produkt in eine Sonderaktion wechselt, erhält jeder, der sich für den Warnhinweis angemeldet hat, eine E-Mail-Benachrichtigung.

## Warnhinweise auf Lager

Der Warnhinweis auf Lager erstellt für jedes Produkt _das nicht vorrätig ist, einen Link namens_ Benachrichtigen Sie mich, wenn dieses Produkt auf Lager ist“. Kunden können auf den Link klicken, um den Warnhinweis zu abonnieren. Wenn das Produkt wieder auf Lager ist, erhalten Kunden eine E-Mail-Benachrichtigung, dass das Produkt verfügbar ist. Produkte mit Warnhinweisen verfügen über eine _Produktwarnungen_ im Bedienfeld Produktinformationen , in der die Kunden aufgeführt sind, die einen Warnhinweis abonniert haben.

![Liste der Produkt- und Preiswarnungs-Abonnements](assets/inventory-product-alerts.png){width="600" zoomable="yes"}

## Einrichten von Warnhinweisen für Produkte

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Catalog]** und wählen Sie darunter **[!UICONTROL Catalog]**.

1. Klicken Sie, um den Abschnitt _[!UICONTROL Product Alerts]_&#x200B;zu erweitern, und gehen Sie folgendermaßen vor:

   ![Produktbenachrichtigungen](assets/config-catalog-product-alerts.png){width="600" zoomable="yes"}

   - Um Ihren Kunden Warnhinweise zu Preisänderungen anzubieten, setzen Sie **[!UICONTROL Allow Alert When Product Price Changes]** auf `Yes`.

   - Legen Sie **[!UICONTROL Price Alert Email Template]** auf die Vorlage fest, die Sie für die Preiswarnbenachrichtigungen verwenden möchten.

   - Um Warnhinweise anzubieten, wenn nicht vorrätige Produkte erneut verfügbar werden, setzen Sie **[!UICONTROL Allow Alert When Product Comes Back in Stock]** auf `Yes`.

     >[!NOTE]
     >
     >Die _Benachrichtigen, wenn dieses Produkt auf Lager ist_ wird nur angezeigt, wenn **[!UICONTROL Display Out of Stock Products]** auf `Yes` eingestellt ist (in der Konfiguration unter [!UICONTROL Catalog] > [!UICONTROL Inventory]).

   - Legen Sie **[!UICONTROL Stock Alert Email Template]** auf die Vorlage fest, die Sie für Warnhinweise zu Produktbeständen verwenden möchten.

   - Legen Sie **[!UICONTROL Alert Email Sender]** auf den [Store-](../getting-started/store-details.md#store-email-addresses){target="_blank"}&quot; fest, der als Absender des E-Mail-Warnhinweises angezeigt werden soll. Weitere Informationen zum [Speichern von E-Mail](../configuration-reference/general/store-email-addresses.md){target="_blank"}Adressen finden Sie im Benutzerhandbuch zu Core.

1. Klicken Sie abschließend auf **[!UICONTROL Save Config]**.

## Konfigurieren von E-Mail-Vorlagen für Produktwarnungen

Konfigurieren, fügen oder ändern Sie als Nächstes die E-Mail-Vorlage für Ihren Preishinweis hinzu. Sie können die Konfiguration Ihrer Preiswarnhinweise bearbeiten, nachdem Sie zusätzliche Vorlagen erstellt haben.

Ausführlichere Informationen zur Verwendung von E-Mail-Nachrichten finden Sie unter [Nachrichtenvorlagen](../systems/email-template-custom.md#message-templates) im _Admin Systems Guide_.

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Marketing]** > _[!UICONTROL Communications]_>**[!UICONTROL Email Templates]**.

1. Klicken Sie auf **[!UICONTROL Add New Template]**.

1. Wählen _unter „Standardvorlage laden_ die **[!UICONTROL Template]** aus, die Sie anpassen möchten.

   Sie können die in Ihrem Design enthaltene Warnhinweisvorlage auswählen. Sie können auch die `Price Alert` oder `Stock Alert` Vorlagen unter _[!UICONTROL Magento_PriceAlert]_&#x200B;auswählen.

1. Klicken Sie auf **[!UICONTROL Load Template]**.

1. Geben Sie einen **[!UICONTROL Template Name]** ein.

   Sie können diesen Namen in der Konfiguration &quot;_&quot;_.

1. Lesen Sie den vorhandenen Inhalt durch und nehmen Sie die erforderlichen Änderungen für Folgendes vor:

   | Feld | Beschreibung |
   | ----- | ----- |
   | [!UICONTROL Template Subject] | Dieser Text wird in der Betreffzeile einer E-Mail angezeigt. |
   | [!UICONTROL Template Content] | Dieser Text wird im vollständigen Inhalt der gesendeten E-Mail angezeigt. |

1. Um generierte Informationen aus [!DNL Commerce] hinzuzufügen, verwenden Sie die Option **[!UICONTROL Insert Variable]** , um eine Liste der verfügbaren Variablen zu verwenden.

1. Klicken Sie auf **[!UICONTROL Save Template]**.

## Einstellungen für die Ausführung von Warnhinweisen für Produkte

Mit diesen Einstellungen können Sie festlegen, wie oft [!DNL Commerce] auf Änderungen prüft, für die Warnhinweise gesendet werden müssen. Sie können auch den Empfänger, den Absender und die Vorlage für E-Mails auswählen, die gesendet werden, wenn der Versand von Warnhinweisen fehlschlägt.

![Einstellungen für die Ausführung von Warnhinweisen](assets/config-catalog-product-alerts-run-settings.png){width="600" zoomable="yes"}

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Catalog]** und wählen Sie darunter **[!UICONTROL Catalog]**.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Product Alerts Run Settings]** .

1. Um zu bestimmen, wie oft Warnhinweise für Produkte gesendet werden, legen Sie **[!UICONTROL Frequency]** auf einen der folgenden Werte fest:

   - `Daily`
   - `Weekly`
   - `Monthly`

1. Um zu bestimmen, zu welcher Tageszeit Warnhinweise gesendet werden, legen Sie **[!UICONTROL Start Time]** auf die Stunde, Minute und Sekunde fest.

   >[!NOTE]
   >
   >Warnhinweise für Produkte werden vom Verbraucher „product_alert“ gesendet.

1. Geben Sie **[!UICONTROL Error Email Recipient]** die E-Mail-Adresse der zu kontaktierenden Person ein, wenn ein Fehler auftritt.

1. Wählen Sie für die **[!UICONTROL Error Email Sender]** die Store-Identität aus, die als Absender der Fehlerbenachrichtigung angezeigt wird.

1. Legen Sie **[!UICONTROL Error Email Template]** auf die Transaktions-E-Mail-Vorlage fest, die für die Fehlerbenachrichtigung verwendet werden soll.

1. Klicken Sie abschließend auf **[!UICONTROL Save Config]**.
