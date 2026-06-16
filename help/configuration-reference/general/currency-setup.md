---
title: '[!UICONTROL General] > [!UICONTROL Currency Setup]'
description: Überprüfen Sie die Konfigurationseinstellungen auf der Seite [!UICONTROL General] > [!UICONTROL Currency Setup] des Commerce Admin.
exl-id: a84be30f-f2eb-4c86-942c-2d49e5cf23af
role: Admin
feature: Currency, Configuration, Data Import/Export
TQID: https://experienceleague.adobe.com/L9VCzj3Kb0IEd-XSk6Q-boF6jgIdURXoULgfhO-Hd5s
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 357
ht-degree: 1%

---

# [!UICONTROL General] > [!UICONTROL Currency Setup]

{{config}}

>[!NOTE]
>
>Weitere Informationen [&#x200B; diesen Konfigurationen finden &#x200B;](../../stores-purchase/currency-configuration.md) unter „Währungskonfiguration“.

## [!UICONTROL Currency Options]

![Währungseinstellungen > Währungsoptionen](./assets/currency-setup-currency-options.png)<!-- zoom -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Base Currency] | Website | Die primäre Währung, die für alle Online-Zahlungsvorgänge verwendet wird. Für mehrere Store-Ansichten muss der Umfang des Preises in der Konfiguration [Katalog](../catalog/catalog.md) festgelegt werden. |
| [!UICONTROL Default Display Currency] | Shop-Ansicht | Die primäre Währung zur Anzeige von Preisen. |
| [!UICONTROL Allowed Currencies] | Shop-Ansicht | Die Währungen, die von Ihrem Geschäft zur Zahlung akzeptiert werden. |

{style="table-layout:auto"}

## [!UICONTROL Fixer.io (legacy)]

>[!IMPORTANT]
>
>Ab Version 2.4.6 wird der [[!DNL Fixer.io]](https://fixer.io/)-Service nicht mehr unterstützt und durch den Service [[!DNL Fixer API] (APILayer)](https://apilayer.com/marketplace/fixer-api) ersetzt. Es wird dringend empfohlen, ein APILayer-Konto anstelle eines veralteten [!DNL Fixer.io]-Kontos zu verwenden.

![Währungseinstellungen > Fixer.io](./assets/currency-setup-fixer.png)<!-- zoom -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL API key] | Global | Der Schlüssel, der für den Zugriff auf den Konvertierungsdienst über Ihr [!DNL fixer.io] verwendet wird. Weitere Informationen finden Sie unter [[!DNL fixer.io]](https://fixer.io/). |
| [!UICONTROL Connection Timeout in Seconds] | Global | Bestimmt die Anzahl der Sekunden, in denen es zu Inaktivität kommt, bevor bei einer Fixer.io-Sitzung eine Zeitüberschreitung auftritt. Standardwert: `100` |

{style="table-layout:auto"}

## [!UICONTROL Fixer Api (APILayer)]

![Währungseinstellungen > Fixer-API (APILayer)](./assets/currency-setup-fixer-api.png)<!-- zoom -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL API key] | Global | Der Schlüssel, der für den Zugriff auf den Konvertierungsdienst über Ihr [!DNL APILayer] verwendet wird. Weitere Informationen finden Sie unter [[!DNL APILayer]](https://apilayer.com/). |
| [!UICONTROL Connection Timeout in Seconds] | Global | Bestimmt die Anzahl der Sekunden, in denen es zu Inaktivität kommt, bevor bei einer [!DNL APILayer] Sitzung eine Zeitüberschreitung auftritt. Der Standardwert ist `100`. |

{style="table-layout:auto"}

## [!UICONTROL Currency Converter API]

![Währungseinstellungen > Währungsumrechner-API](./assets/currency-setup-converter.png)<!-- zoom -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL API key] | Global | Der Schlüssel, der für den Zugriff auf den Konvertierungsdienst verwendet wird. Weitere Informationen finden Sie unter [[!DNL Currency Convertor] API](https://free.currencyconverterapi.com/). |
| [!UICONTROL Connection Timeout in Seconds] | Global | Bestimmt die Anzahl der Sekunden, in denen es zu Inaktivität kommt, bevor bei einer [!DNL Currency Converter] Sitzung eine Zeitüberschreitung auftritt. Standardwert: `100` |

{style="table-layout:auto"}

## [!UICONTROL Scheduled Import Settings]

![Währungseinstellungen > Einstellungen für den geplanten Import](./assets/currency-setup-scheduled-import-settings.png)<!-- zoom -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Enabled] | Shop-Ansicht | Legt fest, ob der geplante Import für Währungskurse aktiviert ist. Optionen: `Yes` / `No` |
| [!UICONTROL Service] | Shop-Ansicht | Gibt den Service an, der die Daten für den geplanten Import bereitstellt. Der Standardwert ist `fixer.io` |
| [!UICONTROL Start Time] | Shop-Ansicht | Gibt die Startzeit nach Stunde, Minute und Sekunde an, basierend auf einer 24-Stunden-Zeit. |
| [!UICONTROL Frequency] | Shop-Ansicht | Bestimmt, wie oft der geplante Import stattfindet. Optionen: `Daily` / `Weekly` / `Monthly` |
| [!UICONTROL Error Email Recipient] | Shop-Ansicht | Identifiziert die E-Mail-Adresse jeder Person, die per E-Mail über geplante Importfehler benachrichtigt wird. Trennen Sie bei mehreren Empfängern jeden Eintrag durch ein Komma. |
| [!UICONTROL Error Email Sender] | Website | Identifiziert den Store-Kontakt, der als Absender der Fehler-E-Mail-Benachrichtigung angezeigt wird. Standardabsender: `General Contact` |
| [!UICONTROL Error Email Template] | Website | Gibt die Vorlage an, die als Grundlage für die Fehler-E-Mail-Benachrichtigung verwendet wird. Standardvorlage: `Currency Update Warnings` |

{style="table-layout:auto"}
