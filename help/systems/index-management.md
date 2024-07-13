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

Die Indexer können auf &quot;Aktualisieren beim Speichern&quot;oder &quot;Planen&quot;eingestellt werden. Alle Indizes können beide Optionen verwenden, mit Ausnahme des Kundenrasters, das nur beim Speichern unterstützt wird. Bei der Indizierung beim Speichern startet Commerce eine Neuindizierung bei Speicheraktionen. Auf der Seite Indexverwaltung wird die Aktualisierung abgeschlossen und der Cache geleert, wobei die Neuindizierungsmeldung innerhalb von ein bis zwei Minuten angezeigt wird. Bei der Neuindizierung in einem Zeitplan wird eine Neuindizierung gemäß einem Zeitplan als Cron-Auftrag ausgeführt. Eine Systemmeldung wird angezeigt, wenn kein [cron-Auftrag](cron.md) verfügbar ist, um ungültige Indexer zu aktualisieren. Ihr Speicher bleibt während der Neuindizierungsprozesse verfügbar.

>[!NOTE]
> Adobe Commerce-Händler, die Live Search, Catalog Service oder Product Recommendations verwenden, haben die Möglichkeit, einen [SaaS-basierten Preisindex](https://experienceleague.adobe.com/docs/commerce-merchant-services/price-indexer/index.html) zu verwenden.

Wenn eine Neuindizierung erforderlich ist, wird oben auf der Seite eine Benachrichtigung angezeigt. Der Index und die Nachricht werden basierend auf dem Neuindizierungsmodus und den möglichen Aktionen, die Sie ausführen, gelöscht. Weitere Informationen zur Indizierung finden Sie unter [Implementieren der Indizierung durch die Anwendung](https://developer.adobe.com/commerce/php/development/components/indexing/#how-the-application-implements-indexing) im _PHP Developer Guide_.

![Indexverwaltung - Aktionen](./assets/index-management.png){width="700" zoomable="yes"}

- Die Indexverwaltung hat eine etwas andere Darstellung für flache Produktkataloge.
- Um Probleme zu vermeiden, wenn mehrere Admin-Benutzer Objekte aktualisieren, die eine automatische Neuindizierung des Triggers erfordern, sollten Sie alle Indexer so einstellen, dass sie planmäßig als [cron-Aufträge](cron.md) ausgeführt werden. Andernfalls kann jedes Mal, wenn ein Objekt gespeichert wird, jedes Objekt mit wechselseitigen Abhängigkeiten zu einem Deadlock führen. Zu den Symptomen eines Deadlock gehören eine hohe CPU-Auslastung und MySQL-Fehler. Als Best Practice wird empfohlen, die geplante Indizierung zu verwenden.
- ![Adobe Commerce](../assets/adobe-logo.svg) (nur Adobe Commerce) Standardmäßig werden Admin-Aktionen wie die Neuindizierung vom System protokolliert und können im Bericht [Aktionsprotokolle](action-log-report.md) angezeigt werden. Die Aktionsprotokollierung kann in der [Protokollierung von Admin-Aktionen](action-log.md) in den erweiterten Admin-Einstellungen Ihres Stores konfiguriert werden.

## Best Practices für die Neuindizierung

Die Neuindizierung und Zwischenspeicherung dienen in Commerce unterschiedlichen Zwecken. Indizes verfolgen Datenbankinformationen, um die Suchleistung zu verbessern, den Datenabruf für Storefronts zu beschleunigen und mehr. [Caches](cache-management.md) speichern geladene Daten, Bilder, Formate und Ähnliches für eine verbesserte Leistung beim Laden und Aufrufen der Storefront.

- Normalerweise sollten Sie die Daten bei der Aktualisierung in Commerce neu indizieren.
- Wenn Sie über einen großen oder mehrere Stores verfügen, können Sie Indexer wie Kategorie und Produkte auf geplante Cron-Aufträge setzen, da eine Neuindizierung möglich ist. Sie können die Neuindizierung auch außerhalb der Spitzenzeiten planen.
- Bei der Neuindizierung müssen Sie nicht auch einen Leerungs-Cache durchführen.
- Bei einer Neuinstallation von Commerce müssen Sie den Cache leeren und die Neuindizierung durchführen.
- Das Leeren von Caches und die Neuindizierung leeren den Cache des Webbrowsers Ihres Computers nicht. Löschen Sie den Browser-Cache, nachdem Sie Aktualisierungen an Ihrer Storefront durchgeführt haben.

## Indexmodus ändern

>[!IMPORTANT]
>
>Bei Stores, die [Adobe Commerce B2B](https://experienceleague.adobe.com/docs/commerce-admin/b2b/introduction.html) verwenden und Elasticsearch als Volltext-Indexer (`catalogsearch_fulltext`) festgelegt haben: Der Volltext-Index muss erneut ausgeführt werden, nachdem sich die Massenberechtigungen geändert haben oder sich der Indexer &quot;Berechtigungen&quot;im Modus &quot;Geplant&quot;befindet.

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL System]** > _[!UICONTROL Tools]_>**[!UICONTROL Index Management]**.

1. Aktivieren Sie das Kontrollkästchen für jeden Indexer, den Sie ändern möchten.

1. Setzen Sie **[!UICONTROL Actions]** auf einen der folgenden Werte:

   - `Update on Save`
   - `Update by Schedule`
   - `Invalidate index`

   >[!IMPORTANT]
   >
   >Das Kundenraster kann nur mit `Update on Save` neu indiziert werden. Dieser Index unterstützt **_nicht_** `Update by Schedule`.

1. Klicken Sie auf **[!UICONTROL Submit]** , um die Änderung auf jeden ausgewählten Indexer anzuwenden.

   **Spalten für die Indexverwaltung**

   | Spalte | Beschreibung |
   | ------ |---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
   | [!UICONTROL Indexer] | Der Name des Indexers. |
   | [!UICONTROL Description] | Eine Beschreibung des Indexers. |
   | [!UICONTROL Mode] | Gibt den aktuellen Aktualisierungsmodus für jeden Indexer an. Optionen: <br/>**[!UICONTROL Update on Save]**- Der Index wird so eingestellt, dass er beim Speichern einer Entitätsänderung aktualisiert wird. Zu diesen Entitäten gehören Produkte, Kategorien und Kunden. Wenn die Speicheraktion abgeschlossen ist, beginnt eine Reihe von Schritten damit, die Änderungen zu erfassen und den Index zu aktualisieren. Die Seite Indexverwaltung aktualisiert und löscht die Neuindizierungsmeldung innerhalb von ein oder zwei Minuten.<br/>**[!UICONTROL Update on Schedule]** - Der Index wird gemäß einem [cron-Auftrag](cron.md) planmäßig aktualisiert. Der Cron-Auftrag enthält das Zeitintervall für die Neuindizierung und schreibt bei Ausführung Aktualisierungen an den Index. |
   | [!UICONTROL Schedule Status] | Zeigt die geplanten Statusaktualisierungen an. |
   | [!UICONTROL Status] | Zeigt einen der folgenden Werte an: <br/>**[!UICONTROL Ready]**- Der Index ist aktuell.<br/>**[!UICONTROL Suspended]** - Die Neuindizierung wird angehalten. <br/>**[!UICONTROL Processing]**- Die Neuindizierung wird derzeit ausgeführt.<br/>**[!UICONTROL Reindex Required]** - Es wurde eine Änderung vorgenommen, die eine Neuindizierung erfordert, die Indexer jedoch nicht automatisch aktualisiert werden können. Überprüfen Sie, ob [cron](cron.md) korrekt verfügbar und konfiguriert ist. |
   | [!UICONTROL Updated] | Gibt Datum und Uhrzeit der letzten Aktualisierung eines Index an. |

   {style="table-layout:auto"}

## Neuindizieren über die Befehlszeile

Commerce bietet über die Befehlszeile zusätzliche Neuindizierungsoptionen. Vollständige Details und Befehlsoptionen finden Sie unter [Neuindizieren](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/manage-indexers.html#reindex){:target=&quot;blank&quot;} im _Konfigurationshandbuch_.

## Index-Trigger-Ereignisse

## Neuindizierung von Triggern

| Indextyp | Neuindizierungsereignis |
| ---------- | ---------------- |
| [!UICONTROL Product Prices] | Hinzufügen der Kundengruppe<br/>Ändern der Konfigurationseinstellungen |
| [!UICONTROL Flat catalog product data] | Hinzufügen von store<br/>Hinzufügen einer Store-Gruppe<br/>Hinzufügen, Bearbeiten oder Löschen von Attributen (für Suchen und Filtern) |
| [!UICONTROL Flat catalog category data] | Hinzufügen von store<br/>Hinzufügen einer Store-Gruppe<br/>Hinzufügen, Bearbeiten oder Löschen von Attributen (für Suchen und Filtern) |
| [!UICONTROL Catalog category/product index] | Hinzufügen, Bearbeiten oder Löschen von Produkten (einzeln, groß und importiert)<br/>Ändern von Produkt-zu-Kategorie-Beziehungen<br/>Hinzufügen, Bearbeiten oder Löschen von Kategorien<br/>Hinzufügen oder Löschen von Stores<br/>Löschen von Store-Gruppen<br/>Löschen von Websites |
| [!UICONTROL Catalog search index] | Hinzufügen, Bearbeiten oder Löschen von Produkten (einzeln, groß und importieren)<br/>Hinzufügen oder Löschen von Stores<br/>Löschen von Store-Gruppen<br/>Löschen von Websites |
| [!UICONTROL Stock status index] | Ändern Sie die Einstellungen für die Lagerbestandskonfiguration. |
| [!UICONTROL Category permissions index] | Hinzufügen von store<br/>Hinzufügen einer Store-Gruppe<br/>Hinzufügen, Löschen oder Aktualisieren von Attributen (für Suchen und Filtern) |

{style="table-layout:auto"}

>[!IMPORTANT]
>
>Die Verwendung eines flachen Katalogs wird nicht mehr als Best Practice empfohlen. Die kontinuierliche Verwendung dieser Funktion führt bekanntermaßen zu Leistungsbeeinträchtigungen und anderen Indizierungsproblemen. Weitere Informationen finden Sie unter [Verwenden eines Flachkatalog-Produkts](../catalog/catalog-flat.md) .

## Indexaktionen und Steuerelemente

| Aktion | Ergebnis | Steuerelemente |
| ------ | ------ | -------- |
| Erstellen eines Stores, einer neuen Kundengruppe oder einer Aktion, die in `Actions that Cause a Full Reindex` aufgeführt ist | Vollständige Neuindizierung | Die vollständige Neuindizierung erfolgt gemäß dem von Ihrem Adobe Commerce- oder Magento Open Source-Cron-Auftrag festgelegten Zeitplan. |
| Massenladen von Elementen (Commerce-Import/-Export, Direct SQL-Abfrage und jede andere Methode, mit der Daten direkt hinzugefügt, geändert oder gelöscht werden) | Teilweise Neuindizierung (nur geänderte Elemente werden neu indiziert) | In der Häufigkeit, die durch Ihren Commerce-Cron-Auftrag bestimmt wird. |
| Ändern des Umfangs (z. B. von global zu website) | Teilweise Neuindizierung (nur geänderte Elemente werden neu indiziert) | In der Häufigkeit, die durch Ihren Commerce-Cron-Auftrag bestimmt wird. |

{style="table-layout:auto"}

## Ereignisse mit vollständiger Neuindizierung des Triggers

| Indexer | Ereignis |
| ------- | ----- |
| [!UICONTROL Catalog Category Flat Indexer] | Erstellen Sie einen Webstore<br/>Erstellen Sie eine Webspeicheransicht<br/>Erstellen oder löschen Sie ein Attribut, das eines der folgenden ist:<br/>- Durchsuchbar oder sichtbar in der erweiterten Suche<br/>- Filterbar<br/>- In Suche filtern<br/>- Wird für die Sortierung verwendet<br/>Ändern Sie ein vorhandenes Attribut in eines der vorherigen.<br/> Speicheroptionen für flache Kategorien aktivieren |
| [!UICONTROL Catalog Product Flat Indexer] | Erstellen Sie einen Webstore<br>Erstellen einer Webspeicheransicht<br/>Erstellen oder löschen Sie ein Attribut, das eines der folgenden ist:<br/>- Durchsuchbar oder sichtbar in der erweiterten Suche<br>- Filterbar<br>- In Suche filtern<br/>- Wird zum Sortieren von <br/>Ändern Sie ein vorhandenes Attribut in eines der vorherigen.<br/> Speicheroptionen für flache Kategorien aktivieren |
| [!UICONTROL Stock status indexer] | Wenn sich die folgenden _Optionen für den Katalog-Bestand_ in der Systemkonfiguration ändern:<br/>`Stock Options` - &quot;Nicht vorrätige Produkte anzeigen&quot;<br/>`Product Stock Options` - &quot;Vorrätig verwalten&quot; |
| [!UICONTROL Price Indexer] | Hinzufügen einer Kundengruppe.<br/>Wenn sich eine der folgenden Optionen für den Katalogbestand in der Systemkonfiguration ändert:<br/>`Stock Options` - &quot;Nicht vorrätige Produkte anzeigen&quot;<br/>`Product Stock Options` - &quot;Lager verwalten&quot;<br/>`Price` - &quot;Umfang des Katalogpreises&quot; |
| [!UICONTROL Category or Product Indexer] | Erstellen oder Löschen einer Store-Ansicht<br/>Löschen eines Stores<br/>Löschen einer Website |

{style="table-layout:auto"}
