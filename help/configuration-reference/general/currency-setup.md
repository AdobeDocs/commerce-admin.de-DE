---
title: '[!UICONTROL General] &gt; [!UICONTROL Currency Setup]'
description: Überprüfen Sie die Konfigurationseinstellungen auf der [!UICONTROL General] &gt; [!UICONTROL Currency Setup] Seite des Commerce-Administrators.
exl-id: a84be30f-f2eb-4c86-942c-2d49e5cf23af
role: Admin
feature: Currency, Configuration, Data Import/Export
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '356'
ht-degree: 3%

---

# [!UICONTROL General] > [!UICONTROL Currency Setup]

{{config}}

>[!NOTE]
>
>Siehe [Währungskonfiguration](../../stores-purchase/currency-configuration.md) für weitere Informationen zu diesen Konfigurationen.

## [!UICONTROL Currency Options]

![Währungseinstellungen > Währungsoptionen](./assets/currency-setup-currency-options.png)<!-- zoom -->

| Feld | [Anwendungsbereich](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Base Currency] | Webseite | Die Primärwährung, die für alle Online-Zahlungsvorgänge verwendet wird. Bei mehreren Store-Ansichten muss der Umfang des Preises in der Variablen [Katalog](../catalog/catalog.md) Konfiguration. |
| [!UICONTROL Default Display Currency] | Store-Ansicht | Die Primärwährung, die zur Anzeige der Preise verwendet wird. |
| [!UICONTROL Allowed Currencies] | Store-Ansicht | Die Währungen, die von Ihrem Geschäft gegen Bezahlung akzeptiert werden. |

{style="table-layout:auto"}

## [!UICONTROL Fixer.io (legacy)]

>[!IMPORTANT]
>
>Ab Version 2.4.6 wird die [[!DNL Fixer.io]](https://fixer.io/) -Dienst veraltet ist und durch die [[!DNL Fixer API] (APILayer)](https://apilayer.com/marketplace/fixer-api) -Dienst. Es wird dringend empfohlen, ein APILayer-Konto anstelle eines veralteten zu verwenden [!DNL Fixer.io] -Konto.

![Währungseinstellungen > Fixer.io](./assets/currency-setup-fixer.png)<!-- zoom -->

| Feld | [Anwendungsbereich](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL API key] | Global | Der Schlüssel, der für den Zugriff auf den Konvertierungsdienst über [!DNL fixer.io] -Konto. Weitere Informationen finden Sie unter [[!DNL fixer.io]](https://fixer.io/). |
| [!UICONTROL Connection Timeout in Seconds] | Global | Bestimmt die Anzahl der Sekunden Inaktivität, bevor eine Fixer.io-Sitzung mit einem Timeout beendet wird. Standardwert: `100` |

{style="table-layout:auto"}

## [!UICONTROL Fixer Api (APILayer)]

![Währungseinstellungen > Fixer-API (APILayer)](./assets/currency-setup-fixer-api.png)<!-- zoom -->

| Feld | [Anwendungsbereich](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL API key] | Global | Der Schlüssel, der für den Zugriff auf den Konvertierungsdienst über [!DNL APILayer] -Konto. Weitere Informationen finden Sie unter [[!DNL APILayer]](https://apilayer.com/). |
| [!UICONTROL Connection Timeout in Seconds] | Global | Bestimmt die Anzahl der Sekunden Inaktivität vor einer [!DNL APILayer] -Sitzung beendet ist. Der Standardwert ist `100`. |

{style="table-layout:auto"}

## [!UICONTROL Currency Converter API]

![Währungseinstellungen > Währungsumrechner-API](./assets/currency-setup-converter.png)<!-- zoom -->

| Feld | [Anwendungsbereich](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL API key] | Global | Der Schlüssel für den Zugriff auf den Konvertierungsdienst. Weitere Informationen finden Sie unter [[!DNL Currency Convertor] API](https://free.currencyconverterapi.com/). |
| [!UICONTROL Connection Timeout in Seconds] | Global | Bestimmt die Anzahl der Sekunden Inaktivität vor einer [!DNL Currency Converter] -Sitzung beendet ist. Standardwert:`100` |

{style="table-layout:auto"}

## [!UICONTROL Scheduled Import Settings]

![Währungseinstellungen > Geplante Importeinstellungen](./assets/currency-setup-scheduled-import-settings.png)<!-- zoom -->

| Feld | [Anwendungsbereich](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Enabled] | Store-Ansicht | Bestimmt, ob der geplante Import für Währungskurse aktiviert ist. Optionen: `Yes` / `No` |
| [!UICONTROL Service] | Store-Ansicht | Gibt den Dienst an, der die Daten für den geplanten Import bereitstellt. Der Standardwert ist `fixer.io` |
| [!UICONTROL Start Time] | Store-Ansicht | Gibt die Startzeit nach Stunde, Minute und Sekunde basierend auf einer 24-Stunden-Uhr an. |
| [!UICONTROL Frequency] | Store-Ansicht | Bestimmt, wie oft der geplante Import stattfindet. Optionen: `Daily` / `Weekly` / `Monthly` |
| [!UICONTROL Error Email Recipient] | Store-Ansicht | Identifiziert die E-Mail-Adresse jeder Person, die per E-Mail über geplante Importfehler benachrichtigt wird. Trennen Sie bei mehreren Empfängern jeden Eintrag durch ein Komma. |
| [!UICONTROL Error Email Sender] | Webseite | Identifiziert den Store-Kontakt, der als Absender der E-Mail-Benachrichtigung angezeigt wird. Standardabsender: `General Contact` |
| [!UICONTROL Error Email Template] | Webseite | Gibt die Vorlage an, die als Grundlage für die Fehler-E-Mail-Benachrichtigung verwendet wird. Standardvorlage: `Currency Update Warnings` |

{style="table-layout:auto"}
