---
title: Cacheverwaltung
description: Erfahren Sie, wie Sie die Cache-Verwaltungstools verwenden, die eine einfache Möglichkeit bieten, die Leistung Ihrer Site zu verbessern.
exl-id: c87f85ca-81b9-4cbf-9817-3d779397eefd
feature: Cache, System
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '1422'
ht-degree: 0%

---

# Cacheverwaltung

Das Cache-Verwaltungssystem von Adobe Commerce und Magento Open Source bietet eine einfache Möglichkeit, die Leistung Ihrer Site zu verbessern. Wenn ein Cache eine Aktualisierung erfordert, wird oben im Arbeitsbereich ein Hinweis angezeigt, der Sie durch den Prozess führt. Folgen Sie dem Link zum Verwalten des Cache und aktualisieren Sie die ungültigen Caches.

![Produktattribut speichern - Cache-Meldung aktualisieren](./assets/product-attribute-save-msg-update-cache.png){width="500"}

>[!NOTE]
>
>Wenn Katalogentitäten geändert werden, kann sich dies auf andere Seiten auswirken und mehrere Caches gleichzeitig ungültig machen. Wenn Sie die Seite zur Cache-Verwaltung überprüfen, werden möglicherweise ungültige Elemente angezeigt, die aktualisiert werden müssen, wenn sie _**nicht direkt bearbeitet**_. Diese Invalidierung tritt beispielsweise dann auf, wenn Sie ein Produkt im Katalog bearbeiten und es einer beliebigen Kategorie zugewiesen wird oder wenn Sie eine verwandte Produktregel ändern.

Die _[!UICONTROL Cache Management]_-Seite zeigt den Status jedes primären Caches und des zugehörigen Tags an. Die großen Schaltflächen in der oberen rechten Ecke können verwendet werden, um den Cache oder den All-Include-Cache-Speicher zu leeren. Am unteren Rand der Seite befinden sich zusätzliche Schaltflächen, um den Cache für Katalogproduktbilder und den JavaScript-/CSS-Cache zu leeren.

Nachdem Sie einen Cache gelöscht haben, aktualisieren Sie Ihren Browser immer, um sicherzustellen, dass Sie die neuesten Dateien sehen können. Beim Löschen des Commerce-Cache wird der Cache des Webbrowsers nicht gelöscht. Möglicherweise müssen Sie den Browser-Cache löschen, um aktualisierte Inhalte anzuzeigen.

Weitere technische Informationen finden Sie unter [Cache-Übersicht](https://developer.adobe.com/commerce/frontend-core/guide/caching/){:target=&quot;_blank&quot;} im _Entwicklungshandbuch für Commerce Frontend_.

Zugriff auf _[!UICONTROL Cache Management]_Seite durch einen der folgenden Schritte:

- Klicken Sie auf **[!UICONTROL Cache Management]** in der Meldung über dem Arbeitsbereich.
- Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL System]** > _[!UICONTROL Tools]_>**[!UICONTROL Cache Management]**.

![Cacheverwaltung](./assets/cache-management-invalid.png){width="700" zoomable="yes"}

## Best Practices für die Zwischenspeicherung

Die Neuindizierung und Zwischenspeicherung dienen in Commerce unterschiedlichen Zwecken. [Indizes](index-management.md) Nachverfolgen von Datenbankinformationen für eine verbesserte Suchleistung, einen schnelleren Datenabruf für Storefronts und mehr. Caches speichern geladene Daten, Bilder, Formate und Ähnliches für eine verbesserte Leistung beim Laden und Aufrufen der Storefront.

- Leeren Sie den Cache immer, nachdem Sie Erweiterungen/Module installiert haben. Sie können eine oder mehrere Erweiterungen installieren und dann den Cache leeren.
- Leeren Sie den Cache nach der Installation von Commerce. Bei Neuinstallationen sollten Sie auch neu indizieren.
- Leeren Sie den Cache, nachdem Sie von einer Open Source- oder Commerce-Version auf eine andere aktualisiert haben.
- Berücksichtigen Sie beim Leeren von Caches den Cache-Typ und planen Sie die Leerung während Nicht-Spitzenzeiten. Wählen Sie beispielsweise eine Zeit aus, zu der wenige Kunden auf die Site zugreifen können, wie z. B. späte Nacht oder frühe Morgen. Das Löschen einiger Cache-Typen während Spitzenzeiten führt zu einer hohen Belastung des Administrators und kann zu einem Herunterfahren der Site führen, bis diese abgeschlossen ist.
- Wann [Neuindizierung](index-management.md), müssen Sie nicht auch einen leeren Cache ausführen.

## Rollenressourcen für die Cacheverwaltung

Der Zugriff auf bestimmte Cache-Wartungsaktionen kann Benutzern nach Rolle zugewiesen werden, einschließlich Optionen zum Anzeigen, Umschalten und Leeren von Caches. Adobe empfiehlt die Aktivierung von Flush-Aktionen nur für Benutzer auf Administratorebene. Die Bereitstellung des Zugriffs auf alle Cache-Management-Funktionen kann die Leistung Ihrer Storefront beeinträchtigen.

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

## Aktualisieren bestimmter Caches

1. Aktivieren Sie für jeden Cache, der aktualisiert werden soll, das Kontrollkästchen am Anfang der Zeile.

1. Satz **[!UICONTROL Actions]** nach `Refresh` und klicken **[!UICONTROL Submit]**.

## Aktualisierung der Massenaktion durchführen

1. Um eine Gruppe von Caches auszuwählen, legen Sie **[!UICONTROL Mass Actions]** auf einen der folgenden Werte zu:

   - `Select All`
   - `Select Visible`

1. Aktivieren Sie das Kontrollkästchen jedes Caches, auf den die Aktion abzielen soll.

1. Satz **[!UICONTROL Actions]** nach `Refresh` und klicken **[!UICONTROL Submit]**.

## Leeren Sie den Cache des Produktbilds.

1. under _[!UICONTROL Additional Cache Management]_klicken **[!UICONTROL Flush Catalog Images Cache]**, um vorgenerierte Produktbilddateien zu löschen.

   Die `Image cache was cleaned` wird oben im Arbeitsbereich angezeigt.

1. Löschen Sie den Cache Ihres Browsers.

## JavaScript-/CSS-Cache leeren

1. under _[!UICONTROL Additional Cache Management]_klicken **[!UICONTROL Flush JavaScript/CSS Cache]**um alle JavaScript- und CSS-Dateien zu löschen, die in einer Datei zusammengeführt wurden.

   Die `The JavaScript/CSS cache has been cleaned` wird oben im Arbeitsbereich angezeigt.

1. Löschen Sie den Cache Ihres Browsers.

## Leeren mithilfe der Befehlszeile

Commerce bietet über die Befehlszeile zusätzliche Optionen für den Leerungs-Cache. Für diese Optionen ist möglicherweise der Entwicklersupport erforderlich. Ausführliche Informationen und Befehlsoptionen finden Sie unter [Verwalten des Cache](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/manage-cache.html){:target=&quot;_blank&quot;} im _Konfigurationshandbuch_.

## Steuerelemente

| Kontrolle | Beschreibung |
|--- |--- |
| [!UICONTROL Mass Actions] | Aktiviert das Kontrollkästchen mehrerer Caches. Optionen: <br/>**[!UICONTROL Select All]**— Wählt das Kontrollkästchen aller Caches aus.<br/>** Auswahl aufheben **— Löscht das Kontrollkästchen aller Caches.<br/>**[!UICONTROL Select Visible]** — Wählt das Kontrollkästchen aller sichtbaren Caches aus. <br/>**[!UICONTROL Unselect Visible]**— Löscht das Kontrollkästchen aller sichtbaren Caches. |
| [!UICONTROL Actions] | Bestimmt die Aktion, die auf alle ausgewählten Caches angewendet werden soll. Optionen: <br/>**[!UICONTROL Enable]**— Aktiviert alle ausgewählten Caches.<br/>**[!UICONTROL Disable]** — Deaktiviert alle ausgewählten Caches. <br/>**[!UICONTROL Refresh]**- Aktualisiert alle ausgewählten Caches. |
| [!UICONTROL Submit] | Wendet die Aktion auf alle ausgewählten Caches an. |

{style="table-layout:auto"}

### Schaltflächen

| Schaltfläche | Beschreibung |
|--- |--- |
| [!UICONTROL Flush Magento Cache] | Entfernt alle Elemente im standardmäßigen Commerce-Cache (`var/cache`), entsprechend den zugehörigen Commerce-Tags. |
| [!UICONTROL Flush Cache Storage] | Entfernt alle Elemente aus dem Cache, unabhängig vom Commerce-Tag. Wenn Ihr System einen alternativen Cache-Speicherort verwendet, werden alle zwischengespeicherten Dateien, die von anderen Anwendungen verwendet werden, im Prozess entfernt. |
| [!UICONTROL Flush Catalog Images Cache] | Entfernt alle automatisch in der Größe angepassten und mit Wasserzeichen versehenen Katalogbilder, die in `media/catalog/product/cache`. Wenn kürzlich hochgeladene Bilder nicht im Katalog angezeigt werden, versuchen Sie, den Katalog zu leeren und den Browser zu aktualisieren. |
| [!UICONTROL Flush JavaScript/CSS Cache] | Entfernt die zusammengeführte Kopie von JavaScript- und CSS-Dateien aus dem Cache. Wenn aktuelle Änderungen am Stylesheet oder JavaScript im Store nicht berücksichtigt werden, versuchen Sie, den JavaScript-/CSS-Cache zu leeren und den Browser zu aktualisieren. |
| [!UICONTROL Flush Static Files Cache] | Entfernt vorverarbeitete Ansichtsdateien und statische Dateien. |

{style="table-layout:auto"}

### Caches

| Cache | Beschreibung | Zugeordnetes Tag |
| ----- | ----------- | -------------- |
| [!UICONTROL Configuration] | Verschiedene XML-Konfigurationen, die über Module hinweg erfasst und zusammengeführt wurden.<br>**[!UICONTROL System]**-  `config.xml`,`local.xml`<br>**[!UICONTROL Module]** -  `config.xml` | `CONFIG` |
| [!UICONTROL Layouts] | Anweisungen zum Erstellen von Layouts. | `LAYOUT_GENERAL_CACHE_TAG` |
| [!UICONTROL Blocks HTML output] | Seitenblöcke - HTML. | `BLOCK_HTML` |
| [!UICONTROL Collections Data] | Sammlungsdatendateien. | `COLLECTION_DATA` |
| [!UICONTROL Reflection Data] | Löscht die normalerweise während der Laufzeit generierten Reflexionsdaten der API-Oberfläche. | `REFLECTION` |
| [!UICONTROL Database DDL operations] | Ergebnisse von DDL-Abfragen, beispielsweise die Beschreibung von Tabellen oder Indizes. | `DB_DDL` |
| [!UICONTROL Compiled Config] | Ergebnisse der Codekompilierung. | `COMPILED_CONFIG` |
| [!UICONTROL EAV types and attributes] | Deklarierungs-Cache für Entitätstypen. | `EAV` |
| [!UICONTROL Customer Notification] | Vorübergehende Benachrichtigungen, die in der Benutzeroberfläche angezeigt werden. | `CUSTOMER_NOTIFICATION` |
| [!UICONTROL Integrations Configuration] | Integrationskonfigurationsdatei. | `INTEGRATION` |
| [!UICONTROL Integrations API Configuration] | Integrations-API-Konfigurationsdatei. | `INTEGRATION_API_CONFIG` |
| [!UICONTROL Page Cache] | Zwischenspeicherung auf der vollständigen Seite. | `FPC` |
| [!UICONTROL Translations] | Übersetzungsdateien. | `TRANSLATE` |
| [!UICONTROL Web Services Configuration] | REST- und SOAP-Konfigurationen, generierte WSDL-Datei. | `WEBSERVICE` |
| [!UICONTROL Target Rule] | Target-Regelindex | `TARGET_RULE` |

{style="table-layout:auto"}

## Vollseitenzwischenspeicherung

Adobe Commerce und Magento Open Source verwenden das vollständige Caching auf dem Server, um schnell Kategorie-, Produkt- und CMS-Seiten anzuzeigen. Die Zwischenspeicherung über die vollständige Seite verbessert die Antwortzeit und verringert die Auslastung des Servers. Ohne Zwischenspeicherung muss jede Seite möglicherweise Codeblöcke ausführen und Informationen aus der Datenbank abrufen. Bei aktiviertem ganzseitigen Caching kann eine vollständig generierte Seite jedoch direkt aus dem Cache gelesen werden.

>[!NOTE]
>
>Es wird empfohlen, [Varnish Cache](https://varnish-cache.org/){:target=&quot;_blank&quot;} darf nur in einer Produktionsumgebung verwendet werden.

Zwischengespeicherte Inhalte können zur Verarbeitung der Anforderungen von ähnlichen Besuchstypen verwendet werden. Daher können Seiten, die einem Gelegenheitsbesucher angezeigt werden, von denen abweichen, die einem Kunden angezeigt werden. Für die Zwischenspeicherung ist jeder Besuch einer von drei Typen:

- `Non-sessioned` - Während eines nicht sitzungsbezogenen Besuchs zeigt der Käufer Seiten an, interagiert jedoch nicht mit dem Store. Das System speichert den Inhalt jeder angezeigten Seite zwischen und stellt ihn anderen Benutzern ohne Sitzung zur Verfügung.
- `Sessioned` - Während eines Sitzungsbesuchs wird Käufern, die mit dem Geschäft interagieren, eine Sitzungs-ID zugewiesen, beispielsweise durch den Vergleich von Produkten oder das Hinzufügen von Produkten zum Warenkorb. Zwischengespeicherte Seiten, die während der Sitzung generiert werden, werden nur von diesem Käufer während der Sitzung verwendet.
- `Customer` - Kundensitzungen werden für diejenigen erstellt, die sich für ein Konto bei Ihrem Geschäft registriert und bei ihrem Konto angemeldet haben. Während der Sitzung können Kunden spezielle Angebote, Promotions und Preise unterbreitet werden, die auf ihrer zugewiesenen Kundengruppe basieren.

Technische Informationen finden Sie unter [Konfigurieren und Verwenden von Varnish](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cache/varnish/config-varnish.html){:target=&quot;_blank&quot;} und [Verwenden von Redis für die Seite &quot;Commerce&quot;und den Standardcache](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cache/redis/redis-pg-cache.html){:target=&quot;_blank&quot;} im _Konfigurationshandbuch_.

**_So konfigurieren Sie den ganzseitigen Cache:_**

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Advanced]** und wählen **[!UICONTROL System]**.

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL Full Page Cache]** Abschnitt.

   ![Erweiterte Konfiguration - Vollseitencache](../configuration-reference/advanced/assets/system-full-page-cache.png){width="600" zoomable="yes"}

1. Satz **[!UICONTROL Caching Application]** auf einen der folgenden Werte zu:

   - `Built-in Application`
   - `Varnish Caching`

1. Um den Timeout für den Seiten-Cache festzulegen, geben Sie die **[!UICONTROL TTL for public content]**. (Der Standardwert ist `86400`)

1. Bei Verwendung von Varnish müssen Sie die **[!UICONTROL Varnish Configuration]** wie folgt:

   - **[!UICONTROL Access list]** - Geben Sie die IP-Adressen ein, die die Varnish-Konfiguration bereinigen können, um eine Konfigurationsdatei zu generieren. Trennen Sie mehrere Einträge durch ein Komma. Der Standardwert ist `localhost`.

   - **[!UICONTROL Backend host]** - Geben Sie die IP-Adresse des Backend-Hosts ein, der Konfigurationsdateien generiert. Der Standardwert ist `localhost`.

   - **[!UICONTROL Backend port]** - Identifizieren Sie den Backend-Port, der zum Generieren von Konfigurationsdateien verwendet wird. Der Standardwert ist: `8080`.

   - **[!UICONTROL Grace period]** - Geben Sie die Anzahl der Sekunden an, die als Übergangsphase zum Generieren von Konfigurationsdateien verwendet werden sollen. Siehe [Erweiterte Varnish-Konfiguration](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cache/config-varnish-advanced.html) im _Konfigurationshandbuch_.

   - So exportieren Sie die Konfiguration als `varnish.vcl` klicken Sie auf die Schaltfläche für die von Ihnen verwendete Version von Varnish.

   ![Erweiterte Konfiguration - Vollbild-Cache-Lack der Seite](../configuration-reference/advanced/assets/system-full-page-cache-varnish.png){width="600" zoomable="yes"}

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save Config]**.
