---
title: '[!UICONTROL General] &gt; [!UICONTROL Web]'
description: Überprüfen Sie die Konfigurationseinstellungen auf der Seite [!UICONTROL General] &gt; [!UICONTROL Web] des Commerce Admin-Bereichs.
exl-id: 1809b03a-a55c-41b4-947b-f66f4bd290a1
feature: Site Management, Configuration
source-git-commit: 5a4417373f6dc720e8e14f883c27348a475ec255
workflow-type: tm+mt
source-wordcount: '1793'
ht-degree: 0%

---

# [!UICONTROL General] > [!UICONTROL Web]

{{config}}

## [!UICONTROL URL Options]

![Web > Allgemeine Optionen](./assets/web-url-options.png)<!-- zoom -->

<!-- [URL Options configuration settings](https://experienceleague.adobe.com/de/docs/commerce-admin/stores-sales/site-store/store-urls) -->

| Feld | Umfang | Beschreibung |
|  ---  |  ---  |  ---  |
| [!UICONTROL Add Store Code to URLs] | Global | Wenn Webserver-Neuschreibungen aktiviert sind, fügt den Speichercode der aktuellen Ansicht in die URL ein. Optionen: `Yes` / `No`. <br />Wenn dieses Feld auf `Yes` gesetzt ist, müssen Sie Store-Codes in Ihre Browser-URLs aufnehmen, um sicherzustellen, dass URL-Neuschreibungen korrekt zugeordnet werden und alle Seiten erfolgreich geöffnet werden. Dadurch werden Fehler _404 Page Not Found_ vermieden. |
| [!UICONTROL Auto-redirect to Base URL] | Shop-Ansicht | (Bei Einzelspeicher-Setups) Wenn auf Ihrer Site ein fehlerhafter Link vorhanden ist, leitet den Traffic an die Basis-URL weiter statt an eine Seite mit der Meldung „404 Seite nicht gefunden“. Optionen: ` No` / `Yes (302 Found)` / `Yes (301 Moved Permanently)` <br />**_Wichtig:_**&#x200B;Verwenden Sie keine automatische Umleitung zur Basis-URL für Multi-Store-Setups. |
| [!UICONTROL Catalog media URL format] | Global | Definiert das [URL-Format](../../catalog/catalog-urls.md) das Produkten und Kategorien zugewiesen ist. Optionen: Eindeutiger Hash pro Bildvariante (Legacy-Modus) definiert den konvertierten Dateinamen als eindeutigen Hash-Wert. Die auf Abfrageparametern basierende Bildoptimierung definiert [Bildoptimierung](../../content-design/media-gallery-image-optimization.md) Prozess in Abhängigkeit von Abfrageparametern. |

{style="table-layout:auto"}

## [!UICONTROL Search Engine Optimization]

![Web > Suchmaschinenoptimierung](./assets/web-search-engine-optimization.png)<!-- zoom -->

<!-- [Search Engine Optimization configuration settings](https://experienceleague.adobe.com/de/docs/commerce-admin/marketing/seo/url-rewrites/url-rewrite) -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Use Web Server Rewrites] | Shop-Ansicht | PHP-basierte Systeme enthalten in der Regel eine Datei namens `index.php` im Root-Ordner. Standardmäßig wird der Dateiname in der URL direkt nach dem Namen des Stammordners angezeigt. Wenn diese Option aktiviert ist, lässt das System `index.php` in der URL weg. Diese Best Practice für die Benutzerfreundlichkeit macht jede URL knapper und hat keine Auswirkungen auf die Leistung oder den Site-Rang. Optionen: `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Base URLs]

![Web > Basis-URLS](./assets/web-base-urls.png)<!-- zoom -->

<!-- [Base URLS configuration settings](https://experienceleague.adobe.com/de/docs/commerce-admin/stores-sales/site-store/store-urls) -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Base URL] | Shop-Ansicht | Die vollständige Adresse des Commerce-Stammordners, der nicht über einen verschlüsselten (SSL-)Kanal ausgeführt wird. Die URL muss mit einem Schrägstrich enden. |
| [!UICONTROL Base Link URL] | Shop-Ansicht | Ein Markup-Tag, das als Platzhalter für die Basis-URL verwendet wird. |
| [!UICONTROL Base URL for Static View Files] | Shop-Ansicht | Ein Pfad, der auf den Speicherort der vom Design verwendeten statischen Dateien verweist, z. B. CSS, Schriftarten, Bilder und JavaScript. Ein Platzhalter wird verwendet, um die Basis-URL darzustellen. Wenn Ihre Commerce-Installation über mehrere Sites mit derselben Ordnerstruktur verfügt, können Sie für jede Site einen anderen Ordner erstellen. Legen Sie den Konfigurationsbereich auf die richtige Site fest, bevor Sie die Basis-URL für statische Ansichtsdateien eingeben. Sie können auch einen Ordner außerhalb Ihrer Commerce-Installation angeben. |
| [!UICONTROL Base URL for User Media Files] | Shop-Ansicht | Ein Pfad, der auf den Speicherort von Katalogbildern und anderen Mediendateien verweist. Ein Platzhalter wird verwendet, um die Basis-URL darzustellen. Wenn Ihre Commerce-Installation über mehrere Sites mit derselben Ordnerstruktur verfügt, können Sie für jeden einen anderen Medienordner haben. Dadurch können Sie jeden Medienordner separat sichern und zurücksetzen. Sie können auch einen Medienordner außerhalb Ihrer Commerce-Installation angeben. |

{style="table-layout:auto"}

## [!UICONTROL Base URLs (Secure)]

![Web > Basis-URLs (sicher)](./assets/web-base-urls-secure.png)<!-- zoom -->

<!-- [Base URLs (Secure) configuration settings](https://experienceleague.adobe.com/de/docs/commerce-admin/stores-sales/site-store/store-urls) -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Secure Base URL] | Shop-Ansicht | Die vollständige Adresse des Commerce-Stammordners, der mit dem verschlüsselten sicheren Protokoll (SSL/TLS) bereitgestellt wird. Die URL muss mit einem Schrägstrich enden. |
| [!UICONTROL Secure Base Link URL] | Shop-Ansicht | Ein Markup-Tag, das als Platzhalter für die Basis-URL verwendet wird, die über einen sicheren Kanal ausgeführt wird. |
| [!UICONTROL Secure Base URL for Static View Files] | Shop-Ansicht | Ein Markup-Tag, das auf den Speicherort von statischen Dateien wie CSS, Schriftarten, Bildern und JavaScript verweist, die vom Design verwendet werden. Die Dateien können sich entweder auf einem unsicheren oder auf einem sicheren Kanal befinden. Wenn Ihre Commerce-Installation über mehrere Sites mit derselben Ordnerstruktur verfügt, können Sie für jede Site einen anderen Ordner erstellen. Legen Sie den Konfigurationsbereich auf die richtige Site fest, bevor Sie die Basis-URL für statische Ansichtsdateien eingeben. Sie können auch einen Ordner außerhalb Ihrer Commerce-Installation angeben. |
| [!UICONTROL Secure Base URL for User Media Files] | Shop-Ansicht | Ein Pfad, der auf den Speicherort von Katalogbildern und anderen Mediendateien verweist. Die Dateien können sich entweder auf einem unsicheren oder auf einem sicheren Kanal befinden. Ein Platzhalter wird verwendet, um die Basis-URL darzustellen. Wenn Ihre Commerce-Installation über mehrere Sites mit derselben Ordnerstruktur verfügt, können Sie für jeden einen anderen Medienordner haben. Dadurch können Sie jeden Medienordner separat sichern und zurücksetzen. Sie können auch einen Medienordner außerhalb Ihrer Commerce-Installation angeben. |
| [!UICONTROL Use Secure URLs on Storefront] | Shop-Ansicht | Wenn Ihre Domain über ein Sicherheitszertifikat verfügt, können Sie die Storefront mit oder ohne SSL-Verschlüsselung ausführen. Optionen: <br />**`Yes`**- Store-URLs beginnen mit `https`, um anzugeben, dass die Seite mit einem verschlüsselten, sicheren Protokoll bereitgestellt wird.<br />**`No`** - Store-URLs beginnen mit `http`, um anzugeben, dass die Seite ohne sicheres Protokoll bereitgestellt wird. |
| [!UICONTROL Use Secure URLs in Admin] | Global | Wenn Ihre Domain über ein Sicherheitszertifikat verfügt, können Sie den Store Admin mit oder ohne SSL-Verschlüsselung ausführen. Optionen: <br />**`Yes`**- Admin-URLs beginnen mit `https`, um anzugeben, dass die Seite mit einem verschlüsselten, sicheren Protokoll bereitgestellt wird.<br />**`No`** - Admin-URLs beginnen mit `http`, um anzugeben, dass die Seite ohne sicheres Protokoll bereitgestellt wird.<br /> Wenn sichere URLs für Store und Admin aktiviert sind, werden zwei zusätzliche Felder angezeigt, um `HSTS` zu aktivieren und zu konfigurieren. |
| [!UICONTROL Enable HTTP Strict Transport Security (HSTS)] | Shop-Ansicht | Wenn diese Option aktiviert ist, bietet [`HSTS`][1] ein Maß an Sicherheit gegen „Man in the Middle“-Angriffe und verhindert, dass Benutzer die Meldung „Ungültiges Zertifikat“ überschreiben. Optionen: `Yes` / `No` |
| [!UICONTROL Upgrade Insecure Requests] | Shop-Ansicht | Wenn diese Option aktiviert ist, werden vom Browser empfangene unsichere (`HTTP`) Anforderungen in das sichere (`HTTPS`) Protokoll konvertiert. Optionen: `Yes` / `No` |
| [!UICONTROL Offloader Header] | Global | Gibt den `offloader_header` Wert in Ihrer Server-Konfiguration an, um das Protokoll zwischen dem Client und dem Lastenausgleich zu identifizieren. Bei den meisten Commerce-Installationen wird der Standardwert `X-Forwarded-Proto` (XFP) verwendet, um das Protokoll entweder als `HTTP` oder `HTTPS` zu identifizieren. |

{style="table-layout:auto"}

## [!UICONTROL Default Pages]

![Web > Standardseiten](./assets/web-default-pages.png)<!-- zoom -->

<!-- [Default Pages configuration settings](https://experienceleague.adobe.com/de/docs/commerce-admin/content-design/elements/pages/pages#configure-default-pages) -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Default Web URL] | Shop-Ansicht | Gibt die Landingpage an, die mit der Basis-URL verknüpft ist. Dies ist standardmäßig auf „cms“ festgelegt, um eine Seite aus dem Commerce Content Management System (CMS) anzugeben. Sie können auch einen anderen Typ von Landingpage verwenden, z. B. einen Blog. Wenn beispielsweise ein Blog auf dem Server unter `magento/blog` installiert ist, können Sie den Namen des Ordners „blog“ als relativen Pfad zur Auswahl der Seiten eingeben. |
| [!UICONTROL CMS Home Page] | Shop-Ansicht | Um die Startseite für den Store auszuwählen, wählen Sie einfach die CMS-Seite aus der Liste aus. Standardmäßig listet die CMS-Startseite alle CMS-Seiten auf, die für Ihren Store verfügbar sind. |
| [!UICONTROL Default No-route URL] | Shop-Ansicht | Enthält die URL der Standardseite, die angezeigt werden soll, wenn ein `404 Page not Found` auftritt. Der Standardwert ist `cms/noroute/index`. |
| [!UICONTROL CMS No Route Page] | Shop-Ansicht | Gibt eine bestimmte CMS-Seite an, die angezeigt werden soll, wenn der Fehler 404 Page Not Found auftritt. Die Standardseite ist 404 Nicht gefunden. |
| [!UICONTROL CMS No Cookies Page] | Shop-Ansicht | Gibt eine bestimmte CMS-Seite an, die angezeigt wird, wenn Cookies für den Browser nicht aktiviert sind. Auf dieser Seite wird erläutert, warum Cookies verwendet werden und wie Sie sie für jeden Browser aktivieren können. Die Standardseite ist Cookies aktivieren. |
| [!UICONTROL Show Breadcrumbs for CMS Pages] | Shop-Ansicht | Legt fest, ob eine Breadcrumb-Spur auf allen CMS-Seiten im Katalog angezeigt wird. Optionen: `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Default Layouts]

![Standard-Layouts](./assets/web-default-layouts.png)<!-- zoom -->

<!--[Default Layouts](https://experienceleague.adobe.com/de/docs/commerce-admin/content-design/design/layout/page-layout) -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Default Product Layout] | Global | Bestimmt das [Layout](../../content-design/page-layout.md), das standardmäßig für Produktseiten verwendet wird. Optionen: <br/>**`No layout updates`**- Standardmäßig sind Layout-Aktualisierungen für Produktseiten nicht verfügbar.<br/>**`Empty`** - verwendet standardmäßig ein leeres Layout für Produktseiten. <br/>**`1 column`**- Verwendet standardmäßig ein einspaltiges Layout für Produktseiten.<br/>**`2 columns with left bar`** - Standardmäßig wird ein zweispaltiges Layout mit der Seitenleiste auf der linken Seite für Produktseiten verwendet. <br/>**`2 columns with right bar`**- Standardmäßig wird ein zweispaltiges Layout mit der Seitenleiste auf der rechten Seite für Produktseiten verwendet.<br/>**`3 columns`** - Standardmäßig wird ein dreispaltiges Layout mit Seitenleisten links und rechts für Produktseiten verwendet.<br/>**`Page -- Full Width`**- (Erfordert [!DNL Page Builder]) Standardmäßig verwendet das Layout Seite - Volle Breite für Produktseiten.<br/>**`Category - Full Width`** - (Erfordert [!DNL Page Builder]) Standardmäßig verwendet das Layout Kategorie - Volle Breite für Produktseiten. <br/>**`Product - Full Width`**- (Erfordert [!DNL Page Builder]) Standardmäßig verwendet das Layout Produkt - Volle Breite für Produktseiten. |
| [!UICONTROL Default Category Layout] | Global | Bestimmt das [Layout](../../content-design/page-layout.md), das standardmäßig für Kategorieseiten verwendet wird. Optionen: <br/>**`No layout updates`**- Standardmäßig sind Layout-Aktualisierungen für Kategorieseiten nicht verfügbar.<br/>**`Empty`** - verwendet standardmäßig ein leeres Layout für Kategorieseiten. <br/>**`1 column`**- Verwendet standardmäßig ein einspaltiges Layout für Kategorieseiten.<br/>**`2 columns with left bar`** - Standardmäßig wird ein zweispaltiges Layout mit der Seitenleiste auf der linken Seite für Kategorieseiten verwendet. <br/>**`2 columns with right bar`**- Standardmäßig wird ein zweispaltiges Layout mit der Seitenleiste auf der rechten Seite für Kategorieseiten verwendet.<br/>**`3 columns`** - Standardmäßig wird ein dreispaltiges Layout mit Seitenleisten links und rechts für Kategorieseiten verwendet.<br/>**`Page - Full Width`**- (Erfordert [!DNL Page Builder]) Standardmäßig verwendet das Layout Seite - Volle Breite für Kategorieseiten.<br/>**`Category - Full Width`** - (Erfordert [!DNL Page Builder]) Standardmäßig verwendet das Layout Kategorie - Volle Breite für Kategorieseiten. <br/>**`Product - Full Width`**- (Erfordert [!DNL Page Builder]) Standardmäßig verwendet das Layout Produkt - Volle Breite für Kategorieseiten. |
| Standard-Seitenlayout | Global | Bestimmt das [Layout](../../content-design/page-layout.md), das standardmäßig für CMS-Seiten verwendet wird. Optionen: <br/>**`No layout updates`**- Für CMS-Seiten sind Layout-Aktualisierungen standardmäßig nicht verfügbar.<br/>**`Empty`** - Verwendet standardmäßig ein leeres Layout für CMS-Seiten. <br/>**`1 column`**- Verwendet standardmäßig ein einspaltiges Layout für CMS-Seiten.<br/>**`2 columns with left bar`** - Standardmäßig wird ein zweispaltiges Layout mit der Seitenleiste auf der linken Seite für CMS-Seiten verwendet.<br/>**`2 columns with right bar`**- Für CMS-Seiten wird standardmäßig ein zweispaltiges Layout mit der Seitenleiste auf der rechten Seite verwendet.<br/>**`3 columns`** - Für CMS-Seiten wird standardmäßig ein dreispaltiges Layout mit Seitenleisten links und rechts verwendet.<br/>**`Page - Full Width`**- ([!UICONTROL Page Builder] erforderlich) Standardmäßig verwendet das Layout Seite - Volle Breite für CMS-Seiten.<br/>**`Category - Full Width`** - (Erfordert [!UICONTROL Page Builder]) Standardmäßig verwendet das Layout Kategorie - Volle Breite für CMS-Seiten. <br/>**`Product - Full Width`**- ([!DNL Page Builder] erforderlich) Standardmäßig verwendet das Layout Produkt - Volle Breite für CMS-Seiten. |

{style="table-layout:auto"}

## [!UICONTROL Default Cookie Settings]

![Web > Standard-Cookie-Einstellungen](./assets/web-default-cookie-settings.png)<!-- zoom -->

<!-- [Default Cookie configuration settings](https://experienceleague.adobe.com/de/docs/commerce-admin/start/compliance/privacy/compliance-cookie-law) -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Cookie Lifetime] | Shop-Ansicht | Bestimmt, wie lange ein Cookie vorhanden sein kann, bevor es automatisch gelöscht wird. Der Standardwert ist 3600 Sekunden (1 Stunde) |
| [!UICONTROL Cookie Path] | Shop-Ansicht | Gibt die Ordner auf dem Server an, in denen Commerce-Cookies verwendet werden können. Um Commerce-Cookies überall in der Installation verfügbar zu machen, setzen Sie den Cookie-Pfad auf einen einzelnen Schrägstrich: `/`. Dieser Wert kann nur den Cookie-Pfad enthalten und **_keine_** Cookie-Parameter enthalten. |
| [!UICONTROL Cookie Domain] | Shop-Ansicht | Bestimmt, ob Commerce-Cookies für Subdomains verfügbar sind. Um beispielsweise `mysubdomain`.domain.com zu unterstützen, geben Sie den Namen Ihrer Domain mit einem Punkt am Anfang ein, z. B. `.domain.com`. Dieser Wert kann nur die Cookie-Domain enthalten und **_kann_** keine anderen Cookie-Parameter enthalten. |
| [!UICONTROL Use HTTP Only] | Shop-Ansicht | Bestimmt, ob Commerce-Cookies nur über einen unsicheren Kanal (http) oder auch über einen verschlüsselten Kanal (https) verwendet werden können. Optionen: `Yes` / `No` |
| [!UICONTROL Cookie Restriction Mode] | Website | Bestimmt, ob der Cookie-Einschränkungsmodus aktiviert ist. Optionen: `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Session Validation Settings]

![Web > Sitzungsvalidierung](./assets/web-session-validation-settings.png)<!-- zoom -->

<!-- [Session Validation configuration settings](https://experienceleague.adobe.com/de/docs/commerce-admin/systems/security/security-session-management#session-validation) -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Validate REMOTE_ADDR] | Global | Prüft, ob die IP-Adresse einer Anfrage mit `$_SESSION` Daten übereinstimmt. Die Sitzung wird beendet, wenn eine andere IP-Adresse erkannt wird. Optionen: `Yes` / `No` |
| [!UICONTROL Validate HTTP_VIA] | Global | Überprüft eingehende Proxy-Daten und stellt sicher, dass die Proxy-Adresse einer Anfrage mit `$_SESSION` Daten übereinstimmt. Die Sitzung wird beendet, wenn eine andere Proxy-Adresse erkannt wird. Optionen: `Yes` / `No` |
| [!UICONTROL Validate HTTP_x_FORWARDED_FOR] | Global | Prüft ausgehende Proxydaten und prüft, ob die weitergeleitete Adresse einer Anfrage mit `$_SESSION` Daten übereinstimmt. Die Sitzung wird beendet, wenn eine andere Weiterleitungsadresse erkannt wird. Optionen: `Yes` / `No` |
| [!UICONTROL Validate HTTP_USER_AGENT] | Global | `USER_AGENT` bezieht sich auf den Browser oder das Gerät, der bzw. das für den Zugriff auf die Website verwendet wird. Er überprüft, ob der Name und die Version des Browsers und des Betriebssystems mit `$_SESSION` Daten übereinstimmen. Die Sitzung wird beendet, wenn in derselben Sitzung ein anderer Benutzeragent von einer Anfrage zu einer anderen erkannt wird. Optionen: `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Browser Capabilities Detection]

![Web > Browser-Erkennung](./assets/web-browser-capabilities-detection.png)<!-- zoom -->

<!-- [Browser Capabilities Detection configuration settings](https://experienceleague.adobe.com/de/docs/commerce-admin/systems/security/security-browser-capabilities-detection) -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Redirect to CMS-page if Cookies are Disabled] | Shop-Ansicht | Wenn Cookies vom Browser deaktiviert werden, werden sie automatisch zur CMS-Seite Keine Cookies weitergeleitet. Optionen: `Yes` / `No` |
| [!UICONTROL Show Notice if JavaScript is Disabled] | Shop-Ansicht | Wenn JavaScript vom Browser deaktiviert wird, wird ein Hinweis angezeigt, der den Benutzer auffordert, die JavaScript-Optionen zu aktivieren: `Yes` / `No` (deaktiviert) |
| [!UICONTROL Show Notice if Local Storage is Disabled] | Shop-Ansicht | Zeigt eine Meldung an, wenn der lokale Cache deaktiviert ist. Optionen: `Yes` / `No` |

{style="table-layout:auto"}

[1]: https://cheatsheetseries.owasp.org/cheatsheets/HTTP_Strict_Transport_Security_Cheat_Sheet.html
