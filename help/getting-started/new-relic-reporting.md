---
title: '[!DNL New Relic] reporting'
description: Informationen zum [!DNL New Relic] Berichterstellung für Konten für Adobe Commerce in der Cloud-Infrastruktur, die die Software für den New Relic-APM-Dienst enthält.
exl-id: 65d08bda-da01-4dcf-9d92-189d4d303c76
role: Admin, Leader
feature: System
source-git-commit: 0651a2489a396ab142b60a8678d6c7590fd5f9ee
workflow-type: tm+mt
source-wordcount: '1382'
ht-degree: 0%

---

# [!DNL New Relic] Berichterstellung

[New Relic][1] ist ein Software Analytics-Dienst, der Sie bei der Analyse und Verbesserung von Anwendungsinteraktionen unterstützt. Konten für Adobe Commerce in Cloud-Infrastruktur enthalten die Software für die [!DNL New Relic APM] -Dienst. Weitere Informationen finden Sie unter [New Relic-Dienste][4] im _Benutzerhandbuch zu Commerce on Cloud Infrastructure_.

## Schritt 1: Registrieren Sie sich für eine [!DNL New Relic] account

1. Navigieren Sie zu [[!DNL New Relic]][1] und melden Sie sich für ein Konto an.

   Sie können sich auch für ein kostenloses Testkonto anmelden.

1. Folgen Sie den Anweisungen auf der Website. Wenn Sie dazu aufgefordert werden, wählen Sie das Produkt aus, das Sie zuerst installieren möchten.

1. Suchen Sie in Ihrem Konto die folgenden Anmeldeinformationen, die zum Abschließen der Commerce-Konfiguration erforderlich sind:

   | Option | Beschreibung |
   | ------ | ----------- |
   | Konto-ID | Von Ihrem [!DNL New Relic] -Konto-Dashboard ist die Konto-ID die Nummer in der URL nach: `/accounts` |
   | Bewerbungs-ID | Von Ihrem [!DNL New Relic] Konto-Dashboard, klicken Sie auf **[!UICONTROL New Relic APM]**. Wählen Sie im Menü **[!UICONTROL Applications]**. Wählen Sie dann Ihre Anwendung aus. Die Anwendungs-ID ist die Nummer im URL nach: `/applications/` |
   | Neu Relic-API-Schlüssel | Von Ihrem [!DNL New Relic] Konto-Dashboard, klicken Sie auf **[!UICONTROL Account Settings]**. Wählen Sie im Menü links unter Integrationen die Option **[!UICONTROL Data Sharing]**. Sie können Ihren API-Schlüssel auf dieser Seite erstellen, neu generieren oder löschen. |
   | Insights-API-Schlüssel | Von Ihrem [!DNL New Relic] Konto-Dashboard, klicken Sie auf **[!UICONTROL Insights]**. Wählen Sie im Menü links unter Administration die Option **[!UICONTROL API Keys]**. Ihre Insights-API-Schlüssel werden auf dieser Seite angezeigt. Klicken Sie bei Bedarf auf das Pluszeichen (**+**) neben Schlüssel einfügen , um einen Schlüssel zu generieren. |

   {style="table-layout:auto"}

## Schritt 2: Installieren Sie die [!DNL New Relic] Agent auf dem Server

Verwendung [!DNL New Relic APM Pro] um Daten zu sammeln und zu übertragen, muss der PHP Agent auf Ihrem Server installiert sein.

1. Wenn Sie zur Auswahl eines Webagenten aufgefordert werden, klicken Sie auf **PHP**.

1. Um den PHP Agent auf Ihrem Server einzurichten, folgen Sie den Anweisungen.

   Wenn Sie Hilfe benötigen, lesen Sie [New Relic für PHP][3].

1. Stellen Sie sicher, dass Cron auf Ihrem Server ausgeführt wird.

   Weitere Informationen finden Sie unter [Cron konfigurieren und ausführen][5] in der Entwicklerdokumentation.

## Schritt 3: Konfigurieren Sie Ihren Store.

>[!NOTE]
>Diese Konfigurationsoptionen gelten nicht für Adobe Commerce on Cloud Infrastructure.
>
>Wenn Sie an einem Pro-Abo teilnehmen, ist New Relic bereits verfügbar [standardmäßig vorkonfiguriert und aktiviert](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/monitor/new-relic/new-relic-service.html). Wenn Sie mit dem Startplan arbeiten, müssen Sie die [New Relic-Konfigurationsschritte](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/monitor/new-relic/account-management.html#configure-new-relic-for-starter-environment) die Teil des Einrichtungsprozesses sind.

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. In der linken Navigationsleiste, in der **[!UICONTROL General]** erweitert ist, wählen Sie **[!UICONTROL New Relic Reporting]** und gehen Sie wie folgt vor:

   ![New Relic-Berichtskonfiguration](./assets/new-relic-reporting-general.png){width="600"}

   * Satz **[!UICONTROL Enable New Relic Integration]** nach `Yes`.

   * Im **[!UICONTROL Insights API URL]**, ersetzen Sie den Prozentsatz (`%`) mit Ihrer New Relic-Konto-ID.

   * Geben Sie Ihre **[!UICONTROL New Relic Account ID]**.

   * Geben Sie Ihre **[!UICONTROL New Relic Application ID]**.

   * Geben Sie Ihre **[!UICONTROL New Relic API Key]**.

   * Geben Sie **[!UICONTROL Insights API Key]**.

1. Für **[!UICONTROL New Relic Application Name]** Geben Sie einen Namen ein, um die Konfiguration für die interne Referenz zu identifizieren.

1. (Optional) Für **[!UICONTROL Send Adminhtml and Frontend as Separate Apps]** auswählen `Yes` , um die erfassten Daten für die Storefront und Admin als separate Apps an New Relic zu senden.

   Für diese Option muss ein Name eingegeben werden. **[!UICONTROL New Relic Application Name]**.

   >[!NOTE]
   >
   >Durch Aktivierung dieser Funktion wird die Anzahl der falsch positiven [!DNL New Relic] Warnhinweise und eine konfigurierte Überwachung sowie Warnhinweise sind nur für die Frontend-Leistung möglich. New Relic empfängt separate App-Datendateien mit Namen des Anwendungsnamens an `Adminhtml` und Frontend. Beispiel: `MyStore_Adminhtml`

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save Config]**.

## Schritt 4: Aktivieren von Cron für [!DNL New Relic] Berichterstellung

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL Cron]** Abschnitt.

   ![New Relic Cron-Konfiguration](./assets/new-relic-reporting-cron.png){width="600"}

1. Satz **[!UICONTROL Enable Cron]** nach `Yes`.

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save Config]**.

## [!DNL New Relic] Abfragen

[!DNL New Relic Insights] -Daten basieren auf -Anweisungen, die in [!DNL New Relic Query Language] (NRQL) sowie alle benutzerdefinierten Parameter, die Sie einbeziehen können. Daten können aus Ad-hoc-Abfragen oder aus in Ihrem Dashboard gespeicherten Abfragen zurückgegeben werden. Weitere Informationen finden Sie unter [NRQL-Referenz][6] im [!DNL New Relic] Dokumentation.

### Admin-Ereignisse

#### Aktive Administratoren

Gibt die Anzahl der aktiven Admin-Benutzer zurück.

    SELECT uniqueCount(AdminId)
    VON Transaktion
    WHERE appName=&#39;&lt;your_app_name>&quot; SEIT 15 Minuten

#### Derzeit aktive Admin-Benutzer

Gibt die Namen der aktiven Admin-Benutzer zurück.

    SELECT uniques(AdminName)
    VON Transaktion
    WHERE appName=&#39;&lt;your_app_name>&quot; SEIT 15 Minuten

#### Letzte Admin-Aktivität

Gibt die Anzahl der letzten Admin-Aktionen zurück.

    SELECT count(AdminId)
    VON Transaktion
    WOBEI appName =&#39;&lt;your_app_name>&quot;FACET-AdminName SEIT 1 Tag vor

#### Neueste Admin-Aktivität

Gibt detaillierte Informationen zu den letzten Administratoraktionen zurück, einschließlich Benutzername, Dauer und Applikation Name des Administrators.

    SELECT AdminName, duration, name
    FROM Transaction
    WHERE appName=&#39;&#39; AND AdminName &lt;your_app_name>IS NOT NULL
    AND AdminName !&lt;/your_app_name>= &#39;N/A&#39; LIMIT 50

### Cron-Ereignisse

#### Kategorie Anzahl

Gibt die Anzahl der Applikation Ereignisse in Kategorie während der angegebenen Zeitraum zurück.

    SELECT average(CatalogCategoryCount)
    VON Cron
    WOBEI CatalogCategoryCount NICHT NULL IST
    AND appName = &#39;&lt;your_app_name>&quot;TIMESERIES 2 Minuten

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
    VON Cron
    WOBEI CatalogProductActiveCount NICHT NULL IST
    AND appName = &#39;&lt;your_app_name>&quot;TIMESERIES 2 Minuten

#### Anzahl aktiver Produkte

Gibt die durchschnittliche Anzahl der aktiven Anwendungsereignisse nach Produkt im angegebenen Zeitraum zurück.

    SELECT average(CatalogProductActiveCount)
    VON Cron
    WOBEI CatalogProductActiveCount NICHT NULL IST
    AND CatalogProductActiveCount > 0
    AND appName = &#39;&lt;your_app_name>&quot; SEIT 2 Minuten vor LIMIT 1

#### Konfigurierbare Produkte

Gibt die durchschnittliche Anzahl der Anwendungsereignisse für konfigurierbare Produkte im angegebenen Zeitraum zurück.

    SELECT average(CatalogProductConfigurableCount)
    VON Cron
    WOBEI CatalogProductConfigurableCount NICHT NULL IST
    AND appName = &#39;&lt;your_app_name>&quot;TIMESERIES 2 Minuten

#### Konfigurierbare Produktanzahl

Gibt die durchschnittliche Anzahl der Anwendungsereignisse nach konfigurierbarem Produkt während des angegebenen Zeitraums zurück.

    SELECT average(CatalogProductConfigurableCount)
    VON Cron
    WOBEI CatalogProductConfigurableCount NICHT NULL IST
    AND CatalogProductConfigurableCount > 0
    AND appName = &#39;&lt;your_app_name>&quot; SEIT 2 Minuten vor LIMIT 1

#### Produktanzahl (alle)

Gibt die Gesamtanzahl der Anwendungsereignisse für alle Produkte zurück.

    SELECT average(CatalogProductCount)
    VON Cron
    WOBEI CatalogProductCount NICHT NULL IST
    AND appName = &#39;&lt;your_app_name>&quot;TIMESERIES 2 Minuten

#### Aktuelle Produktanzahl (alle)

Gibt die durchschnittliche Anzahl von Anwendungsereignissen für alle Produkte im angegebenen Zeitraum zurück.

    SELECT average(CatalogProductCount)
    VON Cron
    WOBEI CatalogProductCount NICHT NULL IST
    AND CatalogProductCount > 0
    AND appName = &#39;&lt;your_app_name>&quot; SEIT 2 Minuten vor LIMIT 1

#### Kundenanzahl

Gibt die durchschnittliche Anzahl der Anwendungsereignisse nach Kunde zurück.

    SELECT average(CustomerCount)
    VON Cron
    WOBEI CustomerCount NICHT NULL IST
    AND CustomerCount > 0&lt;
    AND appName = &#39;&lt;your_app_name>&quot;TIMESERIES 2 Minuten

#### Aktuelle Kundenanzahl

Gibt die durchschnittliche Kundenanzahl im angegebenen Zeitraum zurück.

    SELECT average(CustomerCount)
    VON Cron
    WOBEI CustomerCount NICHT NULL IST
    UND CustomerCount > 0
    AND appName = &#39;&lt;your_app_name>&quot; SEIT 2 Minuten vor LIMIT 1

#### Modulstatus

Gibt die durchschnittliche Anzahl der aktivierten, deaktivierten oder installierten Anwendungsmodule während des angegebenen Zeitraums zurück.

    SELECT average(ModulesDisabled), average(ModulesEnabled), average
    (ModulesInstalled)
    VON Cron&lt;
    WOBEI appName = &#39;&lt;your_app_name>&quot;TIMESERIES 2 Minuten

#### Aktueller Modulstatus

Gibt die durchschnittliche Häufigkeit zurück, mit der Module im angegebenen Zeitraum aktiviert, deaktiviert oder installiert wurden.

    SELECT average(ModulesDisabled), average(ModulesEnabled), average
    (ModulesInstalled)
    VON Cron
    WOBEI appName = &#39;&lt;your_app_name>&quot; SEIT 2 Minuten vor LIMIT 1

#### Website- und Store-Anzahl

Gibt die durchschnittliche Anzahl der Anwendungsereignisse nach Website und Store im angegebenen Zeitraum zurück.

    SELECT average(StoreViewCount), average(WebsiteCount)
    VON Cron
    WOBEI appName = &#39;&amp;lt;your_app_name&amp;gt;&#39; TIMESERIES 2 Minuten

#### Aktuelle Website- und Store-Zählungen

Gibt die durchschnittliche Anzahl der aktuellen Anwendungsereignisse im angegebenen Zeitraum zurück.

    SELECT average(StoreViewCount), average(WebsiteCount)
    VON Cron
    WOBEI appName = &#39;&lt;your_app_name>&quot; SEIT 2 Minuten vor LIMIT 1

#### Cron - alle Daten aus dem Ereignis

Gibt alle Ereignisdaten der Anwendung zurück.

    SELECT *
    VON Cron
    WOBEI appName = &#39;&lt;your_app_name>&#39;

### Kunden

#### Aktive Kundenanzahl

Gibt die Anzahl der aktiven Kunden im angegebenen Zeitraum zurück.

    SELECT uniqueCount(CustomerId)
    VON Transaktion
    WOBEI appName = &#39;&lt;your_app_name>&quot; SEIT 15 Minuten

#### Aktive Kunden

Gibt die Namen aktiver Kunden im angegebenen Zeitraum zurück.

    SELECT uniques(CustomerName)
    VON Transaktion
    WHERE appName=&#39;&lt;your_app_name>&quot; SEIT 15 Minuten

#### Top-Kunden

Gibt die wichtigsten Kunden im angegebenen Zeitraum zurück.

    SELECT count(CustomerId)
    VON Transaktion
    WOBEI appName = &#39;&lt;your_app_name>&quot;FACET Customer Name SEIT 1 Tag vor

#### Letzte Admin-Aktivität

Gibt eine definierte Anzahl von Datensätzen der letzten Aktivität zurück, einschließlich des Kundennamens und der Dauer des Besuchs.

    SELECT CustomerName, duration, name
    FROM Transaction
    WHERE appName=&#39;&lt;your_app_name>&#39;
    AND CustomerName IS NOT NULL
    AND CustomerName !&lt;/your_app_name>= &#39;N/A&#39; LIMIT 50

### Bestellungen

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
    AB Transaktion SEIT 1 Tag


[1]: https://newrelic.com/
[3]: https://docs.newrelic.com/docs/agents/php-agent/getting-started/new-relic-php
[4]: https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/monitor/new-relic/new-relic-service.html
[5]: https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/configure-cron-jobs.html
[6]: https://docs.newrelic.com/docs/insights/new-relic-insights/using-new-relic-query-language/nrql-reference
