---
title: '[!DNL New Relic] reporting'
description: Erfahren Sie mehr über die [!DNL New Relic] Berichterstellung, die für Konten für Adobe Commerce in der Cloud-Infrastruktur verfügbar ist, einschließlich der Software für den New Relic APM-Dienst.
exl-id: 65d08bda-da01-4dcf-9d92-189d4d303c76
role: Admin, Leader
feature: System
source-git-commit: 0651a2489a396ab142b60a8678d6c7590fd5f9ee
workflow-type: tm+mt
source-wordcount: '1382'
ht-degree: 0%

---

# [!DNL New Relic] Berichterstellung

[New Relic][1] ist ein Softwareanalysedienst, der Ihnen bei der Analyse und Verbesserung von Anwendungsinteraktionen hilft. Konten für Adobe Commerce in der Cloud-Infrastruktur beinhalten die Software für den Dienst [!DNL New Relic APM] . Weitere Informationen finden Sie unter [New Relic-Dienste][4] im _Commerce on Cloud Infrastructure Guide_.

## Schritt 1: Registrieren Sie sich für ein [!DNL New Relic]-Konto.

1. Gehen Sie zur Website [[!DNL New Relic]][1] und melden Sie sich für ein Konto an.

   Sie können sich auch für ein kostenloses Testkonto anmelden.

1. Folgen Sie den Anweisungen auf der Website. Wenn Sie dazu aufgefordert werden, wählen Sie das Produkt aus, das Sie zuerst installieren möchten.

1. Suchen Sie in Ihrem Konto die folgenden Anmeldeinformationen, die zum Abschließen der Commerce-Konfiguration erforderlich sind:

   | Option | Beschreibung |
   | ------ | ----------- |
   | Konto-ID | Im Dashboard Ihres [!DNL New Relic]-Kontos entspricht die Konto-ID der Nummer in der URL nach: `/accounts` |
   | Bewerbungs-ID | Klicken Sie im Dashboard Ihres [!DNL New Relic]-Kontos auf **[!UICONTROL New Relic APM]**. Wählen Sie im Menü **[!UICONTROL Applications]** aus. Wählen Sie dann Ihre Anwendung aus. Die Anwendungs-ID ist die Nummer im URL nach: `/applications/` |
   | Neu Relic-API-Schlüssel | Klicken Sie im Dashboard Ihres [!DNL New Relic]-Kontos auf **[!UICONTROL Account Settings]**. Wählen Sie im Menü auf der linken Seite unter Integrationen die Option **[!UICONTROL Data Sharing]**. Sie können Ihren API-Schlüssel auf dieser Seite erstellen, neu generieren oder löschen. |
   | Insights-API-Schlüssel | Klicken Sie im Dashboard Ihres [!DNL New Relic]-Kontos auf **[!UICONTROL Insights]**. Wählen Sie im Menü auf der linken Seite unter Administration die Option **[!UICONTROL API Keys]**. Ihre Insights-API-Schlüssel werden auf dieser Seite angezeigt. Klicken Sie bei Bedarf auf das Pluszeichen (**+**) neben &quot;Schlüssel einfügen&quot;, um einen Schlüssel zu generieren. |

   {style="table-layout:auto"}

## Schritt 2: Installieren des [!DNL New Relic] -Agenten auf Ihrem Server

Um mit [!DNL New Relic APM Pro] Daten sammeln und übertragen zu können, muss der PHP Agent auf Ihrem Server installiert sein.

1. Wenn Sie aufgefordert werden, einen Webagenten auszuwählen, klicken Sie auf **PHP**.

1. Um den PHP Agent auf Ihrem Server einzurichten, folgen Sie den Anweisungen.

   Wenn Sie Hilfe benötigen, lesen Sie [New Relic für PHP][3].

1. Stellen Sie sicher, dass Cron auf Ihrem Server ausgeführt wird.

   Weitere Informationen finden Sie unter [Konfigurieren und Ausführen von cron][5] in der Entwicklerdokumentation.

## Schritt 3: Konfigurieren Sie Ihren Store.

>[!NOTE]
>Diese Konfigurationsoptionen gelten nicht für Adobe Commerce on Cloud Infrastructure.
>
>Wenn Sie mit dem Pro-Plan arbeiten, ist New Relic bereits [vorkonfiguriert und standardmäßig aktiviert](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/monitor/new-relic/new-relic-service.html). Wenn Sie den Startplan verwenden, müssen Sie die [New Relic-Konfigurationsschritte](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/monitor/new-relic/account-management.html#configure-new-relic-for-starter-environment) ausführen, die Teil des Einrichtungsprozesses sind.

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Wählen Sie im linken Navigationsbereich, in dem **[!UICONTROL General]** erweitert ist, **[!UICONTROL New Relic Reporting]** und gehen Sie wie folgt vor:

   ![New Relic-Berichtskonfiguration](./assets/new-relic-reporting-general.png){width="600"}

   * Setzen Sie **[!UICONTROL Enable New Relic Integration]** auf `Yes`.

   * Ersetzen Sie in &quot;**[!UICONTROL Insights API URL]**&quot;das Prozentsymbol (`%`) durch Ihre New Relic-Konto-ID.

   * Geben Sie Ihren **[!UICONTROL New Relic Account ID]** ein.

   * Geben Sie Ihren **[!UICONTROL New Relic Application ID]** ein.

   * Geben Sie Ihren **[!UICONTROL New Relic API Key]** ein.

   * Geben Sie **[!UICONTROL Insights API Key]** ein.

1. Geben Sie für **[!UICONTROL New Relic Application Name]** einen Namen ein, um die Konfiguration für die interne Referenz zu identifizieren.

1. (Optional) Wählen Sie für &quot;**[!UICONTROL Send Adminhtml and Frontend as Separate Apps]**&quot;die Option &quot;`Yes`&quot;, um die erfassten Daten für die Storefront und &quot;Admin&quot;als separate Apps an New Relic zu senden.

   Für diese Option muss ein Name für die **[!UICONTROL New Relic Application Name]** eingegeben werden.

   >[!NOTE]
   >
   >Durch Aktivierung dieser Funktion wird die Anzahl der falsch positiven [!DNL New Relic] Warnhinweise reduziert und eine konfigurierte Überwachung und Warnhinweise ausschließlich für die Frontend-Leistung ermöglicht. New Relic empfängt separate App-Datendateien mit Namen des Anwendungsnamens, die an `Adminhtml` und das Frontend angehängt sind. Beispiel: `MyStore_Adminhtml`

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save Config]**.

## Schritt 4: Aktivieren von Cron für die [!DNL New Relic] Berichterstellung

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) im Abschnitt **[!UICONTROL Cron]** .

   ![New Relic Cron-Konfiguration](./assets/new-relic-reporting-cron.png){width="600"}

1. Setzen Sie **[!UICONTROL Enable Cron]** auf `Yes`.

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save Config]**.

## [!DNL New Relic] Abfragen

[!DNL New Relic Insights] -Daten basieren auf Anweisungen, die in [!DNL New Relic Query Language] (NRQL) geschrieben sind, sowie auf benutzerdefinierten Parametern, die Sie möglicherweise einbeziehen. Daten können aus Ad-hoc-Abfragen oder aus in Ihrem Dashboard gespeicherten Abfragen zurückgegeben werden. Weitere Informationen finden Sie in der [NRQL-Referenz][6] in der [!DNL New Relic] -Dokumentation.

### Admin-Ereignisse

#### Aktive Administratoren

Gibt die Anzahl der aktiven Admin-Benutzer zurück.

    SELECT uniqueCount(AdminId)
    FROM Transaction
    WHERE appName=&#39;&lt;Ihr_App_Name>&#39; SEIT 15 Minuten vor 

#### Derzeit aktive Admin-Benutzer

Gibt die Namen der aktiven Admin-Benutzer zurück.

    SELECT uniques(AdminName)
    FROM Transaction
    WHERE appName=&#39;&lt;Ihr_App_Name>&#39; SEIT 15 Minuten vor 

#### Letzte Admin-Aktivität

Gibt die Anzahl der letzten Admin-Aktionen zurück.

    SELECT count(AdminId)
    FROM Transaction
    WHERE appName =&#39;&lt;Ihr_App_Name>&#39; FACET AdminName SEIT 1. Tag vor

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
    AND appName = &#39;&lt;Ihr_App_Name>&#39; TIMESERIES 2 Minuten

#### Aktuelle Kataloganzahl

Gibt die durchschnittliche Anzahl der Anwendungsereignisse im Katalog nach Kategorie im angegebenen Zeitraum zurück.

    SELECT average(CatalogCategoryCount)
    FROM Cron
    WHERE CatalogCategoryCount IS NOT NULL
    AND CatalogCategoryCount > 0
    AND appName = &#39;&lt;your_app_name>&#39; SINCE 2 minutes ago LIMIT 1
&lt;/your_app_name>
#### Aktiv Produkte

Gibt die Anzahl der Anwendungsereignisse nach Produkt im angegebenen Zeitraum zurück.

    SELECT average(CatalogProductActiveCount)
    FROM Cron
    WHERE CatalogProductActiveCount IS NOT NULL
    AND appName = &#39;&lt;Ihr_App_Name>&#39; TIMESERIES 2 Minuten

#### Anzahl aktiver Produkte

Gibt die durchschnittliche Anzahl der aktiven Anwendungsereignisse nach Produkt im angegebenen Zeitraum zurück.

    SELECT average(CatalogProductActiveCount)
    FROM Cron
    WHERE CatalogProductActiveCount IS NOT NULL
    AND CatalogProductActiveCount > 0
    AND appName = &#39;&lt;your_app_name>&#39; SEIT 2 Minuten vor LIMIT 1

#### Konfigurierbare Produkte

Gibt die durchschnittliche Anzahl der Anwendungsereignisse für konfigurierbare Produkte im angegebenen Zeitraum zurück.

    SELECT average(CatalogProductConfigurableCount)
    FROM Cron
    WHERE CatalogProductConfigurableCount IS NOT NULL
    AND appName = &#39;&lt;Ihr_App_Name>&#39; TIMESERIES 2 Minuten

#### Konfigurierbare Produktanzahl

Gibt die durchschnittliche Anzahl der Anwendungsereignisse nach konfigurierbarem Produkt während des angegebenen Zeitraums zurück.

    SELECT average(CatalogProductConfigurableCount)
    FROM Cron
    WHERE CatalogProductConfigurableCount IS NOT NULL
    AND CatalogProductConfigurableCount > 0
    AND appName = &#39;&lt;your_app_name>&#39; SEIT 2 Minuten vor LIMIT 1

#### Produktanzahl (alle)

Gibt die Gesamtanzahl der Anwendungsereignisse für alle Produkte zurück.

    SELECT average(CatalogProductCount)
    FROM Cron
    WHERE CatalogProductCount IS NOT NULL
    AND appName = &#39;&lt;Ihr_App_Name>&#39; TIMESERIES 2 Minuten

#### Aktuelle Produktanzahl (alle)

Gibt die durchschnittliche Anzahl von Anwendungsereignissen für alle Produkte im angegebenen Zeitraum zurück.

    SELECT average(CatalogProductCount)
    FROM Cron
    WHERE CatalogProductCount IST NOT NULL
    AND CatalogProductCount > 0
    AND appName = &#39;&lt;Ihr_App_Name>&#39; SEIT 2 Minuten LIMIT 1

#### Kundenanzahl

Gibt die durchschnittliche Anzahl der Anwendungsereignisse nach Kunde zurück.

    SELECT average(CustomerCount)
    FROM Cron
    WHERE CustomerCount IST NOT NULL
    UND CustomerCount > 0&lt;
    AND appName = &#39;&lt;your_app_name>&#39; TIMESERIES 2 Minuten

#### Aktuelle Kundenanzahl

Gibt die durchschnittliche Kundenanzahl im angegebenen Zeitraum zurück.

    SELECT average(CustomerCount)
    FROM Cron
    WHERE CustomerCount IST NOT NULL
    UND CustomerCount > 0
    AND appName = &#39;&lt;Ihr_App_Name>&#39; SEIT 2 Minuten vor LIMIT 1

#### Modulstatus

Gibt die durchschnittliche Anzahl der aktivierten, deaktivierten oder installierten Anwendungsmodule während des angegebenen Zeitraums zurück.

    SELECT average(ModulesDisabled), average(ModulesEnabled), average
    (ModulesInstalled)
    FROM Cron&lt;
    WHERE appName = &#39;&lt;your_app_name>&#39; TIMESERIES 2 Minuten

#### Aktueller Modulstatus

Gibt die durchschnittliche Häufigkeit zurück, mit der Module im angegebenen Zeitraum aktiviert, deaktiviert oder installiert wurden.

    SELECT average(ModulesDisabled), average(ModulesEnabled), average
    (ModulesInstalled)
    FROM Cron
    WHERE appName = &#39;&lt;Ihr_App_Name>&#39; SEIT 2 Minuten LIMIT 1

#### Website- und Store-Anzahl

Gibt die durchschnittliche Anzahl der Anwendungsereignisse nach Website und Store im angegebenen Zeitraum zurück.

    SELECT average(StoreViewCount), average(WebsiteCount)
    FROM Cron
    WHERE appName = &#39;&amp;lt;your_app_name&amp;gt;&#39; TIMESERIES 2 Minuten

#### Aktuelle Website- und Store-Zählungen

Gibt die durchschnittliche Anzahl der aktuellen Anwendungsereignisse im angegebenen Zeitraum zurück.

    SELECT average(StoreViewCount), average(WebsiteCount)
    FROM Cron
    WHERE appName = &#39;&lt;your_app_name>&#39; SEIT 2 Minuten vor LIMIT 1

#### Cron - alle Daten aus dem Ereignis

Gibt alle Ereignisdaten der Anwendung zurück.

    SELECT *
    FROM Cron
    WHERE appName = &#39;&lt;Ihr_App_Name>&#39;

### Kunden

#### Aktive Kundenanzahl

Gibt die Anzahl der aktiven Kunden im angegebenen Zeitraum zurück.

    SELECT uniqueCount(CustomerId)
    FROM Transaction
    WHERE appName = &#39;&lt;Ihr_App_Name>&#39; SEIT 15 Minuten vor 

#### Aktive Kunden

Gibt die Namen aktiver Kunden im angegebenen Zeitraum zurück.

    SELECT uniques(CustomerName)
    FROM Transaction
    WHERE appName=&#39;&lt;Ihr_App_Name>&#39; SEIT 15 Minuten vor 

#### Top-Kunden

Gibt die wichtigsten Kunden im angegebenen Zeitraum zurück.

    SELECT count(CustomerId)
    FROM Transaction
    WHERE appName = &#39;&lt;Ihr_App_Name>&#39; FACET CustomerName SEIT DEM 1. TAG

#### Letzte Admin-Aktivität

Gibt eine definierte Anzahl von Datensätzen der letzten Aktivität zurück, einschließlich des Kundennamens und der Dauer des Besuchs.

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

Gibt die Gesamtzahl der Zeileneinträge zurück, die im angegebenen Zeitraum bestellt wurden.

    SELECT sum(orderValue)
    FROM Transaktion SINCE 1 day ago

#### Gesamt bestellten Zeileneinträge

Gibt die Gesamtzahl der während der angegebenen Zeitraum bestellten Zeileneinträge zurück.

    SELECT sum(lineItemCount)
    FROM Transaction SEIT DEM 1. TAG ago


[1]: https://newrelic.com/
[3]: https://docs.newrelic.com/docs/agents/php-agent/getting-started/new-relic-php
[4]: https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/monitor/new-relic/new-relic-service.html
[5]: https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/configure-cron-jobs.html
[6]: https://docs.newrelic.com/docs/insights/new-relic-insights/using-new-relic-query-language/nrql-reference
