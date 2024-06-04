---
title: Indexverwaltung
description: Erfahren Sie mehr über die Indexverwaltung, einschließlich der Aktionen für die Neuindizierung von Triggern und Best Practices.
exl-id: cbb249a2-b957-44fe-bf81-df795a8fd5d1
feature: System, Configuration
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '1281'
ht-degree: 0%

---

# Indexverwaltung

Adobe Commerce und Magento Open Source werden automatisch neu indiziert, wenn sich ein oder mehrere Elemente ändern. Zu den Aktionen, die die Neuindizierung von Triggern beinhaltet, gehören Preisänderungen, das Erstellen von Katalogen oder Preisregeln für Warenkorb, das Hinzufügen neuer Kategorien usw. Zur Leistungsoptimierung sammelt Commerce Daten mithilfe von Indexern in spezielle Tabellen. Da sich die Daten ändern, müssen die indizierten Tabellen aktualisiert oder neu indiziert werden. Commerce wird als Hintergrundprozess neu indiziert und Ihr Store bleibt während der Prozesse zugänglich.

Die Neuindizierung von Daten beschleunigt die Verarbeitung und verkürzt die Wartezeit für den Kunden. Wenn Sie beispielsweise den Preis eines Artikels von 4,99 US-Dollar in 3,99 US-Dollar ändern, werden die Daten von Commerce neu indiziert, um die Preisänderung im Store anzuzeigen. Ohne Indizierung müsste Commerce den Preis für jedes Produkt direkt berechnen, die Preisregeln für Warenkörbe, Bundle-Preise, Rabatte, Tier-Preise usw. Das Laden des Preises für ein Produkt kann länger dauern, als der Kunde bereit ist zu warten.

Die Indexer können auf &quot;Aktualisieren beim Speichern&quot;oder &quot;Planen&quot;eingestellt werden. Alle Indizes können beide Optionen verwenden, mit Ausnahme des Kundenrasters, das nur beim Speichern unterstützt wird. Bei der Indizierung beim Speichern startet Commerce eine Neuindizierung bei Speicheraktionen. Auf der Seite Indexverwaltung wird die Aktualisierung abgeschlossen und der Cache geleert, wobei die Neuindizierungsmeldung innerhalb von ein bis zwei Minuten angezeigt wird. Bei der Neuindizierung in einem Zeitplan wird eine Neuindizierung gemäß einem Zeitplan als Cron-Auftrag ausgeführt. Eine Systemmeldung wird angezeigt, wenn eine [Cron-Auftrag](cron.md) ist nicht verfügbar, um ungültige Indexer zu aktualisieren. Ihr Speicher bleibt während der Neuindizierungsprozesse verfügbar.

>[!NOTE]
> Adobe Commerce-Händler, die Live Search, Catalog Service oder Product Recommendations verwenden, haben die Möglichkeit, eine [SaaS-basierter Preisindexer](https://experienceleague.adobe.com/docs/commerce-merchant-services/price-indexer/index.html).

Wenn eine Neuindizierung erforderlich ist, wird oben auf der Seite eine Benachrichtigung angezeigt. Der Index und die Nachricht werden basierend auf dem Neuindizierungsmodus und den möglichen Aktionen, die Sie ausführen, gelöscht. Weitere Informationen zur Indizierung finden Sie unter [Implementieren der Indizierung durch die Anwendung](https://developer.adobe.com/commerce/php/development/components/indexing/#how-the-application-implements-indexing) im _PHP-Entwicklerhandbuch_.

![Indexverwaltung - Aktionen](./assets/index-management.png){width="700" zoomable="yes"}

- Die Indexverwaltung hat eine etwas andere Darstellung für flache Produktkataloge.
- Um Probleme zu vermeiden, wenn mehrere Admin-Benutzer Objekte aktualisieren, die eine automatische Neuindizierung des Triggers ermöglichen, sollten Sie alle Indexer so einstellen, dass sie planmäßig ausgeführt werden [Cron-Aufträge](cron.md). Andernfalls kann jedes Mal, wenn ein Objekt gespeichert wird, jedes Objekt mit wechselseitigen Abhängigkeiten zu einem Deadlock führen. Zu den Symptomen eines Deadlock gehören eine hohe CPU-Auslastung und MySQL-Fehler. Als Best Practice wird empfohlen, die geplante Indizierung zu verwenden.
- ![Adobe Commerce](../assets/adobe-logo.svg) (Nur Adobe Commerce) Standardmäßig werden Admin-Aktionen wie die Neuindizierung vom System protokolliert und können im [Bericht &quot;Aktionsprotokolle&quot;](action-log-report.md). Die Protokollierung von Aktionen kann im Abschnitt [Protokollierung von Admin-Aktionen](action-log.md) in den erweiterten Admin-Einstellungen Ihres Stores.

## Best Practices für die Neuindizierung

Die Neuindizierung und Zwischenspeicherung dienen in Commerce unterschiedlichen Zwecken. Indizes verfolgen Datenbankinformationen, um die Suchleistung zu verbessern, den Datenabruf für Storefronts zu beschleunigen und mehr. [Caches](cache-management.md) Speichern Sie geladene Daten, Bilder, Formate und Ähnliches, um die Leistung beim Laden und Aufrufen der Storefront zu steigern.

- Normalerweise sollten Sie die Daten bei der Aktualisierung in Commerce neu indizieren.
- Wenn Sie über einen großen oder mehrere Stores verfügen, können Sie Indexer wie Kategorie und Produkte auf geplante Cron-Aufträge setzen, da eine Neuindizierung möglich ist. Sie können die Neuindizierung auch außerhalb der Spitzenzeiten planen.
- Bei der Neuindizierung müssen Sie nicht auch einen Leerungs-Cache durchführen.
- Bei einer Neuinstallation von Commerce müssen Sie den Cache leeren und die Neuindizierung durchführen.
- Das Leeren von Caches und die Neuindizierung leeren den Cache des Webbrowsers Ihres Computers nicht. Löschen Sie den Browser-Cache, nachdem Sie Aktualisierungen an Ihrer Storefront durchgeführt haben.

## Indexmodus ändern

>[!IMPORTANT]
>
>Für Stores, die [Adobe Commerce B2B](https://experienceleague.adobe.com/docs/commerce-admin/b2b/introduction.html) und haben Elasticsearch als Volltext festgelegt (`catalogsearch_fulltext`) Indexer: Der Volltext-Index muss erneut ausgeführt werden, nachdem sich die Massenberechtigungen geändert haben oder sich der Indexer &quot;Berechtigungen&quot;im Modus &quot;Geplant&quot;befindet.

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL System]** > _[!UICONTROL Tools]_>**[!UICONTROL Index Management]**.

1. Aktivieren Sie das Kontrollkästchen für jeden Indexer, den Sie ändern möchten.

1. Satz **[!UICONTROL Actions]** auf einen der folgenden Werte zu:

   - `Update on Save`
   - `Update by Schedule`
   - `Invalidate index`

   >[!IMPORTANT]
   >
   >Kundenraster kann nur mit neu indiziert werden. `Update on Save`. Dieser Index **_not_** Support `Update by Schedule`.

1. Klicks **[!UICONTROL Submit]** , um die Änderung auf jeden ausgewählten Indexer anzuwenden.

   **Indexverwaltungsspalten**

   | Spalte | Beschreibung |
   | ------ |---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
   | [!UICONTROL Indexer] | Der Name des Indexers. |
   | [!UICONTROL Description] | Eine Beschreibung des Indexers. |
   | [!UICONTROL Mode] | Gibt den aktuellen Aktualisierungsmodus für jeden Indexer an. Optionen: <br/>**[!UICONTROL Update on Save]**- Der Index wird so eingestellt, dass er jedes Mal aktualisiert wird, wenn eine Entitätsänderung gespeichert wird. Zu diesen Entitäten gehören Produkte, Kategorien und Kunden. Wenn die Speicheraktion abgeschlossen ist, beginnt eine Reihe von Schritten damit, die Änderungen zu erfassen und den Index zu aktualisieren. Die Seite Indexverwaltung aktualisiert und löscht die Neuindizierungsmeldung innerhalb von ein oder zwei Minuten.<br/>**[!UICONTROL Update on Schedule]** - Der Index wird so eingestellt, dass er planmäßig gemäß einem [Cron-Auftrag](cron.md). Der Cron-Auftrag enthält das Zeitintervall für die Neuindizierung und schreibt bei Ausführung Aktualisierungen an den Index. |
   | [!UICONTROL Schedule Status] | Zeigt die geplanten Statusaktualisierungen an. |
   | [!UICONTROL Status] | Zeigt eine der folgenden Optionen an: <br/>**[!UICONTROL Ready]**— Der Index ist aktuell.<br/>**[!UICONTROL Suspended]** - Die Neuindizierung wird angehalten. <br/>**[!UICONTROL Processing]**- Die Neuindizierung wird derzeit ausgeführt.<br/>**[!UICONTROL Reindex Required]** - Es wurde eine Änderung vorgenommen, die eine Neuindizierung erfordert, die Indexer jedoch nicht automatisch aktualisiert werden können. Überprüfen Sie, ob [cron](cron.md) ist verfügbar und korrekt konfiguriert. |
   | [!UICONTROL Updated] | Gibt Datum und Uhrzeit der letzten Aktualisierung eines Index an. |

   {style="table-layout:auto"}

## Neuindizieren über die Befehlszeile

Commerce bietet über die Befehlszeile zusätzliche Neuindizierungsoptionen. Ausführliche Informationen und Befehlsoptionen finden Sie unter [Reindex](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/manage-indexers.html#reindex){:target=&quot;blank&quot;} im _Konfigurationshandbuch_.

## Index-Trigger-Ereignisse

## Neuindizierung von Triggern

| Indextyp | Neuindizierungsereignis |
| ---------- | ---------------- |
| [!UICONTROL Product Prices] | Hinzufügen einer Kundengruppe<br/>Konfigurationseinstellungen ändern |
| [!UICONTROL Flat catalog product data] | Store hinzufügen<br/>Store-Gruppe hinzufügen<br/>Hinzufügen, Bearbeiten oder Löschen von Attributen (für Suchen und Filtern) |
| [!UICONTROL Flat catalog category data] | Store hinzufügen<br/>Store-Gruppe hinzufügen<br/>Hinzufügen, Bearbeiten oder Löschen von Attributen (für Suchen und Filtern) |
| [!UICONTROL Catalog category/product index] | Hinzufügen, Bearbeiten oder Löschen von Produkten (einzeln, groß und importiert)<br/>Ändern von Beziehungen zwischen Produkten und Kategorien<br/>Hinzufügen, Bearbeiten oder Löschen von Kategorien<br/>Hinzufügen oder Löschen von Stores<br/>Löschen von Store-Gruppen<br/>Websites löschen |
| [!UICONTROL Catalog search index] | Hinzufügen, Bearbeiten oder Löschen von Produkten (einzeln, groß und importiert)<br/>Hinzufügen oder Löschen von Stores<br/>Löschen von Store-Gruppen<br/>Websites löschen |
| [!UICONTROL Stock status index] | Ändern Sie die Einstellungen für die Lagerbestandskonfiguration. |
| [!UICONTROL Category permissions index] | Store hinzufügen<br/>Store-Gruppe hinzufügen<br/>Hinzufügen, Löschen oder Aktualisieren von Attributen (für Suchen und Filtern) |

{style="table-layout:auto"}

>[!IMPORTANT]
>
>Die Verwendung eines flachen Katalogs wird nicht mehr als Best Practice empfohlen. Die kontinuierliche Verwendung dieser Funktion führt bekanntermaßen zu Leistungsbeeinträchtigungen und anderen Indizierungsproblemen. Siehe [Einfache Katalogprodukte verwenden](../catalog/catalog-flat.md) für weitere Informationen.

## Indexaktionen und Steuerelemente

| Aktion | Ergebnis | Steuerelemente |
| ------ | ------ | -------- |
| Erstellen Sie einen Store, eine neue Kundengruppe oder eine beliebige Aktion, die unter `Actions that Cause a Full Reindex` | Vollständige Neuindizierung | Die vollständige Neuindizierung erfolgt gemäß dem von Ihrem Adobe Commerce- oder Magento Open Source-Cron-Auftrag festgelegten Zeitplan. |
| Massenladen von Elementen (Commerce-Import/-Export, Direct SQL-Abfrage und jede andere Methode, mit der Daten direkt hinzugefügt, geändert oder gelöscht werden) | Teilweise Neuindizierung (nur geänderte Elemente werden neu indiziert) | In der Häufigkeit, die durch Ihren Commerce-Cron-Auftrag bestimmt wird. |
| Ändern des Umfangs (z. B. von global zu website) | Teilweise Neuindizierung (nur geänderte Elemente werden neu indiziert) | In der Häufigkeit, die durch Ihren Commerce-Cron-Auftrag bestimmt wird. |

{style="table-layout:auto"}

## Ereignisse mit vollständiger Neuindizierung des Triggers

| Indexer | Ereignis |
| ------- | ----- |
| [!UICONTROL Catalog Category Flat Indexer] | Webstore erstellen<br/>Erstellen einer Webspeicheransicht<br/>Erstellen oder löschen Sie ein Attribut, das einem der folgenden Werte entspricht:<br/>- In der erweiterten Suche durchsuchbar oder sichtbar<br/>- Filtern<br/>- In der Suche filtern<br/>- Zur Sortierung verwendet<br/>Ändern Sie ein vorhandenes Attribut in eines der vorangehenden.<br/>Speicheroptionen für flache Kategorien aktivieren |
| [!UICONTROL Catalog Product Flat Indexer] | Webstore erstellen<br>Erstellen einer Webspeicheransicht<br/>Erstellen oder löschen Sie ein Attribut, das einem der folgenden Werte entspricht:<br/>- In der erweiterten Suche durchsuchbar oder sichtbar<br>- Filtern<br>- In der Suche filtern<br/>- Zur Sortierung verwendet <br/>Ändern Sie ein vorhandenes Attribut in eines der vorangehenden.<br/>Speicheroptionen für flache Kategorien aktivieren |
| [!UICONTROL Stock status indexer] | Wenn Folgendes _Optionen für Kataloginventar_ Änderung der Systemkonfiguration:<br/>`Stock Options` - Nicht vorrätige Produkte anzeigen<br/>`Product Stock Options` - Verwalten von Lagern |
| [!UICONTROL Price Indexer] | Hinzufügen einer Kundengruppe.<br/>Wenn sich eine der folgenden Optionen für den Katalogbestand in der Systemkonfiguration ändert:<br/>`Stock Options` - Nicht vorrätige Produkte anzeigen<br/>`Product Stock Options` - Verwalten von Lagern<br/>`Price` - Umfang des Katalogpreises |
| [!UICONTROL Category or Product Indexer] | Erstellen oder Löschen einer Store-Ansicht<br/>Löschen eines Stores<br/>Website löschen |

{style="table-layout:auto"}
