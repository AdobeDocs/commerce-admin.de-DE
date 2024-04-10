---
title: Indexverwaltung
description: Erfahren Sie mehr über die Indexverwaltung, einschließlich der Aktionen zur Neuindizierung von Trigger und Best Practices.
exl-id: cbb249a2-b957-44fe-bf81-df795a8fd5d1
feature: System, Configuration
source-git-commit: 28b8e430336090666402f3f2868311ef98d9217d
workflow-type: tm+mt
source-wordcount: '1282'
ht-degree: 0%

---

# Indexverwaltung

Adobe Commerce und Magento Open Source indizieren sich automatisch neu, wenn sich ein oder mehrere Elemente ändern. Zu den Aktionen, die eine Neuindizierung von Triggern ermöglichen, gehören Preisänderungen, das Erstellen von Preisregeln für Kataloge oder Warenkörbe, das Hinzufügen neuer Kategorien usw. Um die Leistung zu optimieren, sammelt Commerce Daten mithilfe von Indexern in speziellen Tabellen. Wenn sich die Daten ändern, müssen die indizierten Tabellen aktualisiert - oder neu indiziert werden. Commerce indiziert neu als Hintergrundprozess, und der Zugriff auf Ihren Store bleibt während der Prozesse erhalten.

Die Neuindizierung von Daten beschleunigt die Verarbeitung und verkürzt die Wartezeit des Kunden. Wenn Sie beispielsweise den Preis eines Artikels von 4,99 USD auf 3,99 USD ändern, indiziert Commerce die Daten neu, um die Preisänderung im Geschäft anzuzeigen. Ohne Indizierung müsste Commerce den Preis jedes Produkts laufend berechnen. Dies würde z. B. die Preisregeln für Warenkörbe, Paketpreise, Rabatte, Stufenpreise usw. umfassen. Das Laden des Preises für ein Produkt kann länger dauern, als der Kunde bereit ist zu warten.

Die Indexer können so eingestellt werden, dass sie entweder beim Speichern oder planmäßig aktualisiert werden. Alle Indizes können eine der beiden Optionen verwenden, mit Ausnahme des Kundenrasters, das nur beim Speichern unterstützt. Beim Indizieren beim Speichern startet Commerce eine Neuindizierung von Speicheraktionen. Auf der Seite „Indexverwaltung“ wird die Aktualisierung abgeschlossen und der Cache geleert, wobei die Neuindizierungsmeldung innerhalb von ein bis zwei Minuten angezeigt wird. Bei der Neuindizierung nach einem Zeitplan wird eine Neuindizierung nach einem Zeitplan als Cron-Auftrag ausgeführt. Eine Systemmeldung wird angezeigt, wenn ein [Cron-Job](cron.md) kann keine Indexer aktualisieren, die ungültig werden. Ihr Store bleibt während der Neuindizierung zugänglich.

>[!NOTE]
> Adobe Commerce-Händler, die die Live-Suche, den Katalog-Service oder die Produkt-Recommendations verwenden, haben die Möglichkeit, einen [SaaS-basierter Preisindexer](https://experienceleague.adobe.com/docs/commerce-merchant-services/price-indexer/index.html).

Wenn eine Neuindizierung erforderlich ist, wird oben auf der Seite eine Benachrichtigung angezeigt. Der Index und die Nachricht werden je nach Neuindizierungsmodus und den von Ihnen durchgeführten potenziellen Aktionen gelöscht. Weitere Informationen zur Indizierung finden Sie in der [Implementieren der Indizierung durch die Anwendung](https://developer.adobe.com/commerce/php/development/components/indexing/#how-the-application-implements-indexing) in der _PHP-Entwicklerhandbuch_.

![Indexverwaltung - Aktionen](./assets/index-management.png){width="700" zoomable="yes"}

- Die Indexverwaltung bietet eine etwas andere Darstellung für flache Produktkataloge.
- Um Probleme zu vermeiden, wenn mehrere Admin-Benutzerinnen und -Benutzer Objekte aktualisieren, die den Trigger automatisch neu indizieren, wird empfohlen, für alle Indexer die Ausführung planmäßig festzulegen [Cron-Aufträge](cron.md). Andernfalls kann jedes Mal, wenn ein Objekt gespeichert wird, jedes Objekt mit Interdependenzen einen Deadlock verursachen. Zu den Symptomen eines Deadlocks gehören hohe CPU-Auslastung und MySQL-Fehler. Als Best Practice wird empfohlen, die geplante Indizierung zu verwenden.
- ![Adobe Commerce](../assets/adobe-logo.svg) (Nur Adobe Commerce) Standardmäßig werden Admin-Aktionen wie eine Neuindizierung vom System protokolliert und können in der [Bericht zu Aktionslogs](action-log-report.md). Die Aktionsprotokollierung kann in der [Protokollierung von Admin-Aktionen](action-log.md) In den erweiterten Admin-Einstellungen Ihres Stores.

## Best Practices für die Neuindizierung

Die Neuindizierung und das Caching haben in Commerce unterschiedliche Zwecke. Indizes verfolgen Datenbankinformationen, um die Suchleistung zu erhöhen, den Datenabruf für Storefronts zu beschleunigen und vieles mehr. [Caches](cache-management.md) Speichern Sie geladene Daten, Bilder, Formate und dergleichen, um das Laden und den Zugriff auf die Storefront zu verbessern.

- In der Regel möchten Sie beim Aktualisieren von Daten in Commerce eine Neuindizierung durchführen.
- Wenn Sie einen großen oder mehrere Stores haben, sollten Sie Indexer wie Kategorien und Produkte aufgrund der Möglichkeit einer Neuindizierungs-Schleife auf geplante Cron-Aufträge setzen. Möglicherweise möchten Sie die Neuindizierung außerhalb der Spitzenzeiten anhand eines Zeitplans festlegen.
- Bei der Neuindizierung müssen Sie nicht auch einen Leer-Cache ausführen.
- Bei neuen Commerce-Installationen müssen Sie den Cache leeren und neu indizieren.
- Durch Leeren von Caches und Neuindizierung wird der Webbrowser-Cache Ihres Computers nicht geleert. Löschen Sie den Browser-Cache, nachdem Sie Aktualisierungen an Ihrer Storefront abgeschlossen haben.

## Ändern des Indexmodus

>[!IMPORTANT]
>
>Für Stores, die [B2B für Adobe Commerce](https://experienceleague.adobe.com/docs/commerce-admin/b2b/introduction.html) und als Volltext ( ) Elasticsearch festgelegt haben`catalogsearch_fulltext`)-Indexer: Der Volltextindex muss nach jeder Massenberechtigungsänderung oder dann erneut ausgeführt werden, wenn sich der Indexer „Berechtigungen“ im Modus „Geplant“ befindet.

1. Auf der _Admin_ Seitenleiste, zu gehen **[!UICONTROL System]** > _[!UICONTROL Tools]_>**[!UICONTROL Index Management]**.

1. Aktivieren Sie das Kontrollkästchen für jeden Indexer, den Sie ändern möchten.

1. set **[!UICONTROL Actions]** eine der folgenden Möglichkeiten:

   - `Update on Save`
   - `Update by Schedule`
   - `Invalidate index`

   >[!IMPORTANT]
   >
   >Kundenraster kann nur neu indiziert werden mit `Update on Save`. Dieser Index tut Folgendes **_nicht_** Support `Update by Schedule`.

1. Klick **[!UICONTROL Submit]** , um die Änderung auf jeden ausgewählten Indexer anzuwenden.

   **Spalten zur Indexverwaltung**

   | Spalte | Beschreibung |
   | ------ |---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
   | [!UICONTROL Indexer] | Der Name des Indexers. |
   | [!UICONTROL Description] | Eine Beschreibung des Indexers. |
   | [!UICONTROL Mode] | Gibt den aktuellen Aktualisierungsmodus für jeden Indexer an. Optionen: <br/>**[!UICONTROL Update on Save]**- Der Index wird so eingestellt, dass er bei jeder Entitätsänderung aktualisiert wird. Zu diesen Entitäten gehören Produkte, Kategorien und Kunden. Wenn die Speicheraktion abgeschlossen ist, beginnt eine Reihe von Schritten, die Änderungen abzufangen und den Index zu aktualisieren. Die Seite „Indexverwaltung“ wird aktualisiert und die Neuindizierungsmeldung wird innerhalb von ein bis zwei Minuten geleert.<br/>**[!UICONTROL Update on Schedule]** - Der Index wird so eingestellt, dass er planmäßig aktualisiert wird gemäß einer [Cron-Job](cron.md). Der Cron-Auftrag umfasst das Zeitplanintervall für die Neuindizierung, wobei bei der Ausführung Aktualisierungen in den Index geschrieben werden. |
   | [!UICONTROL Schedule Status] | Zeigt die Aktualisierungen des Zeitplanstatus an. |
   | [!UICONTROL Status] | Zeigt eine der folgenden Optionen an: <br/>**[!UICONTROL Ready]**— Der Index ist auf dem neuesten Stand.<br/>**[!UICONTROL Suspended]** - Die Neuindizierung wurde angehalten. <br/>**[!UICONTROL Processing]**- Die Neuindizierung wird derzeit ausgeführt.<br/>**[!UICONTROL Reindex Required]** - Es wurde eine Änderung vorgenommen, die neu indiziert werden muss, aber die Indexer können nicht automatisch aktualisiert werden. Prüfen, ob [Cron](cron.md) ist verfügbar und richtig konfiguriert. |
   | [!UICONTROL Updated] | Gibt das Datum und die Uhrzeit der letzten Aktualisierung eines Index an. |

   {style="table-layout:auto"}

## Neuindizieren über die Befehlszeile

Commerce bietet zusätzliche Neuindizierungsoptionen über die Befehlszeile. Ausführliche Informationen und Befehlsoptionen finden Sie unter [neu indizieren](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/manage-indexers.html#reindex){:target=„blank„} in der _Konfigurationshandbuch_.

## Trigger-Ereignisse indizieren

## Neuindizierung von Trigger

| Indextyp | Ereignis für die Neuindizierung |
| ---------- | ---------------- |
| [!UICONTROL Product Prices] | Kundengruppe hinzufügen<br/>Konfigurationseinstellungen ändern |
| [!UICONTROL Flat catalog product data] | Store hinzufügen<br/>Speichergruppe hinzufügen<br/>Attribut hinzufügen, bearbeiten oder löschen (für die Suche und Filterung) |
| [!UICONTROL Flat catalog category data] | Store hinzufügen<br/>Speichergruppe hinzufügen<br/>Attribut hinzufügen, bearbeiten oder löschen (für die Suche und Filterung) |
| [!UICONTROL Catalog category/product index] | Hinzufügen, Bearbeiten oder Löschen von Produkten (Einzel-, Massen- und Importprodukte)<br/>Produkt-zu-Kategorie-Beziehungen ändern<br/>Kategorien hinzufügen, bearbeiten oder löschen<br/>Hinzufügen oder Löschen von Stores<br/>Speichergruppen löschen<br/>Löschen von Websites |
| [!UICONTROL Catalog search index] | Hinzufügen, Bearbeiten oder Löschen von Produkten (Einzel-, Massen- und Importprodukte)<br/>Hinzufügen oder Löschen von Stores<br/>Speichergruppen löschen<br/>Löschen von Websites |
| [!UICONTROL Stock status index] | Ändern Sie die Inventarkonfigurationseinstellungen. |
| [!UICONTROL Category permissions index] | Store hinzufügen<br/>Speichergruppe hinzufügen<br/>Attribut hinzufügen, löschen oder aktualisieren (für die Suche und Filterung) |

{style="table-layout:auto"}

>[!IMPORTANT]
>
>Die Verwendung eines flachen Katalogs wird nicht mehr als Best Practice empfohlen. Es ist bekannt, dass die fortgesetzte Verwendung dieser Funktion zu Leistungseinbußen und anderen Indizierungsproblemen führt. Siehe [Flaches Katalogprodukt verwenden](../catalog/catalog-flat.md) für weitere Informationen.

## Indexaktionen und Steuerelemente

| Aktion | Ergebnis | Steuerelemente |
| ------ | ------ | -------- |
| Erstellen eines Stores, einer neuen Kundengruppe oder einer beliebigen Aktion, die in aufgeführt ist `Actions that Cause a Full Reindex` | Vollständige Neuindizierung | Die vollständige Neuindizierung erfolgt nach dem Zeitplan, der von Ihrem Adobe Commerce- oder Magento Open Source-Cron-Auftrag festgelegt wird. |
| Massenladen von Elementen (Commerce-Import/Export, Direct SQL-Abfrage und alle anderen Methoden, die Daten direkt hinzufügen, ändern oder löschen) | Teilweise Neuindizierung (nur geänderte Elemente werden neu indiziert) | Mit der Häufigkeit, die von Ihrem Commerce Cron-Auftrag bestimmt wird. |
| Ändern des Umfangs (z. B. von global zu website) | Teilweise Neuindizierung (nur geänderte Elemente werden neu indiziert) | Mit der Häufigkeit, die von Ihrem Commerce Cron-Auftrag bestimmt wird. |

{style="table-layout:auto"}

## Ereignisse mit vollständiger Neuindizierung im Trigger

| Indexer | Ereignis |
| ------- | ----- |
| [!UICONTROL Catalog Category Flat Indexer] | Erstellen eines Webspeichers<br/>Erstellen einer Web-Store-Ansicht<br/>Erstellen oder löschen Sie ein Attribut mit einer der folgenden Eigenschaften:<br/>- Durchsuchbar oder in der erweiterten Suche sichtbar<br/>- Filterbar<br/>- Filterbar bei der Suche<br/>- Wird für die Sortierung verwendet<br/>Ändern Sie ein vorhandenes Attribut in eines der vorherigen Attribute.<br/>Optionen für flache Storefronts aktivieren |
| [!UICONTROL Catalog Product Flat Indexer] | Erstellen eines Webspeichers<br>Erstellen einer Web-Store-Ansicht<br/>Erstellen oder löschen Sie ein Attribut mit einer der folgenden Eigenschaften:<br/>- Durchsuchbar oder in der erweiterten Suche sichtbar<br>- Filterbar<br>- Filterbar bei der Suche<br/>- Wird für die Sortierung verwendet <br/>Ändern Sie ein vorhandenes Attribut in eines der vorherigen Attribute.<br/>Optionen für flache Storefronts aktivieren |
| [!UICONTROL Stock status indexer] | Wenn Folgendes geschieht _Optionen für das Kataloginventar_ Änderung der Systemkonfiguration:<br/>`Stock Options` - Nicht vorrätige Produkte anzeigen<br/>`Product Stock Options` - Lagerverwaltung |
| [!UICONTROL Price Indexer] | Hinzufügen einer Kundengruppe.<br/>Wenn sich eine der folgenden Kataloginventaroptionen in der Systemkonfiguration ändert:<br/>`Stock Options` - Nicht vorrätige Produkte anzeigen<br/>`Product Stock Options` - Lagerverwaltung<br/>`Price` - Katalogpreis-Umfang |
| [!UICONTROL Category or Product Indexer] | Erstellen oder Löschen einer Store-Ansicht<br/>Löschen eines Stores<br/>Löschen einer Website |

{style="table-layout:auto"}
