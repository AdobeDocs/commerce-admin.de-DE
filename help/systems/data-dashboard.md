---
title: Data Management Dashboard
description: Erfahren Sie, wie Sie auf Einblicke über Datenströme für zugreifen können. [!DNL Catalog Service], [!DNL Live Search], und [!DNL Product Recommendation]s.
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

Das Data Management Dashboard ist für alle Commerce-Händler, die [[!DNL Product Recommendations v6.0.0]](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/product-recommendations/guide-overview), [[!DNL Live Search v4.1.0]](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/live-search/guide-overview)oder [[!DNL Catalog Service v1.17]](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/catalog-service/guide-overview) mit einer aktiven Lizenz.

Das Dashboard für die Datenverwaltung befindet sich unter *System* > Datenübertragung > *Data Management Dashboard*.

![Data Management Dashboard](assets/data-management-dashboard.png)

Das Dashboard enthält die folgenden Felder:

| Feld | Beschreibung |
|--- |--- |
| Anwendungsbereich | Spezifische Website für die synchronisierten Daten. |
| [!DNL Product Recommendations] | Zeigt den Synchronisierungsstatus, die Anzahl der synchronisierten Produkte und eine Tabelle der [anzeigbar](https://experienceleague.adobe.com/en/docs/commerce-admin/config/catalog/inventory#stock-options) synchronisierte Produkte für [!DNL Product Recommendations]. |
| [!DNL Live Search] | Zeigt den Synchronisierungsstatus, die Anzahl der synchronisierten Produkte und eine Tabelle der [anzeigbar](https://experienceleague.adobe.com/en/docs/commerce-admin/config/catalog/inventory#stock-options) synchronisierte Produkte für [!DNL Live Search]. |
| [!DNL Catalog Service] | Zeigt den Synchronisierungsstatus, die Anzahl der synchronisierten Produkte und eine Tabelle der synchronisierten Produkte für an [!DNL Catalog Service]. |
| Einstellungen | Öffnet ein Dialogfeld, in dem Sie [Manuelles erneutes Synchronisieren der Katalogdaten](#resync-catalog-data). |
| Synchronisierungsstatus | Zeigt die Anzahl der Produkte an, die innerhalb der letzten drei Stunden von der Commerce-Datenbank an einen der SaaS-Dienste übertragen wurden. Wenn Sie selten einen Katalog aktualisieren, ist dieser Wert häufig null. Wenn eine Synchronisierung ausgeführt wird, klicken Sie auf **[!UICONTROL Refresh]** um eine aktualisierte Anzahl zu erhalten. |
| Produktanzahl | Gibt die Gesamtanzahl der für den Dienst verfügbaren Katalogprodukte an. Die [!DNL Product Recommendations] und [!DNL Live Search] Dashboards zeigen die Gesamtanzahl der _anzeigbar_ Produkte. [!DNL Catalog Service] filtert keine Produkte nach anzuzeigenden Elementen. Wenn Sie also [!DNL Catalog Service] und [!DNL Live Search] oder [!DNL Product Recommendations] installiert ist, können die beiden Dashboards zwei verschiedene Werte für die Produktanzahl anzeigen. |
| Synchrone Produkte | Enthält Details zu den Produkten im Commerce-Core-Index. Standardmäßig ist diese Tabelle nach &quot;Zuletzt aktualisiert&quot;sortiert. Um ein bestimmtes Produkt zu finden, verwenden Sie die **[!UICONTROL Search by SKU]** -Feld. Klicken Sie auf die Schaltfläche **[!UICONTROL Customize Table]** rechts neben dem Tisch. |

## Verwenden des Daten-Management-Dashboards

Wenn Sie Produkte in der Commerce-Datenbank aktualisieren, werden die Produktdaten gemäß Ihrer Systemkonfiguration an die SaaS-Dienste übertragen. Wenn der Synchronisierungsprozess initiiert wird, **Produktanzahl** gibt die Anzahl der Produkte an, die an SaaS-Dienste gesendet werden.

>[!IMPORTANT]
>
>Die Zeit, die zum Abschluss der Synchronisierung benötigt wird, hängt von der Größe Ihres Katalogs und dem Volumen der aktualisierten Daten ab.

Wenn die Anzahl der verarbeiteten Produkte mit der Anzahl der aktualisierten Produkte übereinstimmt, zeigt dies an, dass die Synchronisierung abgeschlossen ist.

>[!NOTE]
>
>Adobe bietet außerdem eine Befehlszeilenschnittstelle und Systemprotokolle, die Entwickler und Systemintegratoren verwenden können, um Synchronisierungsvorgänge zu verwalten und zu verfolgen und Fehler für Commerce SaaS-Dienste zu beheben. Weitere Informationen finden Sie unter [SaaS-Datenexportanleitung](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/saas-data-export/overview).

### Liste der synchronisierten Produkte

Um die Details eines synchronisierten Produkts anzuzeigen, klicken Sie in der Tabelle auf das Produkt.

![Syncd-Produktdetails](assets/sync-product-detail.png)

### Resynchronisation von Katalogdaten

Um sicherzustellen, dass Ihre Commerce SaaS-Dienste immer auf dem neuesten Stand der Produktinformationen sind, sollten Sie [einen Zeitplan implementieren](https://experienceleague.adobe.com/en/docs/commerce-operations/configuration-guide/cli/manage-indexers#reindex) zum Synchronisieren von Katalogdaten.

Während Sie [manuell initiieren](#manually-resync-catalog) Da Katalogdaten von der Commerce-Datenbank zu SaaS-Diensten resynchron sind, wird dies nicht empfohlen, da dies die Belastung der Hardware-Ressourcen erhöhen kann. In den folgenden Szenarien kann es jedoch erforderlich sein, den Katalog manuell neu zu synchronisieren:

- Wenn wichtige Änderungen an Ihrem Produktkatalog vorgenommen werden, z. B. das Hinzufügen neuer Produkte, das Aktualisieren von Produktdetails oder das Ändern von Kategorien

- Wenn Sie Abweichungen oder Leistungsprobleme bei der Anzeige von Produktdaten auf Ihren Storefronts feststellen

- Nach Aktualisierungen oder Änderungen an Integrationen zwischen der Commerce-Datenbank und SaaS-Diensten

- Bei der Bereitstellung von Anpassungen oder Konfigurationen, die sich auf das Produktdatenmanagement oder Synchronisierungsprozesse auswirken

Durch die Einhaltung dieser Richtlinien und die proaktive Neusynchronisierung von Katalogdaten nach Bedarf können Sie die Datenkonsistenz, Genauigkeit und Zuverlässigkeit in Ihrem gesamten Adobe Commerce-Ökosystem sicherstellen.

#### Manuelles erneutes Synchronisieren von Katalogen

Wenn Sie Katalogdaten erneut synchronisieren müssen, klicken Sie auf **[!UICONTROL Settings]** auf der rechten Seite der Seite ein Dialogfeld anzuzeigen, in dem Sie eine Neusynchronisierung starten können. Die erneute Synchronisierung von Katalogdaten zwingt den Dienst dazu, Daten aus der Commerce-Datenbank auf SaaS-Dienste zurückzusetzen.

![Manuelles Synchronisieren von Produkten](assets/resync-data.png)
