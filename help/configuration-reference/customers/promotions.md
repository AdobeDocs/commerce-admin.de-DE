---
title: '[!UICONTROL Customers] &gt; [!UICONTROL Promotions]'
description: Überprüfen Sie die Konfigurationseinstellungen auf der Seite [!UICONTROL Customers] &gt; [!UICONTROL Promotions] des Commerce-Administrators.
exl-id: 93035d46-2e9e-466d-a5e3-d69ce6b662b8
feature: Configuration, Promotions/Events
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '331'
ht-degree: 0%

---

# [!UICONTROL Customers] > [!UICONTROL Promotions]

{{config}}

## [!UICONTROL Automated Email Reminder Rules]

{{ee-feature}}

![Regeln für die automatische E-Mail-Erinnerung](./assets/promotions-automated-email-reminder-rules.png)<!-- zoom -->

<!-- [Automated Email Reminder Rules](https://docs.magento.com/user-guide/marketing/email-reminder-rules-configure.html) -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Enable Reminder Emails] | Global | Aktiviert automatisierte E-Mail-Erinnerungen. Wenn dies auf &quot;Nein&quot;festgelegt ist, werden die verbleibenden Einstellungen ignoriert. Optionen: `Yes` / `No` |
| [!UICONTROL Frequency] | Global | Gibt die Häufigkeit an, mit der Commerce nach neuen Kunden suchen soll, die sich für die automatisierten E-Mail-Erinnerungen qualifizieren. Optionen: <br/>**`Minute Intervals`**- Sendet die E-Mail entsprechend dem ausgewählten Intervall. (5 Minuten, 10 Minuten, 15 Minuten, 20 Minuten oder 30 Minuten)<br/>**`Hourly`** - Sendet die E-Mail stündlich in der Minute, die auf die angegebene Stunde folgt. Geben Sie einen Wert zwischen 0 und 59 ein. <br/>**`Daily`**- Sendet täglich die E-Mail ab der Startzeit. |
| [!UICONTROL Interval] | Global | Das Intervall sollte gleich oder größer als Ihre cron.php-Startzeit sein. Optionen: `5 minutes` / `10 minutes` / `15 minutes` / `20 minutes` / `30 minutes` |
| [!UICONTROL Start Time] | Global | Legt den Tag, die Minute und die Sekunde fest, an der die E-Mail gesendet wird. Wird im 24-Stunden-Format angegeben, basierend auf der Systemzeit auf Ihrem Server. |
| [!UICONTROL Maximum Emails per One Run] | Global | Beschränkt die Anzahl der E-Mails, die in einem geplanten Block gesendet werden. |
| [!UICONTROL Email Send Failure Threshold] | Global | Die Häufigkeit, mit der die Erinnerung versucht, Benachrichtigungen an eine bestimmte E-Mail-Adresse zu senden, und die fehlschlägt. Wenn der Wert auf 0 gesetzt ist, gibt es keinen Schwellenwert, und Benachrichtigungen werden trotz Fehlern weiterhin gesendet. |
| [!UICONTROL Reminder Email Sender] | Store-Ansicht | Die Store-Identität, die als Absender der E-Mail angezeigt wird. |

{style="table-layout:auto"}

## [!UICONTROL Auto Generated Specific Coupon Codes]

![ Automatisch generierte spezifische Couponcodes](./assets/promotions-auto-generated-specific-coupon-codes.png)<!-- zoom -->

<!-- [Auto Generated Specific Coupon Codes](https://docs.magento.com/user-guide/marketing/price-rules-cart-coupon-code-configure.md  -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Code Length] | Global | Definiert die Länge des Couponcodes, ausgenommen das Präfix, das Suffix und die Trennzeichen. |
| [!UICONTROL Code Format] | Global | Definiert das Format des Gutscheincodes. Zu den Optionen gehören: <br/>**`Alphanumeric`**- Jede Kombination von Buchstaben und Zahlen. 0 - Nur Briefe.<br/>**`Alphabetical`** <br/>**`Numeric`**- Nur Zahlen. |
| [!UICONTROL Code Prefix] | Global | Ein Wert, der am Anfang aller Coupon-Codes angehängt wird. Wenn Sie kein Präfix verwenden möchten, lassen Sie das Feld leer. |
| [!UICONTROL Code Suffix] | Global | Ein Wert, der an das Ende aller Codes angehängt wird. Wenn Sie kein Suffix verwenden möchten, lassen Sie das Feld leer. |
| [!UICONTROL Dash Every X Characters] | Global | Das Intervall zum Einfügen eines Bindestrichs (-) in alle Couponcodes. Wenn Sie keinen Bindestrich verwenden möchten, lassen Sie das Feld leer. <br/>_**Hinweis:**_ Couponcodes, die sich nur durch einen Bindestrich unterscheiden, werden als unterschiedliche Codes betrachtet. |

{style="table-layout:auto"}
