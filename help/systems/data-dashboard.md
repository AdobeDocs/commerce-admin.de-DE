---
title: Data Management Dashboard
description: Erfahren Sie, wie Sie auf Einblicke in Datenströme für [!DNL Catalog Service],  [!DNL Live Search] und  [!DNL Product Recommendation]s zugreifen können.
feature: Products, Customers, Data Import/Export
exl-id: 63c261c1-1a52-46f7-93f8-81055edf1f7b
source-git-commit: 4495a27b57c04c6f9c37b2c5237b5f2233cc8532
workflow-type: tm+mt
source-wordcount: '682'
ht-degree: 0%

---

# Data Management Dashboard

Das Data Management Dashboard bietet einen Überblick über den Synchronisierungsstatus für Produktdaten, die von der Commerce-Datenbank an Commerce SaaS-Dienste übertragen werden. Benutzer können den Status der Produktsynchronisierung bequem überwachen und die Datensynchronisierung über ein einheitliches Dashboard starten. Diese Funktion bietet wertvolle Einblicke in die Verfügbarkeit von Produktdaten für Ihre Storefront und stellt sicher, dass sie Ihren Kunden umgehend angezeigt werden kann.

## Zielgruppe

Das Data Management Dashboard ist für alle Commerce-Händler, die [[!DNL Product Recommendations v6.0.0]](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/product-recommendations/guide-overview), [[!DNL Live Search v4.1.0]](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/live-search/guide-overview) oder [[!DNL Catalog Service v1.17]](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/catalog-service/guide-overview) mit einer aktiven Lizenz verwenden, kostenlos verfügbar.

Das Dashboard &quot;Datenverwaltung&quot;befindet sich unter &quot;*System*&quot;> &quot;Datenübertragung&quot;> &quot;*Dashboard &quot;Datenverwaltung&quot;*&quot;.

![Dashboard &quot;Datenverwaltung&quot;](assets/data-management-dashboard.png)

Das Dashboard enthält die folgenden Felder:

| Feld | Beschreibung |
|--- |--- |
| Anwendungsbereich | Spezifische Website für die synchronisierten Daten. |
| [!DNL Product Recommendations] | Zeigt den Synchronisierungsstatus, die Anzahl der synchronisierten Produkte und eine Tabelle der [anzeigbaren](https://experienceleague.adobe.com/en/docs/commerce-admin/config/catalog/inventory#stock-options) synchronisierten Produkte für [!DNL Product Recommendations] an. |
| [!DNL Live Search] | Zeigt den Synchronisierungsstatus, die Anzahl der synchronisierten Produkte und eine Tabelle der [anzeigbaren](https://experienceleague.adobe.com/en/docs/commerce-admin/config/catalog/inventory#stock-options) synchronisierten Produkte für [!DNL Live Search] an. |
| [!DNL Catalog Service] | Zeigt den Synchronisierungsstatus, die Anzahl der synchronisierten Produkte und eine Tabelle der synchronisierten Produkte für [!DNL Catalog Service] an. |
| Einstellungen | Öffnet ein Dialogfeld, in dem Sie die Katalogdaten [ manuell neu synchronisieren können.](#resync-catalog-data) |
| Synchronisierungsstatus | Zeigt die Anzahl der Produkte an, die innerhalb der letzten drei Stunden von der Commerce-Datenbank an einen der SaaS-Dienste übertragen wurden. Wenn Sie selten einen Katalog aktualisieren, ist dieser Wert häufig null. Wenn eine Synchronisation ausgeführt wird, klicken Sie auf &quot;**[!UICONTROL Refresh]**&quot;, um eine aktualisierte Zählung zu erhalten. |
| Produktanzahl | Gibt die Gesamtanzahl der für den Dienst verfügbaren Katalogprodukte an. Die Dashboards [!DNL Product Recommendations] und [!DNL Live Search] zeigen die Gesamtanzahl der _anzeigbaren_ Produkte an. [!DNL Catalog Service] filtert keine Produkte nach anzuzeigenden Werten. Wenn Sie also sowohl [!DNL Catalog Service] als auch [!DNL Live Search] oder [!DNL Product Recommendations] installiert haben, können die beiden Dashboards zwei unterschiedliche Werte für die Produktanzahl anzeigen. |
| Synchrone Produkte | Enthält Details zu den Produkten im Commerce-Core-Index. Standardmäßig ist diese Tabelle nach &quot;Zuletzt aktualisiert&quot;sortiert. Um ein bestimmtes Produkt zu finden, verwenden Sie das Feld **[!UICONTROL Search by SKU]** . Um zu steuern, welche Spalten angezeigt werden, klicken Sie rechts neben der Tabelle auf **[!UICONTROL Customize Table]** . |

## Verwenden des Daten-Management-Dashboards

Wenn Sie Produkte in der Commerce-Datenbank aktualisieren, werden die Produktdaten gemäß Ihrer Systemkonfiguration an die SaaS-Dienste übertragen. Wenn der Synchronisierungsprozess initiiert wird, gibt **Produktanzahl** die Anzahl der Produkte an, die an SaaS-Dienste gesendet werden.

>[!IMPORTANT]
>
>Die Zeit, die zum Abschluss der Synchronisierung benötigt wird, hängt von der Größe Ihres Katalogs und dem Volumen der aktualisierten Daten ab.

Wenn die Anzahl der verarbeiteten Produkte mit der Anzahl der aktualisierten Produkte übereinstimmt, zeigt dies an, dass die Synchronisierung abgeschlossen ist.

>[!NOTE]
>
>Adobe bietet außerdem eine Befehlszeilenschnittstelle und Systemprotokolle, die Entwickler und Systemintegratoren verwenden können, um Synchronisierungsvorgänge zu verwalten und zu verfolgen und Fehler für Commerce SaaS-Dienste zu beheben. Weitere Informationen finden Sie im [SAAS-Datenexport-Handbuch](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/saas-data-export/overview).

### Liste der synchronisierten Produkte

Um die Details eines synchronisierten Produkts anzuzeigen, klicken Sie in der Tabelle auf das Produkt.

![Synchronisierte Produktdetails](assets/sync-product-detail.png)

### Resynchronisation von Katalogdaten

Um sicherzustellen, dass Ihre Commerce SaaS-Dienste immer auf dem neuesten Stand der Produktinformationen sind, sollten Sie [einen Zeitplan ](https://experienceleague.adobe.com/en/docs/commerce-operations/configuration-guide/cli/manage-indexers#reindex) für die Synchronisierung von Katalogdaten implementieren.

Sie können zwar [manuell ](#manually-resync-catalog) eine Neusynchronisierung von Katalogdaten aus der Commerce-Datenbank mit SaaS-Diensten starten, es wird jedoch nicht empfohlen, da dies die Belastung der Hardware-Ressourcen erhöhen kann. In den folgenden Szenarien kann es jedoch erforderlich sein, den Katalog manuell neu zu synchronisieren:

- Wenn wichtige Änderungen an Ihrem Produktkatalog vorgenommen werden, z. B. das Hinzufügen neuer Produkte, das Aktualisieren von Produktdetails oder das Ändern von Kategorien

- Wenn Sie Abweichungen oder Leistungsprobleme bei der Anzeige von Produktdaten auf Ihren Storefronts feststellen

- Nach Aktualisierungen oder Änderungen an Integrationen zwischen der Commerce-Datenbank und SaaS-Diensten

- Bei der Bereitstellung von Anpassungen oder Konfigurationen, die sich auf das Produktdatenmanagement oder Synchronisierungsprozesse auswirken

Durch die Einhaltung dieser Richtlinien und die proaktive Neusynchronisierung von Katalogdaten nach Bedarf können Sie die Datenkonsistenz, Genauigkeit und Zuverlässigkeit in Ihrem gesamten Adobe Commerce-Ökosystem sicherstellen.

#### Manuelles erneutes Synchronisieren von Katalogen

Wenn Sie Katalogdaten neu synchronisieren müssen, klicken Sie rechts auf der Seite auf **[!UICONTROL Settings]** , um ein Dialogfeld anzuzeigen, in dem Sie eine Neusynchronisierung starten können. Die erneute Synchronisierung von Katalogdaten zwingt den Dienst dazu, Daten aus der Commerce-Datenbank auf SaaS-Dienste zurückzusetzen.

![Produkte manuell synchronisieren](assets/resync-data.png)
