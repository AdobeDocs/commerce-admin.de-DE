---
title: '[!UICONTROL General] &gt; [!UICONTROL Web]'
description: Überprüfen Sie die Konfigurationseinstellungen auf der [!UICONTROL General] &gt; [!UICONTROL Web] Seite des Commerce-Administrators.
exl-id: 1809b03a-a55c-41b4-947b-f66f4bd290a1
feature: Site Management, Configuration
source-git-commit: 370131cd73a320b04ee92fa9609cb24ad4c07eca
workflow-type: tm+mt
source-wordcount: '1822'
ht-degree: 0%

---

# [!UICONTROL General] > [!UICONTROL Web]

{{config}}

## [!UICONTROL URL Options]

![Web > Allgemeine Optionen](./assets/web-url-options.png)<!-- zoom -->

<!-- [URL Options configuration settings](https://docs.magento.com/user-guide/stores/store-urls.html) -->

| Feld | Anwendungsbereich | Beschreibung |
|  ---  |  ---  |  ---  |
| [!UICONTROL Add Store Code to URLs] | Global | Wenn Webserver-Neuschreibungen aktiviert sind, fügt den Store-Code der aktuellen Ansicht in die URL ein. Optionen: `Yes` / `No`. <br />Wenn dieses Feld auf `Yes`müssen Sie Store-Codes in Ihre Browser-URLs aufnehmen, um sicherzustellen, dass URL-Neuschreibungen korrekt zugeordnet und alle Seiten erfolgreich geöffnet werden. Dies vermeidet _404 Seite nicht gefunden_ Fehler. |
| [!UICONTROL Auto-redirect to Base URL] | Store-Ansicht | (Bei Einzelspeicher-Setups) Wenn auf Ihrer Site ein defekter Link vorhanden ist, leitet den Traffic zur Basis-URL weiter und nicht zu einer Seite mit der Meldung &quot;404 Seite nicht gefunden&quot;. Optionen:` No` / `Yes (302 Found)` / `Yes (301 Moved Permanently)` <br />**_Wichtig:_**Verwenden Sie keine automatische Umleitung zur Basis-URL für Multi-Store-Setups. |
| [!UICONTROL Catalog media URL format] | Global | Definiert die [URL-Format](../../catalog/catalog-urls.md) den Produkten und Kategorien zugeordnet werden. Optionen: Eindeutiger Hash pro Bildvariante (Legacy-Modus) definiert den konvertierten Dateinamen als einen eindeutigen Hash-Wert. Bildoptimierung basierend auf Abfrageparametern definiert [Bildoptimierung](../../content-design/media-gallery-image-optimization.md) -Prozess abhängig von Abfrageparametern. |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Search Engine Optimization]

![Web > Suchmaschinenoptimierung](./assets/web-search-engine-optimization.png)<!-- zoom -->

<!-- [Search Engine Optimization configuration settings](https://docs.magento.com/user-guide/marketing/url-rewrite.html) -->

| Feld | [Anwendungsbereich](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Use Web Server Rewrites] | Store-Ansicht | PHP-basierte Systeme enthalten normalerweise eine Datei namens `index.php` im Stammordner. Standardmäßig wird der Dateiname in der URL direkt nach dem Namen des Stammordners angezeigt. Wenn diese Option aktiviert ist, werden vom System keine `index.php` von der URL aus. Diese Best Practice für die Benutzerfreundlichkeit macht jede URL präziser und hat keine Auswirkungen auf die Leistung oder den Site-Rang. Optionen: `Yes` / `No` |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Base URLs]

![Web > Basis-URLs](./assets/web-base-urls.png)<!-- zoom -->

<!-- [Base URLS configuration settings](https://docs.magento.com/user-guide/stores/store-urls.html) -->

| Feld | [Anwendungsbereich](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Base URL] | Store-Ansicht | Die vollständige Adresse des Commerce-Stammordners, der nicht über einen verschlüsselten (SSL-)Kanal ausgeführt wird. Die URL muss mit einem Schrägstrich enden. |
| [!UICONTROL Base Link URL] | Store-Ansicht | Ein Markup-Tag, das als Platzhalter für die Basis-URL verwendet wird. |
| [!UICONTROL Base URL for Static View Files] | Store-Ansicht | Ein Pfad, der auf den Speicherort der vom Design verwendeten statischen Dateien verweist, z. B. CSS, Schriftarten, Bilder und JavaScript. Ein Platzhalter wird zur Darstellung der Basis-URL verwendet. Wenn Ihre Commerce-Installation über mehrere Sites mit derselben Ordnerstruktur verfügt, können Sie für jede Site einen anderen Ordner haben. Legen Sie den Konfigurationsbereich auf die richtige Site fest, bevor Sie die Basis-URL für statische Ansichtsdateien eingeben. Sie können auch einen Ordner außerhalb Ihrer Commerce-Installation angeben. |
| [!UICONTROL Base URL for User Media Files] | Store-Ansicht | Ein Pfad, der auf den Speicherort von Katalogbildern und anderen Mediendateien verweist. Ein Platzhalter wird zur Darstellung der Basis-URL verwendet. Wenn Ihre Commerce-Installation über mehrere Sites mit derselben Ordnerstruktur verfügt, können Sie für jeden Ordner einen anderen Medienordner verwenden. Dadurch können Sie jeden Medienordner separat sichern und wiederherstellen. Sie können auch einen Medienordner außerhalb Ihrer Commerce-Installation angeben. |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Base URLs (Secure)]

![Web > Basis-URLs (sicher)](./assets/web-base-urls-secure.png)<!-- zoom -->

<!-- [Base URLs (Secure) configuration settings](https://docs.magento.com/user-guide/stores/store-urls.html) -->

| Feld | [Anwendungsbereich](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Secure Base URL] | Store-Ansicht | Die vollständige Adresse des Commerce-Stammordners, der mit dem verschlüsselten sicheren (SSL/TLS) Protokoll bereitgestellt wird. Die URL muss mit einem Schrägstrich enden. |
| [!UICONTROL Secure Base Link URL] | Store-Ansicht | Ein Markup-Tag, das als Platzhalter für die Basis-URL verwendet wird, die über einen sicheren Kanal ausgeführt wird. |
| [!UICONTROL Secure Base URL for Static View Files] | Store-Ansicht | Ein Markup-Tag, das auf den Speicherort von statischen Dateien wie CSS, Schriftarten, Bilder und JavaScript verweist, die vom Design verwendet werden. Die Dateien können sich auf einem unsicheren oder sicheren Kanal befinden. Wenn Ihre Commerce-Installation über mehrere Sites mit derselben Ordnerstruktur verfügt, können Sie für jede Site einen anderen Ordner haben. Legen Sie den Konfigurationsbereich auf die richtige Site fest, bevor Sie die Basis-URL für statische Ansichtsdateien eingeben. Sie können auch einen Ordner außerhalb Ihrer Commerce-Installation angeben. |
| [!UICONTROL Secure Base URL for User Media Files] | Store-Ansicht | Ein Pfad, der auf den Speicherort von Katalogbildern und anderen Mediendateien verweist. Die Dateien können sich auf einem unsicheren oder sicheren Kanal befinden. Ein Platzhalter wird zur Darstellung der Basis-URL verwendet. Wenn Ihre Commerce-Installation über mehrere Sites mit derselben Ordnerstruktur verfügt, können Sie für jeden Ordner einen anderen Medienordner verwenden. Dadurch können Sie jeden Medienordner separat sichern und wiederherstellen. Sie können auch einen Medienordner außerhalb Ihrer Commerce-Installation angeben. |
| [!UICONTROL Use Secure URLs on Storefront] | Store-Ansicht | Wenn Ihre Domäne über ein Sicherheitszertifikat verfügt, können Sie die Storefront mit oder ohne SSL-Verschlüsselung ausführen. Optionen:<br />**`Yes`**- Store-URLs beginnen mit `https` , um anzugeben, dass die Seite mit einem verschlüsselten, sicheren Protokoll bereitgestellt wird.<br />**`No`** - Store-URLs beginnen mit `http` , um anzugeben, dass die Seite ohne sicheres Protokoll bereitgestellt wird. |
| [!UICONTROL Use Secure URLs in Admin] | Global | Wenn Ihre Domäne über ein Sicherheitszertifikat verfügt, können Sie den Store-Administrator mit oder ohne SSL-Verschlüsselung ausführen. Optionen: <br />**`Yes`**- Admin-URLs beginnen mit `https` , um anzugeben, dass die Seite mit einem verschlüsselten, sicheren Protokoll bereitgestellt wird.<br />**`No`** - Admin-URLs beginnen mit `http` , um anzugeben, dass die Seite ohne sicheres Protokoll bereitgestellt wird.<br /> Wenn sichere URLs sowohl für den Store als auch für Admin aktiviert sind, werden zwei zusätzliche Felder angezeigt, um die `HSTS`. |
| [!UICONTROL Enable HTTP Strict Transport Security (HSTS)] | Store-Ansicht | Wenn aktiviert, [`HSTS`][1] bietet eine Sicherheitsmaßnahme gegen Angriffe vom Typ &quot;man in der Mitte&quot;und verhindert, dass Benutzer die Meldung &quot;ungültiges Zertifikat&quot;überschreiben. Optionen: `Yes` / `No` |
| [!UICONTROL Upgrade Insecure Requests] | Store-Ansicht | Wenn diese Option aktiviert ist, konvertiert unsecure (`HTTP`) -Anfragen, die vom Browser an die sichere (`HTTPS`). Optionen: `Yes` / `No` |
| [!UICONTROL Offloader Header] | Global | Gibt die `offloader_header` -Wert in Ihrer Serverkonfiguration verwenden, um das Protokoll zwischen dem Client und dem Lastenausgleich zu identifizieren. Die meisten Commerce-Installationen verwenden den Standardwert, `X-Forwarded-Proto` (XFP), um das Protokoll als `HTTP` oder `HTTPS`. |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Default Pages]

![Web > Standardseiten](./assets/web-default-pages.png)<!-- zoom -->

<!-- [Default Pages configuration settings](https://docs.magento.com/user-guide/cms/pages-default.html) -->

| Feld | [Anwendungsbereich](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Default Web URL] | Store-Ansicht | Gibt die Landingpage an, die mit der Basis-URL verknüpft ist. Standardmäßig ist dies auf &quot;cms&quot;gesetzt, um eine Seite aus dem Commerce Content Management System (CMS) anzugeben. Sie können auch einen anderen Landingpage-Typ verwenden, z. B. einen Blog. Wenn beispielsweise ein Blog auf dem Server unter `magento/blog`können Sie den Namen des Ordners &quot;blog&quot; als relativen Pfad zur Seitenauswahl eingeben. |
| [!UICONTROL CMS Home Page] | Store-Ansicht | Um die Startseite für den Store auszuwählen, wählen Sie einfach die CMS-Seite aus der Liste aus. Standardmäßig listet die CMS-Startseite die gesamte Auswahl an CMS-Seiten auf, die für Ihren Store verfügbar sind. |
| [!UICONTROL Default No-route URL] | Store-Ansicht | Enthält die URL der Standardseite, die angezeigt werden soll, wenn eine `404 Page not Found` Fehler auftritt. Der Standardwert ist `cms/noroute/index`. |
| [!UICONTROL CMS No Route Page] | Store-Ansicht | Identifiziert eine bestimmte CMS-Seite, die angezeigt werden soll, wenn der Fehler &quot;404 Seite nicht gefunden&quot;auftritt. Die Standardseite ist 404 Not Found. |
| [!UICONTROL CMS No Cookies Page] | Store-Ansicht | Identifiziert eine bestimmte CMS-Seite, die angezeigt wird, wenn Cookies für den Browser nicht aktiviert sind. Auf dieser Seite wird erläutert, warum Cookies verwendet werden und wie sie für jeden Browser aktiviert werden. Die Standardseite ist Cookies aktivieren . |
| [!UICONTROL Show Breadcrumbs for CMS Pages] | Store-Ansicht | Bestimmt, ob eine Breadcrumb-Leiste auf allen CMS-Seiten im Katalog angezeigt wird. Optionen: `Yes` / `No` |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Default Layouts]

![Standardlayouts](./assets/web-default-layouts.png)<!-- zoom -->

<!--[Default Layouts](https://docs.magento.com/user-guide/design/page-layout.html) -->

| Feld | [Anwendungsbereich](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Default Product Layout] | Global | Bestimmt die [layout](../../content-design/page-layout.md) wird standardmäßig für Produktseiten verwendet. Optionen: <br/>**`No layout updates`**- Standardmäßig sind keine Layoutaktualisierungen für Produktseiten verfügbar.<br/>**`Empty`** - Standardmäßig wird ein leeres Layout für Produktseiten verwendet. <br/>**`1 column`**- Standardmäßig wird ein einspaltiges Layout für Produktseiten verwendet.<br/>**`2 columns with left bar`** - Standardmäßig wird ein zweispaltiges Layout mit der Seitenleiste auf der linken Seite für Produktseiten verwendet. <br/>**`2 columns with right bar`**- Standardmäßig wird ein zweispaltiges Layout mit der Seitenleiste auf der rechten Seite für Produktseiten verwendet.<br/>**`3 columns`** - Standardmäßig wird ein dreiseitiges Layout mit Seitenleisten auf der linken und rechten Seite für Produktseiten verwendet.<br/>**`Page -- Full Width`**- (Erfordert [!DNL Page Builder]) Standardmäßig wird das Layout Seite - Vollbreite für Produktseiten verwendet.<br/>**`Category - Full Width`** - (Erfordert [!DNL Page Builder]) Standardmäßig wird das Layout Kategorie - Vollständige Breite für Produktseiten verwendet. <br/>**`Product - Full Width`**- (Erfordert [!DNL Page Builder]) Standardmäßig wird das Layout Produkt - Vollständige Breite für Produktseiten verwendet. |
| [!UICONTROL Default Category Layout] | Global | Bestimmt die [layout](../../content-design/page-layout.md) wird standardmäßig für Kategorieseiten verwendet. Optionen: <br/>**`No layout updates`**- Standardmäßig sind keine Layoutaktualisierungen für Kategorieseiten verfügbar.<br/>**`Empty`** - Standardmäßig wird ein leeres Layout für Kategorieseiten verwendet. <br/>**`1 column`**- Standardmäßig wird ein einspaltiges Layout für Kategorieseiten verwendet.<br/>**`2 columns with left bar`** - Standardmäßig wird ein zweispaltiges Layout mit der Seitenleiste auf der linken Seite für Kategorieseiten verwendet. <br/>**`2 columns with right bar`**- Standardmäßig wird ein zweispaltiges Layout mit der Seitenleiste auf der rechten Seite für Kategorieseiten verwendet.<br/>**`3 columns`** - Standardmäßig wird ein dreiseitiges Layout mit Seitenleisten auf der linken und rechten Seite für Kategorieseiten verwendet.<br/>**`Page - Full Width`**- (Erfordert [!DNL Page Builder]) Standardmäßig wird das Layout Seite - Vollbreite für Kategorieseiten verwendet.<br/>**`Category - Full Width`** - (Erfordert [!DNL Page Builder]) Standardmäßig wird das Layout Kategorie - Vollständige Breite für Kategorieseiten verwendet. <br/>**`Product - Full Width`**- (Erfordert [!DNL Page Builder]) Standardmäßig wird das Layout Produkt - Vollständige Breite für Kategorieseiten verwendet. |
| Standardseitenlayout | Global | Bestimmt die [layout](../../content-design/page-layout.md) wird standardmäßig für CMS-Seiten verwendet. Optionen: <br/>**`No layout updates`**- Standardmäßig sind keine Layoutaktualisierungen für CMS-Seiten verfügbar.<br/>**`Empty`** - Standardmäßig wird ein leeres Layout für CMS-Seiten verwendet. <br/>**`1 column`**- Standardmäßig wird ein einspaltiges Layout für CMS-Seiten verwendet.<br/>**`2 columns with left bar`** - Standardmäßig verwendet ein zweispaltiges Layout mit der Seitenleiste auf der linken Seite für CMS-Seiten.<br/>**`2 columns with right bar`**- Standardmäßig verwendet ein zweispaltiges Layout mit der Seitenleiste auf der rechten Seite für CMS-Seiten.<br/>**`3 columns`** - Standardmäßig verwendet ein dreiseitiges Layout mit Seitenleisten auf der linken und rechten Seite für CMS-Seiten.<br/>**`Page - Full Width`**- (Erfordert [!UICONTROL Page Builder]) Standardmäßig verwendet das Layout Seite - Vollbreite für CMS-Seiten.<br/>**`Category - Full Width`** - (Erfordert [!UICONTROL Page Builder]) Standardmäßig verwendet das Layout Kategorie - Vollbreite für CMS-Seiten. <br/>**`Product - Full Width`**- (Erfordert [!DNL Page Builder]) Standardmäßig verwendet das Layout Produkt - Vollständige Breite für CMS-Seiten. |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Default Cookie Settings]

![Web > Standard-Cookie-Einstellungen](./assets/web-default-cookie-settings.png)<!-- zoom -->

<!-- [Default Cookie configuration settings](https://docs.magento.com/user-guide/stores/compliance-cookie-law.html) -->

| Feld | [Anwendungsbereich](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Cookie Lifetime] | Store-Ansicht | Bestimmt, wie lange ein Cookie vorhanden sein kann, bevor es automatisch gelöscht wird. Der Standardwert ist 3600 Sekunden (1 Stunde). |
| [!UICONTROL Cookie Path] | Store-Ansicht | Gibt die Ordner auf dem Server an, in denen Commerce-Cookies verwendet werden können. Um Commerce-Cookies überall in der Installation verfügbar zu machen, setzen Sie den Cookie-Pfad auf einen einzigen Schrägstrich: `/`. Dieser Wert kann nur den Cookie-Pfad enthalten und **_cannot_** enthält alle anderen Cookie-Parameter. |
| [!UICONTROL Cookie Domain] | Store-Ansicht | Bestimmt, ob Commerce-Cookies für Subdomains verfügbar sind. So unterstützen Sie beispielsweise `mysubdomain`.domain.com geben Sie den Namen Ihrer Domäne mit einem Punkt am Anfang ein, z. B. `.domain.com`. Dieser Wert kann nur die Cookie-Domäne enthalten und **_cannot_** enthält alle anderen Cookie-Parameter. |
| [!UICONTROL Use HTTP Only] | Store-Ansicht | Bestimmt, ob Commerce-Cookies nur über einen unsicheren Kanal (http) verwendet werden können oder auch über einen verschlüsselten Kanal (https) verwendet werden können. Optionen: `Yes` / `No` |
| [!UICONTROL Cookie Restriction Mode] | Webseite | Bestimmt, ob der Cookie-Einschränkungsmodus aktiviert ist. Optionen: `Yes` / `No` |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Session Validation Settings]

![Web > Sitzungsvalidierung](./assets/web-session-validation-settings.png)<!-- zoom -->

<!-- [Session Validation configuration settings](https://docs.magento.com/user-guide/stores/security-session-validation.html) -->

| Feld | [Anwendungsbereich](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Validate REMOTE_ADDR] | Global | Überprüft, ob die IP-Adresse einer Anforderung mit `$_SESSION` Daten. Die Sitzung wird beendet, wenn eine andere IP-Adresse erkannt wird. Optionen: `Yes` / `No` |
| [!UICONTROL Validate HTTP_VIA] | Global | Überprüft eingehende Proxy-Daten und prüft, ob die Proxy-Adresse einer Anforderung übereinstimmt `$_SESSION` Daten. Die Sitzung wird beendet, wenn eine andere Proxy-Adresse erkannt wird. Optionen: `Yes` / `No` |
| [!UICONTROL Validate HTTP_x_FORWARDED_FOR] | Global | Überprüft ausgehende Proxy-Daten und prüft, ob die weitergeleitete Adresse einer Anfrage übereinstimmt  `$_SESSION` Daten. Die Sitzung wird beendet, wenn eine andere weitergeleitete Adresse erkannt wird. Optionen: `Yes` / `No` |
| [!UICONTROL Validate HTTP_USER_AGENT] | Global | `USER_AGENT` bezieht sich auf den Browser oder das Gerät, mit dem auf die Website zugegriffen wird. Es wird überprüft, ob der Name und die Version des Browsers und des Betriebssystems mit `$_SESSION` Daten. Die Sitzung wird beendet, wenn ein anderer Benutzeragent in derselben Sitzung von einer Anfrage zu einer anderen erkannt wird. Optionen: `Yes` / `No` |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Browser Capabilities Detection]

![Web > Browserfunktionserkennung](./assets/web-browser-capabilities-detection.png)<!-- zoom -->

<!-- [Browser Capabilities Detection configuration settings](https://docs.magento.com/user-guide/stores/security-browser-capabilities-detection.html) -->

| Feld | [Anwendungsbereich](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Redirect to CMS-page if Cookies are Disabled] | Store-Ansicht | Wenn Cookies vom Browser deaktiviert werden, wird automatisch zur Seite &quot;Keine Cookies&quot;des CMS weitergeleitet. Optionen: `Yes` / `No` |
| [!UICONTROL Show Notice if JavaScript is Disabled] | Store-Ansicht | Wenn JavaScript vom Browser deaktiviert ist, wird ein Hinweis angezeigt, der den Benutzer auffordert, JavaScript-Optionen zu aktivieren: `Yes` / `No` (deaktiviert) |
| [!UICONTROL Show Notice if Local Storage is Disabled] | Store-Ansicht | Zeigt eine Meldung an, wenn der lokale Cache deaktiviert ist. Optionen: `Yes` / `No` |

{:style=&quot;table-layout:auto&quot;}

[1]: https://cheatsheetseries.owasp.org/cheatsheets/HTTP_Strict_Transport_Security_Cheat_Sheet.html
