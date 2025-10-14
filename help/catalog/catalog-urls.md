---
title: Katalog- und Produkt-URLs
description: Erfahren Sie mehr über die URL-Formattypen für Ihre Katalogprodukte und deren Konfiguration.
exl-id: 47405dc6-9b5e-4ca8-87eb-5a222de40793
feature: Catalog Management, Products, Search, Categories
source-git-commit: 1edab49fd8d52a1b7414eb207a21c5c03200e75e
workflow-type: tm+mt
source-wordcount: '909'
ht-degree: 0%

---

# Katalog- und Produkt-URLs

Die URLs, die Sie Produkten und Kategorien zuweisen, spielen eine wichtige Rolle bei der Bestimmung, wie gut Ihre Site von Suchmaschinen indiziert wird. Bevor Sie mit der Erstellung Ihres Katalogs beginnen, ziehen Sie die verfügbaren Optionen in Betracht. Um das aktuelle URL-Format anzuzeigen, gehen Sie zur Storefront und navigieren Sie zu einem beliebigen Produkt in Ihrem Katalog. Das Format der URL hängt von den aktuellen Konfigurationseinstellungen und der Methode ab, die Sie zum Suchen der Seite verwenden.

## URL-Formate

### Dynamische URL

Eine dynamische URL wird _laufender Zeit erstellt_ kann eine Abfragezeichenfolge mit Variablen für die Produkt-ID, die Sortierreihenfolge und die Seite, auf der die Anfrage erfolgt ist, enthalten. Wenn ein Kunde in Ihrem Geschäft nach einem Produkt sucht, könnte die resultierende URL wie folgt aussehen:

- `http://mystore.com/catalogsearch/result/?q=racer+back`
- `http://mystore.com/women/tops-women.html?style_general=135`

### Statische URL

Eine statische URL ist eine feste Adresse für eine bestimmte Seite. Eine statische URL kann in einem suchmaschinenfreundlichen Format angezeigt werden oder in einem Format, das Produkte und Kategorien nach ID referenziert. Diese URLs enthalten Wörter, mit denen Benutzer nach einem Produkt suchen können, und für die Webserver-Neuschreibungen aktiviert sein müssen. Dateien mit statischen URLs werden häufig für Produkt- und Kategorieseiten, Inhaltsseiten und (Design[Assets) &#x200B;](../content-design/theme-assets.md).

- `http://mystore.com/antonia-racer-tank.html`

## URL-Komponenten

### URL-Schlüssel

Der URL-Schlüssel ist der Teil einer statischen URL, die das Produkt oder die Kategorie beschreibt. Wenn Sie ein Produkt oder eine Kategorie erstellen, wird automatisch ein erster URL-Schlüssel basierend auf dem Namen generiert. Informationen zum Ändern des URL-Schlüssels finden [&#x200B; im Abschnitt &#x200B;](product-search-engine-optimization.md)Suchmaschinenoptimierung“ der Produktinformationen.

>[!NOTE]
>
>Standardmäßig werden Sonderzeichen mit Akzenten im URL-Schlüssel automatisch durch ihre regulären Versionen ohne Akzent ersetzt. Beispielsweise wird `ñ` automatisch durch `n` ersetzt. Dieses Verhalten kann deaktiviert werden, indem die _[!UICONTROL Search Engine Optimization: Apply transliteration for product URL]_-Konfigurationsoption auf `No` gesetzt wird. Siehe [Konfigurieren von Katalog-URLs](#configure-catalog-urls).

Der URL-Schlüssel sollte aus Kleinbuchstaben mit nicht nachfolgenden Bindestrichen zwischen diesen Zeichen bestehen, um Wörter zu trennen. Bindestriche sind am Beginn oder am Ende des URL-Schlüssels nicht zulässig. Ein gut gestalteter, „suchmaschinenfreundlicher“ URL-Schlüssel kann den Produktnamen und die Schlüsselwörter enthalten, um die Indizierung durch Suchmaschinen zu verbessern. Der URL-Schlüssel kann so konfiguriert werden, dass eine automatische Umleitung erstellt wird, wenn sich der URL-Schlüssel ändert.

>[!NOTE]
>
>Informationen zum Erweitern von URL-Anpassungen, wie z. B. lokalisierte URLs, finden Sie unter [URL](../merchandising-promotions/url-rewrite.md)Neuschreibungen).

### HTML-Suffix

Ihr Katalog kann so konfiguriert werden, dass das -Suffix als Teil der Kategorie- und Produkt-URLs entweder ein- oder ausgeschlossen wird. Es gibt verschiedene Gründe, warum Benutzer das Suffix verwenden oder weglassen. Einige glauben, dass das Suffix keinen nützlichen Zweck mehr erfüllt und dass Seiten ohne Suffix von Suchmaschinen effektiver indiziert werden. Ihr Unternehmen könnte jedoch über ein standardisiertes Format für URLs verfügen, für das ein Suffix erforderlich ist.

Da das Suffix von der Systemkonfiguration gesteuert wird, sollten Sie es niemals direkt in den URL-Schlüssel einer Kategorie oder eines Produkts eingeben. (Dies führt zu einem doppelten Suffix am Ende der URL.) Unabhängig davon, ob Sie das -Suffix verwenden oder nicht, sollten Sie konsistent sein und dieselbe Einstellung für alle Ihre Produkt- und Kategorieseiten verwenden. Im Folgenden finden Sie Beispiele für URLs mit - und ohne - einem Suffix.

#### URL mit HTML-Suffix

- `http://mystore.com/helena-hooded-fleece.html`
- `http://mystore.com/helena-hooded-fleece.htm`

#### URL ohne HTML-Suffix

- `http://mystore.com/helena-hooded-fleece`

### Kategoriepfad

Sie können die Produkt-URLs so konfigurieren, dass der Kategoriepfad je nach Ihren Voreinstellungen ein- oder ausgeschlossen wird. Standardmäßig ist der Kategoriepfad nicht in Produkt-URLs enthalten. Verschachtelte Kategorien zeigen jedoch immer den vollständigen Kategoriepfad in ihren URLs auf der Storefront an, um Klarheit und Konsistenz in der Kategoriennavigation zu gewährleisten. Die folgenden Beispiele zeigen dieselbe Produkt-URL mit und ohne Kategoriepfad.

#### Produkt-URL mit Kategoriepfad

- `http://mystore.com/women/tops-women/hoodies-and-sweatshirts-women/helena-hooded-fleece.html`

#### Produkt-URL ohne Kategoriepfad

- `http://mystore.com/helena-hooded-fleece.html`

Um zu verhindern, dass Suchmaschinen mehrere URLs indizieren, die zum selben Inhalt führen, können Sie den Kategoriepfad aus der URL ausschließen. Eine andere Methode besteht darin, ein kanonisches Meta-Tag zu verwenden, um Suchmaschinen mitzuteilen, welche URLs indiziert und welche ignoriert werden sollen. Standardmäßig enthält Commerce den Kategoriepfad nicht in Produkt-URLs.

## Konfigurieren von Katalog-URLs

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Catalog]** und wählen Sie darunter **[!UICONTROL Catalog]**.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Search Engine Optimizations]** und legen Sie die Optionen fest:

   - **[!UICONTROL Product URL Suffix]** auf `html` oder `htm` festlegen. Geben Sie das Suffix ohne Punkt ein, da es automatisch angewendet wird.

   - **[!UICONTROL Category URL Suffix]** auf `html` oder `htm` festlegen. Geben Sie das Suffix ohne Punkt ein, da es automatisch angewendet wird.

   - Legen Sie **[!UICONTROL Use Categories Path for Product URLs]** auf Ihre Voreinstellung fest.

   ![Suchmaschinenoptimierung](../configuration-reference/catalog/assets/catalog-search-engine-optimization.png){width="600" zoomable="yes"}

   Eine detaillierte Liste dieser Optionen finden Sie unter [Suchmaschinenoptimierung](../configuration-reference/catalog/catalog.md#search-engine-optimization) in der _Konfigurationsreferenz_.

1. Klicken Sie abschließend auf **[!UICONTROL Save Config]**.

1. Wenn Sie dazu aufgefordert werden, klicken Sie auf den Link **[!UICONTROL Cache Management]** in der Systemmeldung und aktualisieren Sie den ungültigen Cache.

   ![Cache aktualisieren](./assets/msg-cache-management.png){width="450" zoomable="yes"}

   Weitere Informationen zu diesen Optionen finden Sie unter [Caches aktualisieren](../systems/cache-management.md#refresh-specific-caches).

## Konfigurieren des URL-Formats für Katalogmedien

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL General]** und wählen Sie **[!UICONTROL Web]**.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Url Options]** und legen Sie die Optionen fest:

![Web > Allgemeine Optionen](../configuration-reference/general/assets/web-url-options.png){width="600" zoomable="yes"}

| Feld | [Umfang](../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Add Store Code to URLs] | Global | Wenn Webserver-Neuschreibungen aktiviert sind, wird durch Aktivieren dieser Einstellung der Store-Code der aktuellen Ansicht in die URL eingefügt. Optionen: `Yes` / `No` |
| [!UICONTROL Auto-redirect to Base URL] | Global | (Bei Einzelspeicher-Setups) Wenn auf Ihrer Site ein fehlerhafter Link vorhanden ist, wird der Traffic an die Basis-URL und nicht an eine Seite mit der Meldung „404 Seite nicht gefunden“ umgeleitet. Optionen: `No` / `Yes (302 Found)` / `Yes (301 Moved Permanently)` <br /><br />**_wichtig!_**&#x200B;Verwenden Sie keine automatische Umleitung zur Basis-URL für Multi-Store-Setups. |
| [!UICONTROL Catalog media URL format] | Global | Definiert das URL-Format, das Produkten und Kategorien zugewiesen ist. Optionen: <br />**[!UICONTROL Unique hash per image variant (Legacy mode)]**- Definiert den konvertierten Dateinamen als eindeutigen Hash-Wert.<br />**[!UICONTROL Image optimization based on query parameters]** - Definiert [Bildoptimierungsprozess](../content-design/media-gallery-image-optimization.md) abhängig von Abfrageparametern. |

{style="table-layout:auto"}
