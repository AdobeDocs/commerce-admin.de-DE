---
title: Katalog- und Produkt-URLs
description: Erfahren Sie mehr über die URL-Formattypen für Ihre Katalogprodukte und deren Konfiguration.
exl-id: 47405dc6-9b5e-4ca8-87eb-5a222de40793
feature: Catalog Management, Products, Search, Categories
source-git-commit: 11d78b7d7b548c373cfe0ec398814994c3e99e7a
workflow-type: tm+mt
source-wordcount: '882'
ht-degree: 0%

---

# Katalog- und Produkt-URLs

Die URLs, die Sie Produkten und Kategorien zuweisen, spielen eine wichtige Rolle bei der Bestimmung, wie gut Ihre Site von Suchmaschinen indiziert wird. Bevor Sie mit der Erstellung Ihres Katalogs beginnen, sollten Sie die verfügbaren Optionen beachten. Um das aktuelle URL-Format anzuzeigen, gehen Sie zur Storefront und navigieren Sie zu einem beliebigen Produkt in Ihrem Katalog. Das Format der URL hängt von den aktuellen Konfigurationseinstellungen und -methoden ab, die Sie zum Suchen der Seite verwenden.

## URL-Formate

### Dynamische URL

Eine dynamische URL wird _spontan erstellt_ und kann eine Abfragezeichenfolge mit Variablen für die Produkt-ID, die Sortierreihenfolge und die Seite enthalten, auf der die Anforderung erfolgte. Wenn ein Kunde in Ihrem Store nach einem Produkt sucht, sieht die resultierende URL in etwa so aus:

- `http://mystore.com/catalogsearch/result/?q=racer+back`
- `http://mystore.com/women/tops-women.html?style_general=135`

### Statische URL

Eine statische URL ist eine feste Adresse für eine bestimmte Seite. Eine statische URL kann in einem für die Suchmaschine benutzerfreundlichen Format oder in einem Format angezeigt werden, in dem Produkte und Kategorien nach Kennung referenziert werden. Diese URLs enthalten Wörter, mit denen Personen nach einem Produkt suchen können, und erfordern die Aktivierung von Webserver-Neuschreibungen. Dateien mit statischen URLs werden häufig für Produkt- und Kategorieseiten, Inhaltsseiten und [Design-Assets](../content-design/theme-assets.md) verwendet.

- `http://mystore.com/antonia-racer-tank.html`

## URL-Komponenten

### URL-Schlüssel

Der URL-Schlüssel ist Teil einer statischen URL, die das Produkt oder die Kategorie beschreibt. Wenn Sie ein Produkt oder eine Kategorie erstellen, wird basierend auf dem Namen automatisch ein anfänglicher URL-Schlüssel generiert. Informationen zum Ändern des URL-Schlüssels finden Sie im Abschnitt [Suchmaschinenoptimierung](product-search-engine-optimization.md) der Produktinformationen.

>[!NOTE]
>
>Standardmäßig werden Sonderzeichen mit Akzentzeichen automatisch durch ihre regulären, nicht akzentrierten Versionen im URL-Schlüssel ersetzt. Beispielsweise wird `ñ` automatisch durch `n` ersetzt. Dieses Verhalten kann deaktiviert werden, indem die Konfigurationsoption _[!UICONTROL Search Engine Optimization: Apply transliteration for product URL]_auf `No` gesetzt wird. Siehe [Konfigurieren von Katalog-URLs](#configure-catalog-urls).

Der URL-Schlüssel sollte aus Kleinbuchstaben mit nicht nachgestellten Bindestrichen zwischen diesen Zeichen bestehen, um Wörter zu trennen. Bindestriche sind am Anfang oder am Ende des URL-Schlüssels nicht zulässig. Ein gut gestalteter, &quot;suchmaschinenfreundlicher&quot;URL-Schlüssel kann den Produktnamen und Schlüsselwörter enthalten, um die Indexierung durch Suchmaschinen zu verbessern. Der URL-Schlüssel kann so konfiguriert werden, dass eine automatische Umleitung erstellt wird, wenn sich der URL-Schlüssel ändert.

>[!NOTE]
>
>Weitere Informationen zum Erweitern von URL-Anpassungen, z. B. lokalisierten URLs, finden Sie unter [URL-Neuschreibungen](../merchandising-promotions/url-rewrite.md) .

### HTML-Suffix

Ihr Katalog kann so konfiguriert werden, dass das Suffix als Teil der Kategorie- und Produkt-URLs entweder einbezogen oder ausgeschlossen wird. Es gibt verschiedene Gründe, warum Personen das Suffix verwenden oder weglassen möchten. Einige glauben, dass das Suffix keinen nützlichen Zweck mehr erfüllt und dass Seiten ohne Suffix von Suchmaschinen effektiver indiziert werden. Ihr Unternehmen verfügt jedoch möglicherweise über ein standardisiertes Format für URLs, für die ein Suffix erforderlich ist.

Da das Suffix von der Systemkonfiguration gesteuert wird, sollten Sie es nie direkt in den URL-Schlüssel einer Kategorie oder eines Produkts eingeben. (Dies führt zum Doppelsuffix am Ende der URL.) Unabhängig davon, ob Sie das Suffix verwenden möchten oder nicht, sollten Sie konsistent sein und dieselbe Einstellung für alle Produkt- und Kategorieseiten verwenden. Im Folgenden finden Sie Beispiele für URLs mit - und ohne - einem Suffix.

#### URL mit HTML-Suffix

- `http://mystore.com/helena-hooded-fleece.html`
- `http://mystore.com/helena-hooded-fleece.htm`

#### URL ohne HTML-Suffix

- `http://mystore.com/helena-hooded-fleece`

### Kategoriepfad

Sie können die URL so konfigurieren, dass der Kategoriepfad entweder ein- oder ausgeschlossen wird. Standardmäßig ist der Kategoriepfad auf allen Kategorie- und Produktseiten enthalten. Die folgenden Beispiele zeigen dieselbe Produkt-URL mit und ohne Kategoriepfad.

#### URL mit Kategoriepfad

- `http://mystore.com/women/tops-women/hoodies-and-sweatshirts-women/helena-hooded-fleece.html`

#### URL ohne Kategoriepfad

- `http://mystore.com/helena-hooded-fleece.html`

Um zu verhindern, dass Suchmaschinen mehrere URLs indizieren, die zu demselben Inhalt führen, können Sie den Kategoriepfad aus der URL ausschließen. Eine andere Methode besteht darin, ein kanonisches Meta-Tag zu verwenden, um Suchmaschinen mitzuteilen, welche URLs indiziert und welche ignoriert werden sollen. Standardmäßig enthält Commerce den Kategoriepfad nicht in Produkt-URLs.

## Konfigurieren von Katalog-URLs

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bedienfeld den Wert **[!UICONTROL Catalog]** und wählen Sie unter &quot;**[!UICONTROL Catalog]**&quot;.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Search Engine Optimizations]** und legen Sie die Optionen fest:

   - Setzen Sie **[!UICONTROL Product URL Suffix]** auf `html` oder `htm`. Geben Sie das Suffix ohne Punkt ein, da es automatisch angewendet wird.

   - Setzen Sie **[!UICONTROL Category URL Suffix]** auf `html` oder `htm`. Geben Sie das Suffix ohne Punkt ein, da es automatisch angewendet wird.

   - Legen Sie **[!UICONTROL Use Categories Path for Product URLs]** auf Ihre Voreinstellung fest.

   ![Suchmaschinenoptimierung](../configuration-reference/catalog/assets/catalog-search-engine-optimization.png){width="600" zoomable="yes"}

   Eine detaillierte Liste dieser Optionen finden Sie unter [Suchmaschinenoptimierung](../configuration-reference/catalog/catalog.md#search-engine-optimization) in der _Konfigurationsreferenz_.

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save Config]**.

1. Wenn Sie dazu aufgefordert werden, klicken Sie in der Systemmeldung auf den Link **[!UICONTROL Cache Management]** und aktualisieren Sie den ungültigen Cache.

   ![Cache aktualisieren](./assets/msg-cache-management.png){width="450" zoomable="yes"}

   Weitere Informationen zu diesen Optionen finden Sie unter [Aktualisieren von Caches](../systems/cache-management.md#refresh-specific-caches).

## URL-Format für Katalogmedien konfigurieren

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich den Wert **[!UICONTROL General]** und wählen Sie **[!UICONTROL Web]** aus.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Url Options]** und legen Sie die Optionen fest:

![Web > Allgemeine Optionen](../configuration-reference/general/assets/web-url-options.png){width="600" zoomable="yes"}

| Feld | [Umfang](../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Add Store Code to URLs] | Global | Wenn Webserver-Neuschreibungen aktiviert sind, wird durch Aktivieren dieser Einstellung der Store-Code der aktuellen Ansicht in die URL eingefügt. Optionen: `Yes` / `No` |
| [!UICONTROL Auto-redirect to Base URL] | Global | (Bei Einzelspeicher-Setups) Wenn auf Ihrer Site ein defekter Link vorhanden ist, leitet dieser Traffic zur Basis-URL und nicht zu einer Seite mit der Meldung &quot;404 Seite nicht gefunden&quot;weiter. Optionen: `No` / `Yes (302 Found)` / `Yes (301 Moved Permanently)` <br /><br />**_Wichtig!_**Verwenden Sie keine automatische Umleitung zur Basis-URL für Multi-Store-Setups. |
| [!UICONTROL Catalog media URL format] | Global | Definiert das URL-Format, das Produkten und Kategorien zugewiesen ist. Optionen: <br />**[!UICONTROL Unique hash per image variant (Legacy mode)]**- Definiert den konvertierten Dateinamen als eindeutigen Hash-Wert.<br />**[!UICONTROL Image optimization based on query parameters]** - Definiert den Prozess zur [Bildoptimierung](../content-design/media-gallery-image-optimization.md) je nach Abfrageparametern. |

{style="table-layout:auto"}
