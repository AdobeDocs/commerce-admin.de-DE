---
title: '[!DNL New Relic]'
description: Erfahren Sie mehr über die  [!DNL New Relic] -Berichte, die für Konten für Adobe Commerce in der Cloud-Infrastruktur verfügbar sind und die Software für den New Relic APM-Service enthalten.
exl-id: 65d08bda-da01-4dcf-9d92-189d4d303c76
role: Admin, Leader
feature: System
source-git-commit: 0651a2489a396ab142b60a8678d6c7590fd5f9ee
workflow-type: tm+mt
source-wordcount: '1382'
ht-degree: 0%

---

# [!DNL New Relic]

[New Relic][1] ist ein Software-Analyse-Service, mit dem Sie Anwendungsinteraktionen analysieren und verbessern können. Konten für Adobe Commerce in Cloud-Infrastrukturen enthalten die Software für den [!DNL New Relic APM]-Service. Weitere Informationen finden Sie unter [New Relic-Services][4] im Handbuch zu _Commerce in Cloud-Infrastrukturen_.

## Schritt 1: Für ein [!DNL New Relic] Konto anmelden

1. Rufen Sie die [[!DNL New Relic]][1]-Website auf und melden Sie sich für ein Konto an.

   Sie können sich auch für ein kostenloses Testkonto anmelden.

1. Folgen Sie den Anweisungen auf der Website. Wenn Sie dazu aufgefordert werden, wählen Sie das Produkt aus, das Sie zuerst installieren möchten.

1. Suchen Sie in Ihrem Konto die folgenden Anmeldeinformationen, die zum Abschließen der Commerce-Konfiguration erforderlich sind:

   | Option | Beschreibung |
   | ------ | ----------- |
   | Konto-ID | Im Dashboard Ihres [!DNL New Relic]-Kontos ist die Konto-ID die Zahl in der URL nach: `/accounts` |
   | Anwendungs-ID | Klicken Sie im Dashboard Ihres [!DNL New Relic]-Kontos auf **[!UICONTROL New Relic APM]**. Wählen Sie im Menü **[!UICONTROL Applications]** aus. Wählen Sie dann Ihr Programm aus. Die Anwendungs-ID ist die Nummer im URL nach: `/applications/` |
   | Neu Relic-API-Schlüssel | Klicken Sie im Dashboard Ihres [!DNL New Relic]-Kontos auf **[!UICONTROL Account Settings]**. Wählen Sie im Menü links unter Integrationen **[!UICONTROL Data Sharing]** aus. Sie können Ihren API-Schlüssel auf dieser Seite erstellen, neu generieren oder löschen. |
   | Insights-API-Schlüssel | Klicken Sie im Dashboard Ihres [!DNL New Relic]-Kontos auf **[!UICONTROL Insights]**. Wählen Sie im Menü links unter Administration die Option **[!UICONTROL API Keys]** aus. Ihre Insights-API-Schlüssel werden auf dieser Seite angezeigt. Klicken Sie ggf. auf das Pluszeichen (**+**) neben Schlüssel einfügen , um einen Schlüssel zu generieren. |

   {style="table-layout:auto"}

## Schritt 2: Installieren Sie den [!DNL New Relic] auf Ihrem Server.

Um [!DNL New Relic APM Pro] zum Erfassen und Übertragen von Daten zu verwenden, muss der PHP Agent auf Ihrem Server installiert sein.

1. Wenn Sie aufgefordert werden, einen Web-Agenten auszuwählen, klicken Sie auf **PHP**.

1. Um den PHP-Agenten auf Ihrem Server einzurichten, folgen Sie den Anweisungen.

   Wenn Sie Hilfe benötigen, lesen Sie [New Relic for PHP][3].

1. Stellen Sie sicher, dass cron auf Ihrem Server läuft.

   Weitere Informationen finden Sie unter [Konfigurieren und Ausführen von cron][5] in der Entwicklerdokumentation.

## Schritt 3: Konfigurieren des Stores

>[!NOTE]
>Diese Konfigurationsoptionen gelten nicht für Adobe Commerce in der Cloud-Infrastruktur.
>
>Wenn Sie den Pro-Plan verwenden, ist New Relic bereits [vorkonfiguriert und standardmäßig aktiviert](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/monitor/new-relic/new-relic-service.html?lang=de). Wenn Sie den Starter-Plan verwenden, müssen Sie die [New Relic-Konfigurationsschritte](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/monitor/new-relic/account-management.html?lang=de#configure-new-relic-for-starter-environment) ausführen, die Teil des Einrichtungsprozesses sind.

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Wählen Sie im linken Navigationsbereich, in dem die **[!UICONTROL General]** erweitert ist, **[!UICONTROL New Relic Reporting]** aus und führen Sie folgende Schritte aus:

   ![New Relic-Reporting-Konfiguration](./assets/new-relic-reporting-general.png){width="600"}

   * Legen Sie **[!UICONTROL Enable New Relic Integration]** auf `Yes` fest.

   * Ersetzen Sie in der **[!UICONTROL Insights API URL]** das Prozentsymbol (`%`) durch Ihre New Relic-Konto-ID.

   * Geben Sie Ihre **[!UICONTROL New Relic Account ID]** ein.

   * Geben Sie Ihre **[!UICONTROL New Relic Application ID]** ein.

   * Geben Sie Ihre **[!UICONTROL New Relic API Key]** ein.

   * **[!UICONTROL Insights API Key]** eingeben.

1. Geben Sie **[!UICONTROL New Relic Application Name]** einen Namen ein, um die Konfiguration als interne Referenz zu identifizieren.

1. (Optional) Wählen Sie **[!UICONTROL Send Adminhtml and Frontend as Separate Apps]** die Option `Yes` aus, um die erfassten Daten für die Storefront und Admin als separate Apps an New Relic zu senden.

   Für diese Option ist die Eingabe eines Namens für die **[!UICONTROL New Relic Application Name]** erforderlich.

   >[!NOTE]
   >
   >Durch die Aktivierung dieser Funktion wird die Anzahl falsch positiver [!DNL New Relic]-Warnhinweise reduziert und eine konfigurierte Überwachung sowie Warnhinweise ermöglicht, die sich ausschließlich an die Frontend-Leistung richten. New Relic empfängt separate App-Datendateien, an die die Namen der Programme `Adminhtml` und Frontend angehängt werden. Beispiel: `MyStore_Adminhtml`

1. Klicken Sie abschließend auf **[!UICONTROL Save Config]**.

## Schritt 4: Aktivieren von Cron für [!DNL New Relic] Reporting

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Cron]** .

   ![New Relic Cron-Konfiguration](./assets/new-relic-reporting-cron.png){width="600"}

1. Legen Sie **[!UICONTROL Enable Cron]** auf `Yes` fest.

1. Klicken Sie abschließend auf **[!UICONTROL Save Config]**.

## [!DNL New Relic] Abfragen

[!DNL New Relic Insights] Daten basieren auf Anweisungen, die in [!DNL New Relic Query Language] (NRQL) geschrieben wurden, sowie auf benutzerdefinierten Parametern, die Sie möglicherweise einbeziehen. Daten können aus Ad-hoc-Abfragen oder aus Abfragen zurückgegeben werden, die in Ihrem Dashboard gespeichert werden. Weitere Informationen finden Sie in der [NRQL-Referenz][6] in der [!DNL New Relic].

### Admin-Ereignisse

#### Aktive Admin-Benutzer

Gibt die Anzahl der aktiven Admin-Benutzer zurück.

    SELECT uniqueCount(AdminId)
    FROM Transaction
    WHERE appName=&#39;&lt;your_app_name>&#39; SINCE 15 minutes ago

#### Derzeit aktive Admin-Benutzer

Gibt die Namen der aktiven Admin-Benutzenden aus.

    SELECT uniques(AdminName)
    FROM Transaction
    WHERE appName=&#39;&lt;your_app_name>&#39; SINCE 15 minutes ago

#### Letzte Admin-Aktivität

Gibt die Anzahl der letzten Admin-Aktionen zurück.

    SELECT count(AdminId)
    FROM Transaction
    WHERE appName =&#39;&lt;your_app_name>&#39; FACET adminName SINCE 1 day ago

#### Neueste Admin-Aktivität

Gibt detaillierte Informationen zu den letzten Administratoraktionen zurück, einschließlich Benutzername, Dauer und Applikation Name des Administrators.

    SELECT AdminName, duration, name
    FROM Transaction
    WHERE appName=&#39;&lt;your_app_name>&#39; AND AdminName IS NOT NULL
    AND AdminName !&lt;/your_app_name>= &#39;N/A&#39; LIMIT 50

### Cron-Ereignisse

#### Kategorie Anzahl

Gibt die Anzahl der Applikation Ereignisse in Kategorie während der angegebenen Zeitraum zurück.

    SELECT average(CatalogCategoryCount)
    FROM Cron
    WHERE CatalogCategoryCount IS NOT NULL
    AND appName = &#39;&lt;your_app_name>&#39; TIMESERIES 2 minutes

#### Aktuelle Kataloganzahl

Gibt die durchschnittliche Anzahl der Anwendungsereignisse im Katalog nach Kategorie während des angegebenen Zeitraums zurück.

    SELECT average(CatalogCategoryCount)
    FROM Cron
    WHERE CatalogCategoryCount IS NOT NULL
    AND CatalogCategoryCount > 0
    AND appName = &#39;&lt;your_app_name>&#39; SINCE 2 minutes ago LIMIT 1
&lt;/your_app_name>

#### Aktiv Produkte

Gibt die Anzahl der Anwendungsereignisse pro Produkt während des angegebenen Zeitraums zurück.

    SELECT average(CatalogProductActiveCount)
    FROM Cron
    WHERE CatalogProductActiveCount IS NOT NULL
    AND appName = &#39;&lt;your_app_name>&#39; TIMESERIES 2 Minuten

#### Anzahl aktiver Produkte

Gibt die durchschnittliche Anzahl aktiver Anwendungsereignisse pro Produkt während des angegebenen Zeitraums zurück.

    SELECT average(CatalogProductActiveCount)
    FROM Cron
    WHERE CatalogProductActiveCount IS NOT NULL
    AND CatalogProductActiveCount > 0
    AND appName = &#39;&lt;your_app_name>&#39; SINCE 2 minutes ago LIMIT 1

#### Konfigurierbare Produkte

Gibt die durchschnittliche Anzahl von Anwendungsereignissen für konfigurierbare Produkte während des angegebenen Zeitraums zurück.

    SELECT average(CatalogProductConfigurableCount)
    FROM Cron
    WHERE CatalogProductConfigurableCount IS NOT NULL
    AND appName = &#39;&lt;your_app_name>&#39; TIMESERIES 2 Minuten

#### Konfigurierbare Produktzahl

Gibt die durchschnittliche Anzahl der Anwendungsereignisse nach konfigurierbarem Produkt während des angegebenen Zeitraums zurück.

    SELECT average(CatalogProductConfigurableCount)
    FROM Cron
    WHERE CatalogProductConfigurableCount IS NOT NULL
    AND CatalogProductConfigurableCount > 0
    AND appName = &#39;&lt;your_app_name>&#39; SINCE 2 minutes ago LIMIT 1

#### Anzahl der Produkte (alle)

Gibt die Gesamtzahl der Anwendungsereignisse für alle Produkte zurück.

    SELECT average(CatalogProductCount)
    FROM Cron
    WHERE CatalogProductCount IS NOT NULL
    AND appName = &#39;&lt;your_app_name>&#39; TIMESERIES 2 Minuten

#### Aktuelle Produktzahl (alle)

Gibt die durchschnittliche Anzahl der Anwendungsereignisse für alle Produkte während des angegebenen Zeitraums zurück.

    SELECT average(CatalogProductCount)
    FROM Cron
    WHERE CatalogProductCount IS NOT NULL
    AND CatalogProductCount > 0
    AND appName = &#39;&lt;your_app_name>&#39; SINCE 2 minutes ago LIMIT 1

#### Kundenanzahl

Gibt die durchschnittliche Anzahl der Anwendungsereignisse nach Kunde zurück.

    SELECT average(CustomerCount)
    FROM Cron
    WHERE CustomerCount IS NOT NULL
    AND CustomerCount > 0&lt;
    AND appName = &#39;&lt;your_app_name>&#39; TIMESERIES 2 Minuten

#### Aktuelle Kundenanzahl

Gibt die durchschnittliche Anzahl von Kunden während des angegebenen Zeitraums zurück.

    SELECT average(CustomerCount)
    FROM Cron
    WHERE CustomerCount IS NOT NULL
    AND CustomerCount > 0
    AND appName = &#39;&lt;your_app_name>&#39; SINCE 2 minutes ago LIMIT 1

#### Modulstatus

Gibt die durchschnittliche Anzahl der Aktivierungen, Deaktivierungen oder Installationen von Anwendungsmodulen während des angegebenen Zeitraums zurück.

    SELECT average(ModulesDisabled), average(ModulesEnabled), average
    (ModulesInstalled)
    FROM Cron&lt;
    WHERE appName = &#39;&lt;your_app_name>&#39; TIMESERIES 2 Minuten

#### Aktueller Modulstatus

Gibt die durchschnittliche Anzahl der Aktivierungen, Deaktivierungen oder Installationen von Modulen während des angegebenen Zeitraums zurück.

    SELECT average(ModulesDisabled), average(ModulesEnabled), average
    (ModulesInstalled)
    FROM Cron
    WHERE appName = &#39;&lt;your_app_name>&#39; SINCE 2 minutes ago LIMIT 1

#### Anzahl der Websites und Stores

Gibt die durchschnittliche Anzahl von Anwendungsereignissen pro Website und Store während des angegebenen Zeitraums zurück.

    SELECT average(StoreViewCount), average(WebsiteCount)
    FROM Cron
    WHERE appName = &#39;&lt;your_app_name&gt;&#39; TIMESERIES 2 Minuten

#### Aktuelle Website- und Store-Anzahl

Gibt die durchschnittliche Anzahl der aktuellen Anwendungsereignisse während des angegebenen Zeitraums zurück.

    SELECT average(StoreViewCount), average(WebsiteCount)
    FROM Cron
    WHERE appName = &#39;&lt;your_app_name>&#39; SINCE 2 minutes ago LIMIT 1

#### Cron - alle Daten des Ereignisses

Gibt alle Anwendungsereignisdaten zurück.

    SELECT *
    FROM Cron
    WHERE appName = &#39;&lt;your_app_name>&#39;

### Kunden

#### Aktive Kundenanzahl

Gibt die Anzahl der aktiven Kundinnen und Kunden während des angegebenen Zeitraums zurück.

    SELECT uniqueCount(CustomerId)
    FROM Transaction
    WHERE appName = &#39;&lt;your_app_name>&#39; SINCE 15 minutes ago

#### Aktive Kunden

Gibt die Namen der aktiven Kundinnen und Kunden während des angegebenen Zeitraums zurück.

    SELECT uniques(CustomerName)
    FROM Transaction
    WHERE appName=&#39;&lt;your_app_name>&#39; SINCE 15 minutes ago

#### Top-Kunden

Gibt die wichtigsten Kunden im angegebenen Zeitraum zurück.

    SELECT count(CustomerId)
    FROM Transaction
    WHERE appName = &#39;&lt;your_app_name>&#39; FACET CustomerName SINCE 1 day ago

#### Letzte Admin-Aktivität

Gibt eine definierte Anzahl von Datensätzen der letzten Aktivität zurück, die den Kundennamen und die Dauer des Besuchs enthalten.

    SELECT CustomerName, duration, name
    FROM Transaction
    WHERE appName=&#39;&lt;your_app_name>&#39;
    AND CustomerName IS NOT NULL
    AND CustomerName !&lt;/your_app_name>= &#39;N/A&#39; LIMIT 50

### Aufträge

#### Zahl der aufgegebenen Bestellungen

Gibt die Anzahl der Bestellungen zurück, die während der angegebenen Zeitraum erteilt wurden.

    SELECT count(Order)
    FROM Transaktion SINCE 1 day ago

#### Gesamtauftragswert

Gibt die Gesamtzahl der im angegebenen Zeitraum bestellten Zeileneinträge zurück.

    SELECT sum(orderValue)
    FROM Transaktion SINCE 1 day ago

#### Gesamt bestellten Zeileneinträge

Gibt die Gesamtzahl der während der angegebenen Zeitraum bestellten Zeileneinträge zurück.

    SELECT sum(lineItemCount)
    FROM Transaktion SINCE 1 day ago


[1]: https://newrelic.com/
[3]: https://docs.newrelic.com/docs/agents/php-agent/getting-started/new-relic-php
[4]: https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/monitor/new-relic/new-relic-service.html?lang=de
[5]: https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/configure-cron-jobs.html?lang=de
[6]: https://docs.newrelic.com/docs/insights/new-relic-insights/using-new-relic-query-language/nrql-reference
