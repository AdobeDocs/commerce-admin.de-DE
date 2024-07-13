---
title: Jetzt online
description: Die Option _Now Online_ im Menü [!UICONTROL Customers ]listet alle Kunden und Besucher auf, die derzeit in Ihrem Store online sind.
exl-id: 69af669d-f9aa-471b-9d62-5657f3fb2103
source-git-commit: c855a691ed33e1e6e74865ebdfb30ddad21ad83e
workflow-type: tm+mt
source-wordcount: '340'
ht-degree: 0%

---

# Jetzt online

Die Option **[!UICONTROL Now Online]** im Menü [!DNL Customers] listet alle Kunden und Besucher auf, die derzeit in Ihrem Geschäft online sind. Das Zeitintervall, in dem Kunden als aktuell online angezeigt werden, wird in der Konfiguration festgelegt und bestimmt, wie lange die [!DNL Customer's] -Aktivität vom Administrator sichtbar ist. Standardmäßig beträgt das Intervall 15 Minuten. Die Sitzung endet, wenn die Tastatur während dieser Zeit nicht verwendet wird und Kunden sich erneut bei ihren Konten anmelden müssen, um den Einkauf fortzusetzen. Es ist wichtig zu beachten, dass der Inhalt des Warenkorbs für den späteren Zugriff gespeichert wird.

![Online-Kunden](assets/customers-now-online.png){width="700" zoomable="yes"}

Der Online-Status von Kunden wird nur bei der Anmeldung, Registrierung oder einem anderen Ereignis aktualisiert, bei dem der Status geändert wird. Sie umfasst Warenkorbereignisse, z. B. das Hinzufügen, Entfernen und Ändern von Produkten.

>[!NOTE]
>
>Seitenbesuche allein aktualisieren nicht den Online-Status des Kunden. Um solche Informationen zu erfassen, wird empfohlen, [Google Analytics ](../merchandising-promotions/google-analytics.md) (allein oder mit [Google Tag Manager](../merchandising-promotions/google-tag-manager.md)) einzurichten oder andere Analysesoftware mit Adobe Commerce zu verwenden.

## Alle derzeit online verfügbaren Kunden anzeigen

Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Customers]** > **[!UICONTROL Online Now]**.

>[!TIP]
>
>Informationen dazu, wie Sie einem Online-Kunden helfen können, einen Kauf abzuschließen, finden Sie unter [Shopping-Hilfe](../stores-purchase/introduction.md#shopping-assistance).

## Zeitintervall konfigurieren

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich den Wert **[!UICONTROL Customers]** und wählen Sie **[!UICONTROL Customer Configuration]** aus.

1. Erweitern Sie den Abschnitt **[!UICONTROL Online Customers Options]** und führen Sie die folgenden Schritte aus:

   ![Online-Kundenoptionen](../configuration-reference/customers/assets/customer-configuration-online-customers-options.png){width="600" zoomable="yes"}

   - Geben Sie für &quot;**[!UICONTROL Online Minutes Interval]**&quot;die Anzahl der Minuten ein, die für die Kundensitzung angezeigt werden sollen. Lassen Sie das Feld leer, um das Standardintervall von 15 Minuten zu akzeptieren.

   - Geben Sie für &quot;**[!UICONTROL Customer Data Lifetime]**&quot;die Anzahl der Minuten ein, bevor nicht gespeicherte Daten ablaufen, die vom Kunden eingegeben wurden.

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save Config]**.

## Spaltenbeschreibungen

| Spalte | Beschreibung |
| --- | --- |
| **[!UICONTROL ID]** | Die Kunden-ID eines registrierten Kunden. |
| **[!UICONTROL First Name]** | Der Vorname eines registrierten Kunden. |
| **[!UICONTROL Last Name]** | Der Nachname eines registrierten Kunden. |
| **[!UICONTROL Email]** | Die E-Mail-Adresse eines registrierten Kunden. |
| **[!UICONTROL Last Activity]** | Datum und Uhrzeit der letzten Aktivität des Kunden in Ihrem Store. |
| **[!UICONTROL Type]** | Optionen: `Customer` / `Visitor` |
| **[!UICONTROL Last URL]** | Die letzte URL, die der Kunde besucht hat. |
| **[!UICONTROL Company]** | Der Name des Unternehmens, zu dem der Benutzer gehört. |

{style="table-layout:auto"}
