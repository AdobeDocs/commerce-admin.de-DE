---
title: Cache-Verwaltung
description: Erfahren Sie, wie Sie die Cache-Management-Tools verwenden, die eine einfache Möglichkeit bieten, die Leistung Ihrer Site zu verbessern.
exl-id: c87f85ca-81b9-4cbf-9817-3d779397eefd
feature: Cache, System
source-git-commit: fdf04be69754d0209772d9ceb244e3808f3b61d3
workflow-type: tm+mt
source-wordcount: '1811'
ht-degree: 0%

---

# Cache-Verwaltung

Das Cache-Management-System von Adobe Commerce und Magento Open Source bietet eine einfache Möglichkeit, die Leistung Ihrer Site zu verbessern. Wenn ein Cache eine Aktualisierung erfordert, wird eine Benachrichtigung mit einem Link zur [!UICONTROL Cache Management]-Seite angezeigt, um die Aktualisierung abzuschließen.

![Produktattribut speichern - Cache-Nachricht aktualisieren](./assets/product-attribute-save-msg-update-cache.png){width="500"}

Auf der Seite _[!UICONTROL Cache Management]_wird der Status jedes primären Caches und des zugehörigen Tags angezeigt. Die großen Schaltflächen in der oberen rechten Ecke können verwendet werden, um den Cache oder den All-Inclusive-Cache-Speicher zu leeren. Unten auf der Seite können Sie mit zusätzlichen Schaltflächen den Cache für Katalogproduktbilder und den JavaScript-/CSS-Cache leeren.

>[!IMPORTANT]
>
>Wenn Katalogentitäten geändert werden, kann dies Auswirkungen auf andere Seiten haben und mehrere Caches gleichzeitig ungültig machen. Wenn Sie die Seite zur Cache-Verwaltung durchgehen, werden ungültige Elemente angezeigt, die aktualisiert werden müssen, wenn sie _**nicht direkt bearbeitet)**_. Diese Invalidierung tritt beispielsweise auf, wenn Sie ein Produkt im Katalog bearbeiten, das einer beliebigen Kategorie zugewiesen ist, oder wenn Sie eine zugehörige Produktregel ändern.

Aktualisieren Sie nach dem Löschen eines Cache immer Ihren Browser, um sicherzustellen, dass Sie die neuesten Dateien sehen können. Durch Löschen des Commerce-Cache wird der Webbrowser-Cache nicht gelöscht. Möglicherweise müssen Sie den Browser-Cache löschen, um aktualisierte Inhalte anzuzeigen.

Weitere technische Informationen zum Caching in Adobe Commerce finden Sie unter [Übersicht über den Cache](https://developer.adobe.com/commerce/frontend-core/guide/caching/){:target="_blank"} im _Commerce Frontend-Entwicklerhandbuch_.

Greifen Sie auf die _[!UICONTROL Cache Management]_zu, indem Sie eine der folgenden Aktionen ausführen:

- Klicken Sie auf den Link **[!UICONTROL Cache Management]** in der Nachricht über dem Arbeitsbereich.
- Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL System]** > _[!UICONTROL Tools]_>**[!UICONTROL Cache Management]**.

![Cache-Verwaltung](./assets/cache-management-invalid.png){width="700" zoomable="yes"}

## Best Practices für das Caching

Neuindizierung und Caching haben in Commerce unterschiedliche Zwecke. [Indizes](index-management.md) Verfolgen Sie Datenbankinformationen, um die Suchleistung zu erhöhen, den Datenabruf für Storefronts zu beschleunigen und vieles mehr. Caches speichern geladene Daten, Bilder, Formate und dergleichen, um das Laden und Zugreifen auf die Storefront zu verbessern.

- Leeren Sie den Cache immer nach der Installation von Erweiterungen/Modulen. Sie können eine oder mehrere Erweiterungen installieren und dann den Cache leeren.
- Leeren Sie den Cache nach der Installation von Commerce. Bei Neuinstallationen sollten Sie auch eine Neuindizierung durchführen.
- Leeren Sie den Cache nach dem Upgrade von einer Version von Open Source oder Commerce auf eine andere.
- Berücksichtigen Sie beim Leeren von Caches den Typ des Caches und planen Sie die Leerung zu anderen Zeiten als Spitzenzeiten. Wählen Sie beispielsweise einen Zeitpunkt aus, zu dem nur wenige Kunden die Website verwenden, z. B. spät in der Nacht oder am frühen Morgen. Das Löschen von Cache-Typen während Spitzenzeiten kann die Last für den Administrator erhöhen und dazu führen, dass die Site heruntergefahren wird, bis der Vorgang abgeschlossen ist.
- Bei [Neuindizierung](index-management.md) müssen Sie den Cache nicht leeren.

## Cache-Management-Rollenressourcen

Sie können Benutzern nach Rolle Zugriff auf bestimmte Cache-Wartungsaktionen zuweisen, einschließlich Optionen zum Anzeigen, Umschalten und Leeren von Caches. Adobe empfiehlt, Löschaktionen nur für Benutzer auf Administratorebene zu aktivieren. Die Bereitstellung des Zugriffs auf alle Cache-Management-Funktionen kann die Leistung Ihrer Storefront beeinträchtigen.

![Rollenressourcen - Cache-Verwaltung](./assets/permissions-role-resources-cache-management.png){width="600" zoomable="yes"}

Informationen zum Zuweisen von Ressourcen zur Gewährung des Zugriffs für Admin-Benutzerkonten finden Sie unter [Rollenressourcen](permissions-user-roles.md#role-resources). Die folgenden Ressourcen steuern den Zugriff auf die Cache-Verwaltungstools:

- [!UICONTROL Clean Cache Actions]

   - [!UICONTROL Flush Cache Storage]
   - [!UICONTROL Flush Magento Cache]

- [!UICONTROL Cache Type Management]

   - [!UICONTROL Toggle Cache Type]
   - [!UICONTROL Refresh Cache Type]

- [!UICONTROL Additional Cache Management]

   - [!UICONTROL Catalog Images Cache]
   - [!UICONTROL Flush Js/Css]
   - [!UICONTROL Flush Static Files]

## Spezifische Caches aktualisieren

1. Aktivieren Sie für jeden Cache, der aktualisiert werden soll, das Kontrollkästchen am Anfang der Zeile.

1. Legen Sie **[!UICONTROL Actions]** auf `Refresh` fest und klicken Sie auf **[!UICONTROL Submit]**.

## Massenaktion aktualisieren

1. Um eine Gruppe von Caches auszuwählen, setzen Sie **[!UICONTROL Mass Actions]** auf einen der folgenden Werte:

   - `Select All`
   - `Select Visible`

1. Aktivieren Sie das Kontrollkästchen für jeden zu aktualisierenden Cache.

1. Legen Sie **[!UICONTROL Actions]** auf `Refresh` fest und klicken Sie auf **[!UICONTROL Submit]**.

## Leeren des Cache für Produktbilder

1. Klicken Sie unter _[!UICONTROL Additional Cache Management]_auf **[!UICONTROL Flush Catalog Images Cache]**, um die vorgenerierten Produktbilddateien zu löschen.

   Die `Image cache was cleaned` wird oben im Arbeitsbereich angezeigt.

1. Löschen Sie den Cache Ihres Browsers.

## Leeren des JavaScript/CSS-Cache

1. Löschen Sie unter _[!UICONTROL Additional Cache Management]_die Dateien JavaScript und CSS, die durch Klicken auf &quot;**[!UICONTROL Flush JavaScript/CSS Cache]**&quot; in einer Datei zusammengeführt wurden.

   Die `The JavaScript/CSS cache has been cleaned` wird oben im Arbeitsbereich angezeigt.

1. Löschen Sie den Cache Ihres Browsers.

## Leeren mithilfe der Befehlszeile

Systemadministratoren und Entwickler mit Zugriff auf den Commerce-Anwendungsserver können die Cache- und Cache-Konfiguration auch über die Befehlszeile mithilfe der Commerce-CLI verwalten. Siehe [Verwalten des Cache](https://experienceleague.adobe.com/en/docs/commerce-operations/configuration-guide/cli/manage-cache#clean-and-flush-cache-types){:target="_blank"} im _Konfigurationshandbuch_.

## Kontrollen

| Kontrolle | Beschreibung |
|---------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Mass Actions] | Aktiviert das Kontrollkästchen für mehrere Caches. Optionen: <br/>**[!UICONTROL Select All]**— Aktiviert das Kontrollkästchen aller Caches.<br/>** Auswahl aufheben **- Löscht das Kontrollkästchen aller Caches.<br/>**[!UICONTROL Select Visible]** - Aktiviert das Kontrollkästchen aller sichtbaren Caches. <br/>**[!UICONTROL Unselect Visible]**— Löscht das Kontrollkästchen für alle sichtbaren Caches. |
| [!UICONTROL Actions] | Bestimmt die Aktion, die auf alle ausgewählten Caches angewendet werden soll. Optionen: <br/>**[!UICONTROL Enable]**— Aktiviert alle ausgewählten Caches.<br/>**[!UICONTROL Disable]** — Deaktiviert alle ausgewählten Caches. <br/>**[!UICONTROL Refresh]**— Aktualisiert alle ausgewählten Caches. |
| [!UICONTROL Submit] | Wendet die Aktion auf alle ausgewählten Caches an. |

{style="table-layout:auto"}

### Schaltflächen

| Schaltfläche | Beschreibung |
|-----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Flush Magento Cache] | Entfernt alle Elemente im standardmäßigen Commerce-Cache (`var/cache`) entsprechend den zugehörigen Commerce-Tags. |
| [!UICONTROL Flush Cache Storage] | Entfernt alle Elemente aus dem Cache, unabhängig vom Commerce-Tag. Wenn Ihr System einen alternativen Cache-Speicherort verwendet, werden alle zwischengespeicherten Dateien, die von anderen Anwendungen verwendet werden, während des Prozesses entfernt. |
| [!UICONTROL Flush Catalog Images Cache] | Entfernt alle Katalogbilder mit Wasserzeichen, die automatisch in der Größe angepasst und in `media/catalog/product/cache` gespeichert werden. Wenn kürzlich hochgeladene Bilder nicht im Katalog angezeigt werden, versuchen Sie, den Katalog zu leeren und Ihren Browser zu aktualisieren. |
| [!UICONTROL Flush JavaScript/CSS Cache] | Entfernt die zusammengeführte Kopie von JavaScript- und CSS-Dateien aus dem Cache. Wenn die letzten Änderungen am Stylesheet oder an JavaScript nicht im Store angezeigt werden, versuchen Sie, den JavaScript-/CSS-Cache zu leeren und Ihren Browser zu aktualisieren. |
| [!UICONTROL Flush Static Files Cache] | Entfernt vorverarbeitete Ansichtsdateien und statische Dateien. |

{style="table-layout:auto"}

### Caches

Auf der Seite [!UICONTROL Cache Management] werden die Cache-Typen mit ihrem aktuellen Status aufgeführt, die Sie über Admin verwalten können. In diesem Abschnitt werden die von Adobe Commerce unterstützten Standard-Cache-Typen beschrieben. Die Spalten _Cache_ Tag und _Cache-ID_ beschreiben die im Commerce-Anwendungs-Code verwendeten Werte:

- `cache_type_id` definiert die eindeutige Kennung für einen Cache-Typ.

- `%CACHE_TYPE_TAG%` definiert das eindeutige Tag, das beim Gültigkeitsbereich des Cache-Typs verwendet werden soll.

Entwickelnde und Systemintegratoren verwenden diese Werte, um die Zwischenspeicherung zu konfigurieren und zu verwalten, wenn sie Adobe Commerce anpassen oder mit ihm integrieren, z. B. um Integrationen mit GraphQL-APIs zu entwickeln. Der `cache type id` wird auch für die Cache-Verwaltung über die Befehlszeile des Anwendungsservers unter Verwendung der Commerce-CLI verwendet. Beispielsweise zeigt ` bin/magento cache:status config` den aktuellen Status des Konfigurations-Caches an.

>[!NOTE]
>
>Entwickelnde und Systemintegratoren können das Cache-Management-System von Commerce anpassen und erweitern, um benutzerdefinierte Module und Integrationen zu unterstützen. Weitere Informationen finden Sie unter [Konfigurieren des ](https://experienceleague.adobe.com/en/docs/commerce-operations/configuration-guide/cache/caching-overview)&quot; im _Adobe Commerce-Konfigurationshandbuch_.

<!-- prettier-ignore -->

#### Detail der Cache-Liste

| Cache | Beschreibung | Cache-Tag | Cache-ID |
|-------|------------|----------|----------|
| [!UICONTROL Configuration] | Commerce erfasst die XML-Konfiguration aus allen Modulen, führt sie zusammen und speichert das zusammengeführte Ergebnis im Cache.<br>**[!UICONTROL System]**- `config.xml`,`local.xml`<br>**[!UICONTROL Module]** - `config.xml`<br><br>Dieser Cache enthält auch speicherspezifische Einstellungen, die im Dateisystem und in der Datenbank gespeichert sind. Bereinigen oder leeren Sie diesen Cache-Typ nach dem Ändern von Konfigurationsdateien. | `CONFIG` | `config` |
| [!UICONTROL Layouts] | Kompilierte Seiten-Layouts, d. h. die Layout-Komponenten aus allen Komponenten. Diesen Cache-Typ nach dem Ändern von Layout-Dateien bereinigen oder leeren. | `LAYOUT_GENERAL_CACHE_TAG` | `layout` |
| [!UICONTROL Blocks HTML output] | HTML von Seitenfragmenten pro Block. Bereinigen oder leeren Sie diesen Cache-Typ, nachdem Sie die Ansichtsebene geändert haben. | `BLOCK_HTML` | `block_html` |
| [!UICONTROL Collections Data] | Sammlungsdatendateien, die die Ergebnisse von Datenbankabfragen speichern. Bei Bedarf bereinigt Commerce diesen Cache automatisch, aber Drittanbieterentwickler können beliebige Daten in jedes Segment des Caches einfügen. Löschen Sie diesen Cache-Typ oder leeren Sie ihn, wenn Ihr benutzerdefiniertes Modul Logik verwendet, die zu Cache-Einträgen führt, die Commerce nicht bereinigen kann. | `COLLECTION_DATA` | `collections` |
| [!UICONTROL Reflections] | Löscht die API-Schnittstellenreflektionsdaten, die normalerweise zur Laufzeit generiert werden. | `REFLECTION` | `reflection` |
| `Database DDL operations` | Datenbankschema. Bei Bedarf bereinigt Commerce diesen Cache automatisch, aber Drittanbieterentwickler können beliebige Daten in jedes Segment des Caches einfügen. Löschen Sie diesen Cache-Typ, nachdem Sie benutzerdefinierte Änderungen am Datenbankschema vorgenommen haben. (Mit anderen Worten: Es handelt sich um Aktualisierungen, die Commerce nicht selbst vornimmt.) Eine Möglichkeit, das Datenbankschema automatisch zu aktualisieren, besteht darin, den Befehl „magento setup:db-schema:upgrade“ zu verwenden. | `DB_DDL` | `db_ddl` |
| [!UICONTROL Compiled Config] | Ergebnisse der Code-Kompilierung. | `COMPILED_CONFIG` | `compiled_config` |
| [!UICONTROL Webhooks Response Cache] | Zwischenspeichert Antworten auf Webhook-Anfragen. Weitere Informationen finden Sie im [Webhooks-Handbuch](https://developer.adobe.com/commerce/extensibility/webhooks/release-notes/#enhancements-2) in der Commerce-Entwicklerdokumentation. | `WEBHOOKS_RESPONSE` | `webhooks_response` |
| [!UICONTROL EAV types and attributes] | Zwischenspeichert Entitätstypdeklarationen für Metadaten, die sich auf Attribute für Entitätsattributwerte (EAV) beziehen. Zu den Attributen gehören Store-Labels, Links zu zugehörigem PHP-Code, Attribut-Rendering, Sucheinstellungen usw. In der Regel ist es nicht erforderlich, diesen Cache-Typ zu bereinigen oder zu leeren. | `EAV` | `eav` |
| [!UICONTROL Customer Notification] | Temporäre Benachrichtigungen, die in der Benutzeroberfläche angezeigt werden. | `CUSTOMER_NOTIFICATION` | `customer_notification` |
| [!UICONTROL GraphQL Query Resolver Results] | Zwischenspeichert die Ergebnisse von GraphQL-Abfrageauflösern für Kunden-, CMS-Seiten-, CMS-Block- und Produktmediensammlungs-Entitäten. Lassen Sie diesen Cache aktiviert, um die Leistung von GraphQL zu verbessern. | `GRAPHQL_QUERY_RESOLVER_RESULT` | `graphql_query_resolver_result` |
| [!UICONTROL Integrations Configuration] | Konfigurationsdatei für die Integration. Diesen Cache nach dem Ändern oder Hinzufügen von Integrationen bereinigen oder leeren. | `INTEGRATION` | `config_integration` |
| [!UICONTROL Integrations API Configuration] | Konfiguration kompilierter Integrations-APIs für Store-Integrationen. | `INTEGRATION_API_CONFIG` | `config_integration_api` |
| [!UICONTROL Admin UI SDK Cache] | speichert Anpassungen im Admin-Cache. Siehe [Admin-Konfiguration und -](https://developer.adobe.com/commerce/extensibility/admin-ui-sdk/configuration/)) im _Handbuch zur Admin-Benutzeroberfläche in SDK_. | `ADMIN_UI_SDK` | `admin_ui_sdk` |
| [!UICONTROL Page Cache] | Vollständige Seitenzwischenspeicherung. | `FPC` | `full_page` |
| [!UICONTROL Target Rule] | Zielregelindex | `TARGET_RULE` | `target_rule` |
| [!UICONTROL Web Services Configuration] | Zwischenspeichern der Web-API-Struktur. | `WEBSERVICE` | `config_webservice` |
| [!UICONTROL Translations] | Übersetzungsdateien. | `TRANSLATE` | `translate` |

{style="table-layout:auto"}

## Vollständige Seitenzwischenspeicherung

Adobe Commerce und Magento Open Source verwenden das Caching ganzer Seiten auf dem Server, um Kategorie-, Produkt- und CMS-Seiten schnell anzuzeigen. Das Caching ganzer Seiten verbessert die Antwortzeit und reduziert die Last auf dem Server. Ohne Zwischenspeicherung muss jede Seite möglicherweise Codeblöcke ausführen und Informationen aus der Datenbank abrufen. Wenn jedoch die Zwischenspeicherung ganzer Seiten aktiviert ist, kann eine vollständig generierte Seite direkt aus dem Cache gelesen werden.

>[!NOTE]
>
>Es wird empfohlen[ „Varnish Cache](https://varnish-cache.org/){:target="_blank"} nur in einer Produktionsumgebung zu verwenden.

Zwischengespeicherte Inhalte können zur Verarbeitung von Anfragen ähnlicher Besuchstypen verwendet werden. Infolgedessen können Seiten, die einem gelegentlichen Besucher angezeigt werden, von Seiten abweichen, die einem Kunden angezeigt werden. Zum Zwischenspeichern ist jeder Besuch einer von drei Typen:

- `Non-sessioned`: Während eines nicht sitzungsbezogenen Besuchs zeigt der Käufer Seiten an, interagiert jedoch nicht mit dem Store. Das System speichert den Inhalt jeder aufgerufenen Seite zwischen und stellt ihn anderen, nicht sessionierten Käufern zur Verfügung.
- `Sessioned` - Während eines Sitzungsbesuchs wird Käufern, die mit dem Store interagieren, eine Sitzungs-ID zugewiesen. Interaktionen umfassen Aktivitäten wie den Vergleich von Produkten oder das Hinzufügen von Produkten zum Warenkorb. Zwischengespeicherte Seiten, die während der Sitzung generiert werden, werden nur von diesem Kunden während der Sitzung verwendet.
- `Customer` - Kundensitzungen werden für Kunden erstellt, die sich mit ihrem registrierten Konto anmelden und einkaufen. Während der Sitzung können Kunden Sonderangebote, Aktionen und Preise basierend auf ihrer zugewiesenen Kundengruppe präsentiert werden.

Technische Informationen finden Sie unter [Konfigurieren und Verwenden von ](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cache/varnish/config-varnish.html){:target="_blank"} und [Verwenden von Redis für die Commerce-Seite und ](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cache/redis/redis-pg-cache.html){:target="_blank"}-Cache im _Konfigurationshandbuch_.

**_So konfigurieren Sie den Vollseiten-Cache:_**

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Advanced]** und wählen Sie **[!UICONTROL System]**.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Full Page Cache]** .

   ![Erweiterte Konfiguration - vollständiger Seiten-Cache](../configuration-reference/advanced/assets/system-full-page-cache.png){width="600" zoomable="yes"}

1. Legen Sie **[!UICONTROL Caching Application]** auf eine der folgenden Einstellungen fest:

   - `Built-in Application`
   - `Varnish Caching`

1. Um den Timeout für den Seiten-Cache festzulegen, geben Sie den **[!UICONTROL TTL for public content]** ein. (Der Standardwert lautet `86400`)

1. Geben Sie die **[!UICONTROL Handles param size]** ein, um die maximale Anzahl von [Layout](https://developer.adobe.com/commerce/frontend-core/guide/layouts/#layout-handles)Handles) anzugeben, die am [`{BASE-URL}/page_cache/block/esi`](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cache/use-varnish-esi.html) HTTP-Endpunkt verarbeitet werden sollen. Durch Größenbeschränkungen können die Sicherheit und Leistung verbessert werden. (Der Standardwert lautet `100`)

1. Wenn Sie Lack verwenden, füllen Sie den Abschnitt **[!UICONTROL Varnish Configuration]** wie folgt aus:

   - **[!UICONTROL Access list]** : Geben Sie die IP-Adressen ein, die die Varnish-Konfiguration bereinigen können, um eine Konfigurationsdatei zu generieren. Trennen Sie mehrere Einträge durch Kommas. Der Standardwert ist `localhost`.

   - **[!UICONTROL Backend host]** - Geben Sie die IP-Adresse des Backend-Hosts ein, der Konfigurationsdateien generiert. Der Standardwert ist `localhost`.

   - **[!UICONTROL Backend port]** - Identifizieren Sie den Backend-Port, der zum Generieren von Konfigurationsdateien verwendet wird. Der Standardwert lautet: `8080`.

   - **[!UICONTROL Grace period]** - Geben Sie die Anzahl der Sekunden an, die als Übergangsphase zum Generieren von Konfigurationsdateien verwendet werden sollen. Siehe [Erweiterte Lackkonfiguration](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cache/config-varnish-advanced.html) im _Konfigurationshandbuch_.

   - Um die Konfiguration als `varnish.vcl`-Datei zu exportieren, klicken Sie auf die Schaltfläche für die verwendete Varnish-Version.

   ![Erweiterte Konfiguration - Vollständige Seiten-Cache-Lackierung](../configuration-reference/advanced/assets/system-full-page-cache-varnish.png){width="600" zoomable="yes"}

1. Klicken Sie abschließend auf **[!UICONTROL Save Config]**.
