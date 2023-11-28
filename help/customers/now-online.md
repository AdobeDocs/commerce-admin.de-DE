---
title: Jetzt online
description: Die Option _Now Online_ auf der [!UICONTROL Customers ]im Menü werden alle Kunden und Besucher aufgelistet, die derzeit in Ihrem Geschäft online sind.
exl-id: 69af669d-f9aa-471b-9d62-5657f3fb2103
source-git-commit: c855a691ed33e1e6e74865ebdfb30ddad21ad83e
workflow-type: tm+mt
source-wordcount: '338'
ht-degree: 0%

---

# Jetzt online

Die **[!UICONTROL Now Online]** -Option auf [!DNL Customers] im Menü werden alle Kunden und Besucher aufgelistet, die derzeit in Ihrem Geschäft online sind. Das Zeitintervall, in dem Kunden als aktuell online angezeigt werden, wird in der Konfiguration festgelegt und bestimmt, wie lange die [!DNL Customer's] -Aktivität vom Administrator aus sichtbar. Standardmäßig beträgt das Intervall 15 Minuten. Die Sitzung endet, wenn die Tastatur während dieser Zeit nicht verwendet wird und Kunden sich erneut bei ihren Konten anmelden müssen, um den Einkauf fortzusetzen. Es ist wichtig zu beachten, dass der Inhalt des Warenkorbs für den späteren Zugriff gespeichert wird.

![Online-Kunden](assets/customers-now-online.png){width="700" zoomable="yes"}

Der Online-Status von Kunden wird nur bei der Anmeldung, Registrierung oder einem anderen Ereignis aktualisiert, bei dem der Status geändert wird. Sie umfasst Warenkorbereignisse, z. B. das Hinzufügen, Entfernen und Ändern von Produkten.

>[!NOTE]
>
>Seitenbesuche allein aktualisieren nicht den Online-Status des Kunden. Um solche Informationen zu sammeln, wird empfohlen, [Google Analytics einrichten](../merchandising-promotions/google-analytics.md) (allein oder mit [Google Tag Manager](../merchandising-promotions/google-tag-manager.md)) oder andere Analysesoftware mit Adobe Commerce verwenden.

## Alle derzeit online verfügbaren Kunden anzeigen

Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Customers]** > **[!UICONTROL Online Now]**.

>[!TIP]
>
>Informationen zur Unterstützung eines Online-Kunden beim Abschluss eines Kaufs finden Sie unter [Shopping-Hilfe](../stores-purchase/introduction.md#shopping-assistance).

## Zeitintervall konfigurieren

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Customers]** und wählen **[!UICONTROL Customer Configuration]**.

1. Erweitern Sie die **[!UICONTROL Online Customers Options]** und führen Sie folgende Schritte aus:

   ![Online-Kundenoptionen](../configuration-reference/customers/assets/customer-configuration-online-customers-options.png){width="600" zoomable="yes"}

   - Für **[!UICONTROL Online Minutes Interval]** eingeben, geben Sie die Anzahl der Minuten ein, die die Kundensitzung vom Administrator angezeigt werden soll. Lassen Sie das Feld leer, um das Standardintervall von 15 Minuten zu akzeptieren.

   - Für **[!UICONTROL Customer Data Lifetime]** eingeben, geben Sie die Anzahl der Minuten ein, bevor nicht gespeicherte Daten, die vom Kunden eingegeben wurden, ablaufen.

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save Config]**.

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
