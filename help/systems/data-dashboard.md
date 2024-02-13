---
title: Data Management Dashboard
description: Erfahren Sie mehr über das Data Management Dashboard
feature: Products, Customers, Data Import/Export
source-git-commit: 925af4d3841f2972dfffcd52125a41c4a4b28815
workflow-type: tm+mt
source-wordcount: '291'
ht-degree: 0%

---

# Data Management Dashboard

Das Data Management Dashboard bietet Einblicke in Datenströme für Adobe Commerce SaaS-Produkte. Benutzer von [!DNL Live Search], [!DNL Product Recommendations], und [!DNL Catalog Service] Sie können Produktsynchronisierungsstatus anzeigen und Daten aus einem Dashboard neu synchronisieren.

Das Dashboard für die Datenverwaltung befindet sich unter *System* > Datenübertragung > *Data Management Dashboard*.

![Data Management Dashboard](assets/data-management-dashboard.png)

## Einstellungen

Die Schaltfläche Einstellungen rechts auf der Seite öffnet das [[!DNL Catalog Sync]](https://experienceleague.adobe.com/docs/commerce-merchant-services/user-guides/data-services/catalog-sync.html) Dialogfeld &quot;Einstellungen&quot;.

Normalerweise wird die [!DNL Catalog Sync] Der Prozess wird automatisch ausgeführt, einmal pro Stunde.

Die erneute Synchronisierung von Katalogdaten zwingt den Dienst, Daten aus der Commerce-Datenbank zu filtern und sicherzustellen, dass die neuesten Änderungen im Dienst und auf Ihrer Site übernommen werden. Verwenden Sie diese Schaltfläche, wenn Sie mehrere Produktänderungen vorgenommen haben und diese Änderungen vor der normalen automatischen Synchronisierung aktualisieren müssen.

## Synchronisierungsstatus

Die _[!UICONTROL Sync]_Der Statusbereich zeigt die Anzahl der Produkte an, die in den letzten drei Stunden synchronisiert wurden. Wenn Sie selten einen Katalog aktualisieren, ist dieser Wert häufig null. Klicks **[!UICONTROL Refresh]**, um die Anzahl zu aktualisieren.

## Produktanzahl

Das Bedienfeld &quot;Produktanzahl&quot;gibt die Gesamtanzahl der für den Dienst verfügbaren Katalogprodukte an.

Die [!DNL Catalog Service] Dashboard spiegelt die Gesamtzahl der Produkte im Katalog wider, der für den Dienst verfügbar ist. Dies sind im Allgemeinen alle Produkte in der Commerce-Datenbank.

Die Dashboards &quot;Produkt-Recommendations&quot;und &quot;Live-Suche&quot;zeigen die Gesamtanzahl der [_durchsuchbar_](https://experienceleague.adobe.com/docs/commerce-admin/catalog/catalog/search/search.html) Produkte. Wenn einige Produkte nicht durchsuchbar sind, wird der Unterschied in den Produktsummen zwischen [!DNL Product Recommendations] und [!DNL Live Search], und [!DNL Catalog Service].

## Synchrone Produkte

Die Tabelle &quot;Synchronisierte Katalogprodukte&quot;enthält Details zu den Produkten im Index. Standardmäßig ist diese Tabelle nach &quot;Zuletzt aktualisiert&quot;sortiert.

Um ein bestimmtes Produkt zu finden, verwenden Sie die[!UICONTROL Search by SKU]** -Feld .
Klicken Sie auf die Schaltfläche **[!UICONTROL Customize Table]** rechts neben dem Tisch.
