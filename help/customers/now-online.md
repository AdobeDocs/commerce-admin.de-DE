---
title: Kunden jetzt online
description: Die Option _Now Online_ im Menü [!UICONTROL Customers ]listet alle Kunden und Besucher auf, die derzeit in Ihrem Geschäft online sind.
exl-id: 69af669d-f9aa-471b-9d62-5657f3fb2103
TQID: https://experienceleague.adobe.com/jtyDgy3jFmn0XymAYcpc2AOLLWSTDw-3OGkvG9a1SDc
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: bd989d82-1e15-4534-88db-f1f51dd77ffaid: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: e0eb8757-182f-49f3-94a4-1587d16f5094id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 342
ht-degree: 0%

---

# Kunden jetzt online

Die Option **[!UICONTROL Now Online]** im Menü [!DNL Customers] listet alle Kundinnen und Kunden sowie Besucherinnen und Besucher auf, die derzeit in Ihrem Geschäft online sind. Das Zeitintervall, in dem Kundinnen und Kunden angezeigt werden, während der sie aktuell online sind, wird in der Konfiguration festgelegt und bestimmt, wie lange die [!DNL Customer's] Aktivität von der Administratorin bzw. vom Administrator sichtbar ist. Standardmäßig beträgt das Intervall 15 Minuten. Die Sitzung endet, wenn die Tastatur während dieser Zeit nicht verwendet wird und sich Kunden erneut bei ihren Konten anmelden müssen, um den Einkauf fortzusetzen. Beachten Sie, dass der Inhalt der Warenkörbe für den späteren Zugriff gespeichert wird.

![Online-Kunden](assets/customers-now-online.png){width="700" zoomable="yes"}

Der Online-Status von Kundinnen und Kunden wird nur bei der Kundenanmeldung, Registrierung oder einem anderen Statusänderungsereignis aktualisiert. Dazu gehören Warenkorb-bezogene Ereignisse, z. B. das Hinzufügen, Entfernen und Ändern von Produkten.

>[!NOTE]
>
>Bei Seitenbesuchen allein wird der Online-Status des Kunden nicht aktualisiert. Um solche Informationen zu erfassen, wird empfohlen, [Google Analytics einzurichten](../merchandising-promotions/google-analytics.md) (allein oder mit [Google Tag Manager](../merchandising-promotions/google-tag-manager.md)) oder andere Analysesoftware mit Adobe Commerce zu verwenden.

## Alle derzeit online verfügbaren Kunden anzeigen

Navigieren Sie in der _Admin_-Seitenleiste zu **[!UICONTROL Customers]** > **[!UICONTROL Online Now]**.

>[!TIP]
>
>Informationen zur Unterstützung eines Online-Kunden beim Abschluss eines Kaufs finden Sie unter [Shopping-Hilfe](../stores-purchase/introduction.md#shopping-assistance).

## Konfigurieren des Zeitintervalls

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Customers]** und wählen Sie **[!UICONTROL Customer Configuration]**.

1. Erweitern Sie den Abschnitt **[!UICONTROL Online Customers Options]** und gehen Sie folgendermaßen vor:

   ![Online-Kundenoptionen](../configuration-reference/customers/assets/customer-configuration-online-customers-options.png){width="600" zoomable="yes"}

   - Geben Sie **[!UICONTROL Online Minutes Interval]** die Anzahl der Minuten ein, die die Kundensitzung vom Administrator eingesehen werden soll. Lassen Sie das Feld leer, um das Standardintervall von 15 Minuten zu akzeptieren.

   - Geben Sie **[!UICONTROL Customer Data Lifetime]** die Anzahl der Minuten ein, nach denen vom Kunden eingegebene nicht gespeicherte Daten ablaufen.

1. Klicken Sie abschließend auf **[!UICONTROL Save Config]**.

## Spaltenbeschreibungen

| Spalte | Beschreibung |
| --- | --- |
| **[!UICONTROL ID]** | Die Kunden-ID eines registrierten Kunden. |
| **[!UICONTROL First Name]** | Der Vorname eines registrierten Kunden. |
| **[!UICONTROL Last Name]** | Der Nachname eines registrierten Kunden. |
| **[!UICONTROL Email]** | Die E-Mail-Adresse eines registrierten Kunden. |
| **[!UICONTROL Last Activity]** | Datum und Uhrzeit der letzten Aktivität des Kunden in Ihrem Geschäft. |
| **[!UICONTROL Type]** | Optionen: `Customer` / `Visitor` |
| **[!UICONTROL Last URL]** | Die letzte URL, die der Kunde besucht hat. |
| **[!UICONTROL Company]** | Der Name des Unternehmens, dem der Benutzer angehört. |

{style="table-layout:auto"}
