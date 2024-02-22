---
title: Data Management Dashboard
description: Erfahren Sie, wie Sie auf Einblicke über Datenströme für Catalog Service, Live Search und Product Recommendations zugreifen können.
feature: Products, Customers, Data Import/Export
source-git-commit: eed80afd8755d416d979c362f8c21fe97ce2d2ba
workflow-type: tm+mt
source-wordcount: '258'
ht-degree: 0%

---


# Data Management Dashboard

Das Data Management Dashboard bietet Einblicke in Datenströme für Adobe Commerce SaaS-Produkte. Benutzer von [!DNL Live Search], [!DNL Product Recommendations], und [!DNL Catalog Service] Sie können Produktsynchronisierungsstatus anzeigen und Daten aus einem Dashboard neu synchronisieren.

Das Dashboard für die Datenverwaltung befindet sich unter *System* > Datenübertragung > *Data Management Dashboard*.

![Data Management Dashboard](assets/data-management-dashboard.png)

## Einstellungen

Die **[!UICONTROL Settings]** -Schaltfläche rechts auf der Seite öffnet das Dialogfeld, in dem Sie die Katalogdaten neu synchronisieren können.

Die erneute Synchronisierung von Katalogdaten zwingt den Dienst, Daten aus der Commerce-Datenbank abzurufen. Diese Aktion wird normalerweise beim erstmaligen Onboarding verwendet, wenn die Katalogsynchronisierung einige Stunden lang nicht ausgeführt wurde.

## Synchronisierungsstatus

Die _[!UICONTROL Sync]_Der Statusbereich zeigt die Anzahl der Produkte an, die in den letzten drei Stunden synchronisiert wurden. Wenn Sie selten einen Katalog aktualisieren, ist dieser Wert häufig null. Klicks **[!UICONTROL Refresh]**, um die Anzahl zu aktualisieren.

## Produktanzahl

Das Bedienfeld &quot;Produktanzahl&quot;gibt die Gesamtanzahl der für den Dienst verfügbaren Katalogprodukte an.

Die [!DNL Product Recommendations] und [!DNL Live Search] Dashboards zeigen die Gesamtanzahl der _anzeigbar_ Produkte. [!DNL Catalog Service] filtert keine Produkte nach anzuzeigenden Elementen. Wenn Sie also [!DNL Catalog Service] und [!DNL Live Search] oder [!DNL Product Recommendations] installiert ist, können die beiden Dashboards zwei verschiedene Werte für die Produktanzahl anzeigen.

## Synchrone Produkte

Die Tabelle Synchronisierte Produkte enthält Details zu den Produkten im Index. Standardmäßig ist diese Tabelle nach &quot;Zuletzt aktualisiert&quot;sortiert.

Um ein bestimmtes Produkt zu finden, verwenden Sie die **[!UICONTROL Search by SKU]** Feld .
Klicken Sie auf die Schaltfläche **[!UICONTROL Customize Table]** rechts neben dem Tisch.
