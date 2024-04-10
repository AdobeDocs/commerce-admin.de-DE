---
title: Cache-Verwaltung
description: Erfahren Sie, wie Sie die Cache-Management-Tools verwenden, die eine einfache Möglichkeit bieten, die Leistung Ihrer Site zu verbessern.
exl-id: c87f85ca-81b9-4cbf-9817-3d779397eefd
feature: Cache, System
source-git-commit: add2259bf326d7812999e3e7d4724af10f7497c0
workflow-type: tm+mt
source-wordcount: '1845'
ht-degree: 0%

---

# Cache-Verwaltung

Das Cache-Management-System von Adobe Commerce und Magento Open Source bietet eine einfache Möglichkeit, die Leistung Ihrer Site zu verbessern. Wenn ein Cache eine Aktualisierung erfordert, wird oben im Arbeitsbereich ein Hinweis mit einem Link zur [!UICONTROL Cache Management] Seite, auf der Sie Caches anzeigen und aktualisieren können.

![Produktattribut speichern - Cache-Nachricht aktualisieren](./assets/product-attribute-save-msg-update-cache.png){width="500"}

Die _[!UICONTROL Cache Management]_zeigt den Status jedes primären Caches und des zugehörigen Tags an. Die großen Schaltflächen in der oberen rechten Ecke können verwendet werden, um den Cache oder den All-Inclusive-Cache-Speicher zu leeren. Unten auf der Seite können Sie mit zusätzlichen Schaltflächen den Cache für Katalogproduktbilder und den JavaScript-/CSS-Cache leeren.

>[!IMPORTANT]
>
>Wenn Katalogentitäten geändert werden, kann dies Auswirkungen auf andere Seiten haben und mehrere Caches gleichzeitig ungültig machen. Wenn Sie die Seite zur Cache-Verwaltung durchgehen, werden möglicherweise ungültige Elemente angezeigt, die aktualisiert werden müssen, wenn sie aktualisiert wurden _**Nicht direkt bearbeitet**_. Diese Invalidierung tritt beispielsweise auf, wenn Sie ein Produkt im Katalog bearbeiten, das einer beliebigen Kategorie zugewiesen ist, oder wenn Sie eine zugehörige Produktregel ändern.

Aktualisieren Sie nach dem Löschen eines Cache immer Ihren Browser, um sicherzustellen, dass Sie die neuesten Dateien sehen können. Durch Löschen des Commerce-Cache wird der Webbrowser-Cache nicht gelöscht. Möglicherweise müssen Sie den Browser-Cache löschen, um aktualisierte Inhalte anzuzeigen.

Weitere technische Informationen zum Adobe Commerce-Caching finden Sie unter [Cache-Übersicht](https://developer.adobe.com/commerce/frontend-core/guide/caching/){:target=„_blank„} in der _Commerce-Frontend-Entwicklungshandbuch_.

Zugriff auf _[!UICONTROL Cache Management]_Führen Sie einen der folgenden Schritte aus:

- Klicken Sie auf die Schaltfläche **[!UICONTROL Cache Management]** -Link in der Nachricht über dem Arbeitsbereich.
- Auf der _Admin_ Seitenleiste, zu gehen **[!UICONTROL System]** > _[!UICONTROL Tools]_>**[!UICONTROL Cache Management]**.

![Cache-Verwaltung](./assets/cache-management-invalid.png){width="700" zoomable="yes"}

## Best Practices für das Caching

Die Neuindizierung und das Caching haben in Commerce unterschiedliche Zwecke. [Indizes](index-management.md) Verfolgen Sie Datenbankinformationen, um die Suchleistung zu erhöhen, den Datenabruf für Storefronts zu beschleunigen und vieles mehr. Caches speichern geladene Daten, Bilder, Formate und dergleichen, um das Laden und den Zugriff auf die Storefront zu verbessern.

- Leeren Sie den Cache immer nach der Installation von Erweiterungen/Modulen. Sie können eine oder mehrere Erweiterungen installieren und dann den Cache leeren.
- Leeren Sie den Cache nach der Installation von Commerce. Bei Neuinstallationen sollten Sie auch eine Neuindizierung vornehmen.
- Leeren Sie den Cache nach dem Upgrade von einer Version von Open Source oder Commerce auf eine andere.
- Berücksichtigen Sie beim Leeren von Caches die Art des Caches und planen Sie die Leerung zu anderen Zeiten als Spitzenzeiten. Wählen Sie beispielsweise einen Zeitpunkt aus, zu dem nur wenige Kunden auf die Website zugreifen können, z. B. spät in der Nacht oder am frühen Morgen. Das Löschen einiger Cache-Typen in Spitzenzeiten führt zu einer hohen Belastung für den Administrator und kann zu einer Downsite führen, bis sie abgeschlossen ist.
- Wenn [Neuindizierung](index-management.md)Es ist nicht erforderlich, auch einen Leer-Cache durchzuführen.

## Cache-Management-Rollenressourcen

Der Zugriff auf bestimmte Cache-Wartungsaktionen kann Benutzern nach Rolle zugewiesen werden, einschließlich Optionen zum Anzeigen, Umschalten und Leeren von Caches. Adobe empfiehlt, Löschaktionen nur für Benutzer auf Administratorebene zu aktivieren. Die Bereitstellung des Zugriffs auf alle Cache-Management-Funktionen kann die Leistung Ihrer Storefront beeinträchtigen.

![Rollenressourcen - Cache-Verwaltung](./assets/permissions-role-resources-cache-management.png){width="600" zoomable="yes"}

Informationen zum Zuweisen von Ressourcen, um Admin-Benutzerkonten Zugriff zu gewähren, finden Sie unter [Rollenressourcen](permissions-user-roles.md#role-resources). Die folgenden Ressourcen steuern den Zugriff auf die Cache-Verwaltungstools:

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

1. set **[!UICONTROL Actions]** bis `Refresh` und klicken Sie auf **[!UICONTROL Submit]**.

## Massenaktion aktualisieren

1. Um eine Gruppe von Caches auszuwählen, legen Sie Folgendes fest **[!UICONTROL Mass Actions]** eine der folgenden Möglichkeiten:

   - `Select All`
   - `Select Visible`

1. Aktivieren Sie das Kontrollkästchen jedes Caches, der von der Aktion angesprochen werden soll.

1. set **[!UICONTROL Actions]** bis `Refresh` und klicken Sie auf **[!UICONTROL Submit]**.

## Leeren des Cache für Produktbilder

1. Unter _[!UICONTROL Additional Cache Management]_, klicken Sie auf **[!UICONTROL Flush Catalog Images Cache]**, um die vorgenerierten Produktbilddateien zu löschen.

   Die `Image cache was cleaned` Die Meldung wird oben im Arbeitsbereich angezeigt.

1. Löschen Sie den Cache Ihres Browsers.

## Leeren des JavaScript/CSS-Cache

1. Unter _[!UICONTROL Additional Cache Management]_, klicken Sie auf **[!UICONTROL Flush JavaScript/CSS Cache]**, um alle JavaScript- und CSS-Dateien zu löschen, die in einer Datei zusammengeführt wurden.

   Die `The JavaScript/CSS cache has been cleaned` Die Meldung wird oben im Arbeitsbereich angezeigt.

1. Löschen Sie den Cache Ihres Browsers.

## Leeren mithilfe der Befehlszeile

Systemadministratoren und Entwickler mit Zugriff auf den Commerce-Anwendungs-Server können die Cache- und Cache-Konfiguration auch über die Befehlszeile mithilfe der Commerce-CLI verwalten. Siehe [Cache verwalten](https://experienceleague.adobe.com/en/docs/commerce-operations/configuration-guide/cli/manage-cache#:~:text=You%20can%20also%20clean%20and,bin%2Fmagento%20cache%3Aclean%20.) in der _Konfigurationshandbuch_.{:target=„_blank„}.

## Steuerelemente

| Kontrolle | Beschreibung |
|---------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Mass Actions] | Aktiviert das Kontrollkästchen für mehrere Caches. Optionen: <br/>**[!UICONTROL Select All]**— Aktiviert das Kontrollkästchen aller Caches.<br/>** Auswahl aufheben **— Löscht das Kontrollkästchen für alle Caches.<br/>**[!UICONTROL Select Visible]** — Aktiviert das Kontrollkästchen aller sichtbaren Caches. <br/>**[!UICONTROL Unselect Visible]**— Löscht das Kontrollkästchen für alle sichtbaren Caches. |
| [!UICONTROL Actions] | Bestimmt die Aktion, die auf alle ausgewählten Caches angewendet werden soll. Optionen: <br/>**[!UICONTROL Enable]**— Aktiviert alle ausgewählten Caches.<br/>**[!UICONTROL Disable]** — Deaktiviert alle ausgewählten Caches. <br/>**[!UICONTROL Refresh]**— Aktualisiert alle ausgewählten Caches. |
| [!UICONTROL Submit] | Wendet die Aktion auf alle ausgewählten Caches an. |

{style="table-layout:auto"}

### Schaltflächen

| Schaltfläche | Beschreibung |
|-----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Flush Magento Cache] | Entfernt alle Elemente im Standard-Commerce-Cache (`var/cache`), entsprechend den zugehörigen Commerce-Tags. |
| [!UICONTROL Flush Cache Storage] | Entfernt alle Elemente aus dem Cache, unabhängig vom Commerce-Tag. Wenn Ihr System einen alternativen Cache-Speicherort verwendet, werden alle zwischengespeicherten Dateien, die von anderen Anwendungen verwendet werden, während des Prozesses entfernt. |
| [!UICONTROL Flush Catalog Images Cache] | Entfernt alle automatisch skalierten und mit Wasserzeichen versehenen Katalogbilder, die in gespeichert sind. `media/catalog/product/cache`. Wenn kürzlich hochgeladene Bilder nicht im Katalog angezeigt werden, versuchen Sie, den Katalog zu leeren und Ihren Browser zu aktualisieren. |
| [!UICONTROL Flush JavaScript/CSS Cache] | Entfernt die zusammengeführte Kopie von JavaScript- und CSS-Dateien aus dem Cache. Wenn die letzten Änderungen am Stylesheet oder an JavaScript nicht im Store widergespiegelt werden, versuchen Sie, den JavaScript/CSS-Cache zu leeren und Ihren Browser zu aktualisieren. |
| [!UICONTROL Flush Static Files Cache] | Entfernt vorverarbeitete Ansichtsdateien und statische Dateien. |

{style="table-layout:auto"}

### Caches

Die [!UICONTROL Cache Management] auf dieser Seite werden die Cache-Typen aufgelistet, die Sie über Admin mit ihrem aktuellen Status verwalten können. In diesem Abschnitt werden die von Adobe Commerce unterstützten Standard-Cache-Typen beschrieben. Die _Cache-Tag_ und _Cache-ID_ Spalten beschreiben die im Commerce-Anwendungs-Code verwendeten Werte:

- `cache_type_id` Definiert die eindeutige Kennung für einen Cache-Typ.

- `%CACHE_TYPE_TAG%` Definiert das eindeutige Tag, das beim Gültigkeitsbereich des Cache-Typs verwendet werden soll.

Entwickelnde und Systemintegratoren verwenden diese Werte, um die Zwischenspeicherung zu konfigurieren und zu verwalten, wenn sie Adobe Commerce anpassen oder mit ihm integrieren, z. B. um Integrationen mit GraphQL-APIs zu entwickeln. Die `cache type id` wird auch für die Cache-Verwaltung über die Befehlszeile des Anwendungsservers mithilfe der Commerce-CLI verwendet, z. B. ` bin/magento cache:status config` zeigt den aktuellen Status des Konfigurations-Caches an.

>[!NOTE]
>
>Entwickler und Systemintegratoren können das Commerce-Cache-Management-System anpassen und erweitern, um benutzerdefinierte Module und Integrationen zu unterstützen. Einzelheiten siehe [Konfigurieren der Zwischenspeicherung](https://experienceleague.adobe.com/en/docs/commerce-operations/configuration-guide/cache/caching-overview) in der _Adobe Commerce-Konfigurationshandbuch_.

<!-- prettier-ignore -->

#### Details der Cache-Liste

| Cache | Beschreibung | Cache-Tag | Cache-ID |
|-------|------------|----------|----------|
| [!UICONTROL Configuration] | Commerce erfasst die XML-Konfiguration aus allen Modulen, führt sie zusammen und speichert das zusammengeführte Ergebnis im Cache.<br>**[!UICONTROL System]**-  `config.xml`,`local.xml`<br>**[!UICONTROL Module]** - `config.xml`<br><br>Dieser Cache enthält auch speicherspezifische Einstellungen, die im Dateisystem und in der Datenbank gespeichert sind. Bereinigen oder leeren Sie diesen Cache-Typ nach dem Ändern von Konfigurationsdateien. | `CONFIG` | `config` |
| [!UICONTROL Layouts] | Kompilierte Seiten-Layouts, d. h. die Layout-Komponenten aus allen Komponenten. Bereinigen oder leeren Sie diesen Cache-Typ nach der Änderung von Layout-Dateien. | `LAYOUT_GENERAL_CACHE_TAG` | `layout` |
| [!UICONTROL Blocks HTML output] | HTML von Seitenfragmenten pro Block. Bereinigen oder leeren Sie diesen Cache-Typ, nachdem Sie die Ansichtsebene geändert haben. | `BLOCK_HTML` | `block_html` |
| [!UICONTROL Collections Data] | Sammlungsdatendateien, die die Ergebnisse von Datenbankabfragen speichern. Bei Bedarf bereinigt Commerce diesen Cache automatisch, aber Drittanbieterentwickler können beliebige Daten in jedes Segment des Caches einfügen. Bereinigen oder leeren Sie diesen Cache-Typ, wenn Ihr benutzerdefiniertes Modul Logik verwendet, die zu Cache-Einträgen führt, die Commerce nicht bereinigen kann. | `COLLECTION_DATA` | `collections` |
| [!UICONTROL Reflections] | Löscht die API-Schnittstellenreflektionsdaten, die normalerweise zur Laufzeit generiert werden. | `REFLECTION` | `reflection` |
| `Database DDL operations` | Datenbankschema. Bei Bedarf bereinigt Commerce diesen Cache automatisch, aber Drittanbieterentwickler können beliebige Daten in jedes Segment des Caches einfügen. Bereinigen oder leeren Sie diesen Cache-Typ, nachdem Sie benutzerdefinierte Änderungen am Datenbankschema vorgenommen haben. (Mit anderen Worten: Es handelt sich um Aktualisierungen, die Commerce nicht selbst herstellt.) Eine Möglichkeit, das Datenbankschema automatisch zu aktualisieren, besteht in der Verwendung des Magento-Setups:db-schema:Upgrade-Befehl. | `DB_DDL` | `db_ddl` |
| [!UICONTROL Compiled Config] | Ergebnisse der Code-Kompilierung. | `COMPILED_CONFIG` | `compiled_config` |
| [!UICONTROL Webhooks Response Cache] | Zwischenspeichert Antworten auf Webhook-Anfragen. Weitere Informationen finden Sie in der [Handbuch zu Webhooks](https://developer.adobe.com/commerce/extensibility/webhooks/release-notes/#enhancements-2) in der Commerce-Entwicklerdokumentation. | `WEBHOOKS_RESPONSE` | `webhooks_response` |
| [!UICONTROL EAV types and attributes] | Entitätstypdeklarations-Cache für Metadaten, die sich auf EAV-Attribute beziehen (z. B. Speicherbezeichnungen, Links zu zugehörigem PHP-Code, Attribut-Rendering, Sucheinstellungen usw.). In der Regel ist es nicht erforderlich, diesen Cache-Typ zu bereinigen oder zu leeren. | `EAV` | `eav` |
| [!UICONTROL Customer Notification] | Temporäre Benachrichtigungen, die in der Benutzeroberfläche angezeigt werden. | `CUSTOMER_NOTIFICATION` | `customer_notification` |
| [!UICONTROL GraphQL Query Resolver Results] | Zwischenspeichert die Ergebnisse von GraphQL-Abfrageauflösern für Kunden-, CMS-Seiten-, CMS-Block- und Produktmediensammlungsentitäten. Lassen Sie diesen Cache aktiviert, um die Leistung von GraphQL zu verbessern. | `GRAPHQL_QUERY_RESOLVER_RESULT` | `graphql_query_resolver_result` |
| [!UICONTROL Integrations Configuration] | Konfigurationsdatei für die Integration. Bereinigen oder leeren Sie diesen Cache, nachdem Sie Integrationen geändert oder hinzugefügt haben. | `INTEGRATION` | `config_integration` |
| [!UICONTROL Integrations API Configuration] | Kompilierte Integrations-APIs für Store-Integrationen. | `INTEGRATION_API_CONFIG` | `config_integration_api` |
| [!UICONTROL Admin UI SDK Cache] | speichert Anpassungen im Admin-Cache. Siehe [Admin-Konfiguration und -Tests](https://developer.adobe.com/commerce/extensibility/admin-ui-sdk/configuration/) in der _Admin-Benutzeroberfläche - SDK-Handbuch_. | `ADMIN_UI_SDK` | `admin_ui_sdk` |
| [!UICONTROL Page Cache] | Vollständige Seitenzwischenspeicherung. | `FPC` | `full_page` |
| [!UICONTROL Target Rule] | Zielregelindex | `TARGET_RULE` | `target_rule` |
| [!UICONTROL Web Services Configuration] | Zwischenspeichern der Web-API-Struktur. | `WEBSERVICE` | `config_webservice` |
| [!UICONTROL Translations] | Übersetzungsdateien. | `TRANSLATE` | `translate` |

{style="table-layout:auto"}

## Vollständige Seitenzwischenspeicherung

Adobe Commerce und Magento Open Source verwenden die vollständige Seitenzwischenspeicherung auf dem Server, um Kategorie-, Produkt- und CMS-Seiten schnell anzuzeigen. Die vollständige Seitenzwischenspeicherung verbessert die Antwortzeit und reduziert die Last auf dem Server. Ohne Zwischenspeicherung muss jede Seite möglicherweise Codeblöcke ausführen und Informationen aus der Datenbank abrufen. Wenn jedoch die vollständige Seitenzwischenspeicherung aktiviert ist, kann eine vollständig generierte Seite direkt aus dem Cache gelesen werden.

>[!NOTE]
>
>Es wird empfohlen, [Lackcache](https://varnish-cache.org/){:target=„_blank„} nur in einer Produktionsumgebung verwendet werden.

Zwischengespeicherte Inhalte können verwendet werden, um Anfragen ähnlicher Besuchstypen zu verarbeiten. Daher können Seiten, die einem gelegentlichen Besucher angezeigt werden, von denen abweichen, die einem Kunden angezeigt werden. Für das Caching ist jeder Besuch einer von drei Typen:

- `Non-sessioned` - Während eines nicht sitzungsbezogenen Besuchs zeigt der Käufer die Seiten an, interagiert jedoch nicht mit dem Store. Das System speichert den Inhalt jeder betrachteten Seite im Cache und stellt ihn anderen, nicht sessionierten Käufern zur Verfügung.
- `Sessioned` - Während eines Sitzungsbesuchs wird Käufern, die mit dem Geschäft interagieren, eine Sitzungs-ID zugewiesen (z. B. durch Aktivitäten wie den Vergleich von Produkten oder das Hinzufügen von Produkten zum Warenkorb). Zwischengespeicherte Seiten, die während der Sitzung generiert werden, werden nur von diesem Erstkäufer während der Sitzung verwendet.
- `Customer` - Kundensitzungen werden für diejenigen erstellt, die sich bei Ihrem Geschäft und Shop für ein Konto registriert haben, während sie sich bei ihren Konten angemeldet haben. Während der Sitzung können Kunden Sonderangebote, Aktionen und Preise präsentiert werden, die auf ihrer zugewiesenen Kundengruppe basieren.

Technische Informationen finden Sie unter [Konfigurieren und Verwenden von Lack](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cache/varnish/config-varnish.html){:target=„_blank„} und [Redis für die Commerce-Seite und den Standard-Cache verwenden](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cache/redis/redis-pg-cache.html){:target=„_blank„} in der _Konfigurationshandbuch_.

**_So konfigurieren Sie den Vollseiten-Cache:_**

1. Auf der _Admin_ Seitenleiste, zu gehen **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich . **[!UICONTROL Advanced]** und wählen **[!UICONTROL System]**.

1. Expand ![Erweiterungsauswahl](../assets/icon-display-expand.png) Die **[!UICONTROL Full Page Cache]** -Abschnitt.

   ![Erweiterte Konfiguration - vollständiger Seiten-Cache](../configuration-reference/advanced/assets/system-full-page-cache.png){width="600" zoomable="yes"}

1. set **[!UICONTROL Caching Application]** eine der folgenden Möglichkeiten:

   - `Built-in Application`
   - `Varnish Caching`

1. Um die maximale Wartezeit für den Seiten-Cache festzulegen, geben Sie Folgendes ein **[!UICONTROL TTL for public content]**. (Der Standardwert lautet `86400`)

1. So geben Sie die maximale Anzahl von an [Layout-Griffe](https://developer.adobe.com/commerce/frontend-core/guide/layouts/#layout-handles) zur Verarbeitung am [`{BASE-URL}/page_cache/block/esi`](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cache/use-varnish-esi.html) HTTP-Endpunkt eingeben **[!UICONTROL Handles param size]**. Eine Größenbeschränkung kann die Sicherheit und Leistung verbessern. (Der Standardwert lautet `100`)

1. Wenn Sie „Lack“ verwenden, vervollständigen Sie **[!UICONTROL Varnish Configuration]** -Abschnitt wie folgt:

   - **[!UICONTROL Access list]** : Geben Sie die IP-Adressen ein, die die Lackkonfiguration bereinigen können, um eine Konfigurationsdatei zu generieren. Trennen Sie mehrere Einträge durch ein Komma. Der Standardwert lautet `localhost`.

   - **[!UICONTROL Backend host]** : Geben Sie die IP-Adresse des Backend-Hosts ein, der Konfigurationsdateien generiert. Der Standardwert lautet `localhost`.

   - **[!UICONTROL Backend port]** - Identifizieren Sie den Backend-Port, der zum Generieren von Konfigurationsdateien verwendet wird. Der Standardwert lautet: `8080`.

   - **[!UICONTROL Grace period]** : Geben Sie die Anzahl der Sekunden an, die als Übergangsphase zum Generieren von Konfigurationsdateien verwendet werden sollen. Siehe [Erweiterte Lackkonfiguration](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cache/config-varnish-advanced.html) in der _Konfigurationshandbuch_.

   - So exportieren Sie die Konfiguration als `varnish.vcl` auf die Schaltfläche für die Version von Varnish klicken, die Sie verwenden.

   ![Erweiterte Konfiguration - Lackierung des vollständigen Seiten-Cache](../configuration-reference/advanced/assets/system-full-page-cache-varnish.png){width="600" zoomable="yes"}

1. Klicken Sie abschließend auf **[!UICONTROL Save Config]**.
