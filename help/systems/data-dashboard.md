---
title: Dashboard für das Daten-Management
description: Erfahren Sie, wie Sie auf Einblicke zu Datenströmen für [!DNL Catalog Service],  [!DNL Live Search] und  [!DNL Product Recommendation] zugreifen können.
feature: Products, Customers, Data Import/Export
exl-id: 63c261c1-1a52-46f7-93f8-81055edf1f7b
source-git-commit: 5da244a548b15863fe31b5df8b509f8e63df27c2
workflow-type: tm+mt
source-wordcount: '682'
ht-degree: 0%

---

# Dashboard für das Daten-Management

Das Daten-Management-Dashboard bietet einen Überblick über den Synchronisierungsstatus für Produktdaten, die aus der Commerce-Datenbank an Commerce SaaS-Services übertragen werden. Benutzer können den Status der Produktsynchronisierung bequem überwachen und die Datensynchronisierung über ein einheitliches Dashboard starten. Diese Funktion bietet wertvolle Einblicke in die Verfügbarkeit von Produktdaten für Ihre Storefront, sodass sie Ihren Kundinnen und Kunden sofort angezeigt werden können.

## Zielgruppe

Das Daten-Management-Dashboard steht allen Commerce-Händlern, die [[!DNL Product Recommendations v6.0.0]](https://experienceleague.adobe.com/en/docs/commerce/product-recommendations/guide-overview), [[!DNL Live Search v4.1.0]](https://experienceleague.adobe.com/en/docs/commerce/live-search/guide-overview) oder [[!DNL Catalog Service v1.17]](https://experienceleague.adobe.com/en/docs/commerce/catalog-service/guide-overview) mit einer aktiven Lizenz verwenden, ohne zusätzliche Kosten zur Verfügung.

Das Daten-Management-Dashboard befindet sich unter *System* > Datenübertragung > *Daten-Management-Dashboard*.

![Daten-Management-Dashboard](assets/data-management-dashboard.png)

Das Dashboard enthält die folgenden Felder:

| Feld | Beschreibung |
|--- |--- |
| Umfang | Spezifische Website für die synchronisierten Daten. |
| [!DNL Product Recommendations] | Zeigt den Synchronisierungsstatus, die Anzahl der synchronisierten Produkte und eine Tabelle der [anzeigbaren](https://experienceleague.adobe.com/en/docs/commerce-admin/config/catalog/inventory#stock-options) synchronisierten Produkte für [!DNL Product Recommendations] an. |
| [!DNL Live Search] | Zeigt den Synchronisierungsstatus, die Anzahl der synchronisierten Produkte und eine Tabelle der [anzeigbaren](https://experienceleague.adobe.com/en/docs/commerce-admin/config/catalog/inventory#stock-options) synchronisierten Produkte für [!DNL Live Search] an. |
| [!DNL Catalog Service] | Zeigt den Synchronisierungsstatus, die Anzahl der synchronisierten Produkte und eine Tabelle der synchronisierten Produkte für [!DNL Catalog Service] an. |
| Einstellungen | Öffnet ein Dialogfeld, in dem Sie [die Katalogdaten manuell neu synchronisieren](#resync-catalog-data). |
| Synchronisierungsstatus | Zeigt die Anzahl der Produkte an, die innerhalb der letzten drei Stunden von der Commerce-Datenbank zu einem der SaaS-Services übertragen wurden. Wenn Sie Ihren Katalog gelegentlich aktualisieren, ist dieser Wert häufig null. Wenn eine Synchronisierung ausgeführt wird, klicken Sie auf **[!UICONTROL Refresh]** , um eine aktualisierte Anzahl abzurufen. |
| Anzahl der Produkte | Gibt die Gesamtzahl der Katalogprodukte an, die für den Service verfügbar sind. Die [!DNL Product Recommendations]- und [!DNL Live Search]-Dashboards zeigen die Gesamtzahl der _anzeigbaren_ an. [!DNL Catalog Service] filtert Produkte nicht nach anzeigbaren Inhalten. Wenn Sie also sowohl [!DNL Catalog Service] als auch [!DNL Live Search] oder [!DNL Product Recommendations] installiert haben, können die beiden Dashboards zwei verschiedene Werte für die Produktanzahl anzeigen. |
| Synchronisierte Produkte | Enthält Details zu den Produkten im Commerce-Kernindex. Standardmäßig wird diese Tabelle nach „Zuletzt aktualisiert“ sortiert. Um ein bestimmtes Produkt zu finden, verwenden Sie das Feld **[!UICONTROL Search by SKU]** . Um zu steuern, welche Spalten angezeigt werden, klicken Sie auf **[!UICONTROL Customize Table]** rechts neben der Tabelle. |

## Verwenden des Daten-Management-Dashboards

Wenn Sie Produkte in der Commerce-Datenbank aktualisieren, werden Produktdaten entsprechend Ihrer Systemkonfiguration an SaaS-Services übertragen. Wenn der Synchronisierungsvorgang gestartet wird, gibt **Produktanzahl** die Anzahl der an SaaS-Services gesendeten Produkte an.

>[!IMPORTANT]
>
>Die Zeit, die zum Abschluss der Synchronisierung benötigt wird, hängt von Ihrer Kataloggröße und dem Volumen der aktualisierten Daten ab.

Wenn die Anzahl der verarbeiteten Produkte mit der Anzahl der aktualisierten Produkte übereinstimmt, bedeutet dies, dass die Synchronisierung abgeschlossen ist.

>[!NOTE]
>
>Adobe bietet außerdem eine Befehlszeilenschnittstelle und Systemprotokolle, die Entwickler und Systemintegratoren verwenden können, um Synchronisierungsvorgänge zu verwalten und zu verfolgen und Fehler für Commerce SaaS-Services zu beheben. Weitere Informationen finden Sie im [SaaS-Datenexporthandbuch](https://experienceleague.adobe.com/en/docs/commerce/saas-data-export/overview).

### Liste der synchronisierten Produkte

Um die Details eines synchronisierten Produkts anzuzeigen, klicken Sie in der Tabelle auf das Produkt.

![Produktdetails synchronisieren](assets/sync-product-detail.png)

### Katalogdaten neu synchronisieren

Um sicherzustellen, dass Ihre Commerce SaaS-Services immer mit den neuesten Produktinformationen aktualisiert werden, sollten Sie [einen Zeitplan) ](https://experienceleague.adobe.com/en/docs/commerce-operations/configuration-guide/cli/manage-indexers#reindex) Synchronisieren von Katalogdaten implementieren.

Sie können zwar [manuell initiieren](#manually-resync-catalog) eine Neusynchronisierung von Katalogdaten aus der Commerce-Datenbank mit SaaS-Services durchführen, dies wird jedoch nicht empfohlen, da dies die Belastung der Hardwareressourcen erhöhen kann. In den folgenden Szenarien kann es jedoch erforderlich sein, den Katalog manuell neu zu synchronisieren:

- Wenn wesentliche Änderungen an Ihrem Produktkatalog vorgenommen werden, z. B. beim Hinzufügen neuer Produkte, Aktualisieren von Produktdetails oder Ändern von Kategorien

- Wenn Sie Diskrepanzen oder Leistungsprobleme bei der Anzeige von Produktdaten auf Ihren Storefronts bemerken

- Nach allen Aktualisierungen oder Änderungen an Integrationen zwischen der Commerce-Datenbank und den SaaS-Services

- Beim Bereitstellen von Anpassungen oder Konfigurationen, die sich auf die Verwaltung von Produktdaten oder Synchronisierungsprozesse auswirken

Durch Befolgung dieser Richtlinien und das proaktive Neusynchronisieren von Katalogdaten nach Bedarf können Sie die Konsistenz, Genauigkeit und Zuverlässigkeit der Daten in Ihrem gesamten Adobe Commerce-Ökosystem gewährleisten.

#### Katalog manuell neu synchronisieren

Wenn Sie Katalogdaten erneut synchronisieren müssen, klicken Sie auf der rechten Seite der Seite auf **[!UICONTROL Settings]** , um ein Dialogfeld anzuzeigen, in dem Sie eine erneute Synchronisierung starten können. Durch das Neusynchronisieren von Katalogdaten wird der Service gezwungen, Daten erneut aus der Commerce-Datenbank auf SaaS-Services abzurufen.

![Produkte manuell synchronisieren](assets/resync-data.png)
