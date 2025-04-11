---
source-git-commit: a37e67c332140fbba7609db8cc5e22a3625a1c9d
workflow-type: tm+mt
source-wordcount: '2387'
ht-degree: 0%

---
# Adobe Commerce mit B2B-Paketen

<!-- The 'packages' variable contains the 'packages' node of the '_data/codebase/b2b/composer_lock.json' file
 -->

<!-- The 'packages-dev' variable contains the 'packages-dev' node of the '_data/codebase/b2b/composer_lock.json' file
 -->

<!-- The 'product' variable contains data of the 'magento/product-enterprise-edition' package
 -->

<!-- The edition variable contains `commerce-b2b` value from the _data/names.yml file
 -->

Adobe Commerce B2B verwendet Composer, um PHP-Pakete zu verwalten.

In der `composer.json`-Datei wird die Liste der Pakete deklariert, während in der `composer.lock`-Datei eine vollständige Liste der Pakete (eine Vollversion jedes Pakets und seiner Abhängigkeiten) gespeichert wird, die zum Erstellen einer Installation von Adobe Commerce B2B verwendet werden.

Die folgende Referenzdokumentation wird aus der `composer.lock` generiert und behandelt die erforderlichen Pakete in Adobe Commerce B2B 1.5.2.

## Abhängigkeiten

`magento/extension-b2b 1.5.2` weist die folgenden Abhängigkeiten auf:

- Magento/Framework: >=103.0.6 &lt;103.0.9
- Magento/Magento2-B2B-Base: 1.5.2
- [magento/module-B2B](https://developer.adobe.com/commerce/php/module-reference/module-b2b/): 100.5.2
- [magento/module-bundle-negotiate-quote](https://developer.adobe.com/commerce/php/module-reference/module-bundle-negotiable-quote/): 100.5.1
- [magento/module-bundle-requisition-list](https://developer.adobe.com/commerce/php/module-reference/module-bundle-requisition-list/): 100.5.1
- [magento/module-bundle-requisition-list-graph-ql](https://developer.adobe.com/commerce/php/module-reference/module-bundle-requisition-list-graph-ql/): 1.5.1
- [magento/module-bundle-shared-catalog](https://developer.adobe.com/commerce/php/module-reference/module-bundle-shared-catalog/): 100.5.1
- [magento/module-checkout-address-search-negotiate-quote](https://developer.adobe.com/commerce/php/module-reference/module-checkout-address-search-negotiable-quote/): 100.5.1
- [magento/module-checkout-agreement-negotiate-quote](https://developer.adobe.com/commerce/php/module-reference/module-checkout-agreements-negotiable-quote/): 100.5.1
- [magento/module-checkout-agreement-purchase-order](https://developer.adobe.com/commerce/php/module-reference/module-checkout-agreements-purchase-order/): 1.5.1
- [magento/module-company](https://developer.adobe.com/commerce/php/module-reference/module-company/): 102.0.2
- [magento/module-company-asynchronous-operations](https://developer.adobe.com/commerce/php/module-reference/module-company-asynchronous-operations/): 1.5.1
- [magento/module-company-credit](https://developer.adobe.com/commerce/php/module-reference/module-company-credit/): 100.5.2
- [magento/module-company-credit-graph-ql](https://developer.adobe.com/commerce/php/module-reference/module-company-credit-graph-ql/): 1.5.1
- [magento/module-company-customer-import-export](https://developer.adobe.com/commerce/php/module-reference/module-company-customer-import-export/): 1.5.0
- [magento/module-company-graph-ql](https://developer.adobe.com/commerce/php/module-reference/module-company-graph-ql/): 1.5.2
- [magento/module-company-negotiate-quote](https://developer.adobe.com/commerce/php/module-reference/module-company-negotiable-quote/): 1.5.1
- [magento/module-company-negotiate-quote-template](https://developer.adobe.com/commerce/php/module-reference/module-company-negotiable-quote-template/): 1.5.1
- [magento/module-company-payment](https://developer.adobe.com/commerce/php/module-reference/module-company-payment/): 100.5.1
- [magento/module-company-quote](https://developer.adobe.com/commerce/php/module-reference/module-company-quote/): 1.5.2
- [magento/module-company-quote-graph-ql](https://developer.adobe.com/commerce/php/module-reference/module-company-quote-graph-ql/): 1.5.2
- [magento/module-company-relation](https://developer.adobe.com/commerce/php/module-reference/module-company-relation/): 1.5.2
- [magento/module-company-relation-shared-catalog](https://developer.adobe.com/commerce/php/module-reference/module-company-relation-shared-catalog/): 1.5.1
- [magento/module-company-shipping](https://developer.adobe.com/commerce/php/module-reference/module-company-shipping/): 1.5.1
- [magento/module-configurable-Negotiable-quote](https://developer.adobe.com/commerce/php/module-reference/module-configurable-negotiable-quote/): 100.5.1
- [magento/module-configurable-requirement-list](https://developer.adobe.com/commerce/php/module-reference/module-configurable-requisition-list/): 100.5.1
- [magento/module-configurable-requirement-list-graph-ql](https://developer.adobe.com/commerce/php/module-reference/module-configurable-requisition-list-graph-ql/): 1.5.1
- [magento/module-configurable-shared-catalog](https://developer.adobe.com/commerce/php/module-reference/module-configurable-shared-catalog/): 100.5.1
- [magento/module-downloadable-company](https://developer.adobe.com/commerce/php/module-reference/module-downloadable-company/): 1.5.1
- [magento/module-downloadable-requirement-list-graph-ql](https://developer.adobe.com/commerce/php/module-reference/module-downloadable-requisition-list-graph-ql/): 1.5.1
- [magento/module-gift-card-negotiate-quote](https://developer.adobe.com/commerce/php/module-reference/module-gift-card-negotiable-quote/): 100.5.1
- [magento/module-gift-card-requisition-list](https://developer.adobe.com/commerce/php/module-reference/module-gift-card-requisition-list/): 100.5.1
- [magento/module-gift-card-requisition-list-graph-ql](https://developer.adobe.com/commerce/php/module-reference/module-gift-card-requisition-list-graph-ql/): 1.5.1
- [magento/module-gift-card-shared-catalog](https://developer.adobe.com/commerce/php/module-reference/module-gift-card-shared-catalog/): 100.5.1
- [magento/module-grouped-requisition-list](https://developer.adobe.com/commerce/php/module-reference/module-grouped-requisition-list/): 100.5.1
- [magento/module-grouped-shared-catalog](https://developer.adobe.com/commerce/php/module-reference/module-grouped-shared-catalog/): 100.5.1
- [magento/module-Negotiable-quote](https://developer.adobe.com/commerce/php/module-reference/module-negotiable-quote/): 101.0.2
- [magento/module-negotiate-quote-async-order](https://developer.adobe.com/commerce/php/module-reference/module-negotiable-quote-async-order/): 1.5.1
- [magento/module-Negotiable-quote-duplicate](https://developer.adobe.com/commerce/php/module-reference/module-negotiable-quote-duplicate/): 1.5.2
- [magento/module-Negotiable-quote-duplicate-graph-ql](https://developer.adobe.com/commerce/php/module-reference/module-negotiable-quote-duplicate-graph-ql/): 1.5.1
- [magento/module-Negotiable-quote-graph-ql](https://developer.adobe.com/commerce/php/module-reference/module-negotiable-quote-graph-ql/): 1.5.1
- [magento/module-Negotiable-quote-requirement-list](https://developer.adobe.com/commerce/php/module-reference/module-negotiable-quote-requisition-list/): 1.5.1
- [magento/module-Negotiable-quote-requirement-list-graph-ql](https://developer.adobe.com/commerce/php/module-reference/module-negotiable-quote-requisition-list-graph-ql/): 1.5.1
- [magento/module-negotiate-quote-shared-catalog](https://developer.adobe.com/commerce/php/module-reference/module-negotiable-quote-shared-catalog/): 100.5.1
- [magento/module-Negotiable-quote-template](https://developer.adobe.com/commerce/php/module-reference/module-negotiable-quote-template/): 1.5.2
- [magento/module-Negotiable-quote-template-graph-ql](https://developer.adobe.com/commerce/php/module-reference/module-negotiable-quote-template-graph-ql/): 1.5.2
- [magento/module-negotiate-quote-template-shared-catalog](https://developer.adobe.com/commerce/php/module-reference/module-negotiable-quote-template-shared-catalog/): 1.5.1
- [magento/module-negotiate-quote-weee](https://developer.adobe.com/commerce/php/module-reference/module-negotiable-quote-weee/): 100.5.1
- [magento/module-order-history-search](https://developer.adobe.com/commerce/php/module-reference/module-order-history-search/): 100.5.2
- [magento/module-paypal-negotiate-quote](https://developer.adobe.com/commerce/php/module-reference/module-paypal-negotiable-quote/): 1.5.1
- [magento/module-paypal-purchase-order](https://developer.adobe.com/commerce/php/module-reference/module-paypal-purchase-order/): 1.5.1
- [magento/module-purchase-order](https://developer.adobe.com/commerce/php/module-reference/module-purchase-order/): 100.5.2
- [magento/module-purchase-order-graph-ql](https://developer.adobe.com/commerce/php/module-reference/module-purchase-order-graph-ql/): 1.5.1
- [magento/module-purchase-order-rule](https://developer.adobe.com/commerce/php/module-reference/module-purchase-order-rule/): 100.5.2
- [magento/module-purchase-order-rule-graph-ql](https://developer.adobe.com/commerce/php/module-reference/module-purchase-order-rule-graph-ql/): 1.5.1
- [magento/module-quick-order](https://developer.adobe.com/commerce/php/module-reference/module-quick-order/): 100.5.1
- [magento/module-quick-order-graph-ql](https://developer.adobe.com/commerce/php/module-reference/module-quick-order-graph-ql/): 1.5.1
- [magento/module-requirement-list](https://developer.adobe.com/commerce/php/module-reference/module-requisition-list/): 100.5.2
- [magento/module-requirement-list-graph-ql](https://developer.adobe.com/commerce/php/module-reference/module-requisition-list-graph-ql/): 1.5.1
- [magento/module-shared-catalog](https://developer.adobe.com/commerce/php/module-reference/module-shared-catalog/): 100.5.2
- [magento/module-shared-catalog-graph-ql](https://developer.adobe.com/commerce/php/module-reference/module-shared-catalog-graph-ql/): 1.5.1
- magento/security-package-b2b: 1.0.6

## Drittanbieterlizenzen

### Apache-2.0, nur LGPL-2.1

<table>
  <thead>
    <tr>
      <th>-Name</th>
      <th>Typ</th>
      <th>Beschreibung</th>
    </tr>
  </thead>
  <tbody>
  <tr>
    <td>
      <a href="https://github.com/opensearch-project/opensearch-php">opensearch-project/opensearch-php</a>
    </td>
    <td>Bibliothek</td>
    <td>PHP-Client für OpenSearch</td>
  </tr>
  </tbody>
</table>

### Apache-2.0

<table>
  <thead>
    <tr>
      <th>-Name</th>
      <th>Typ</th>
      <th>Beschreibung</th>
    </tr>
  </thead>
  <tbody>
  <tr>
    <td>
      <a href="https://github.com/adobe/stock-api-libphp">astock/stock-api-libphp</a>
    </td>
    <td>Bibliothek</td>
    <td>Adobe Stock-API-Bibliothek</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/awslabs/aws-crt-php">aws/aws-crt-php</a>
    </td>
    <td>Bibliothek</td>
    <td>AWS Common Runtime für PHP</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/aws/aws-sdk-php">aws/aws-sdk-php</a>
    </td>
    <td>Bibliothek</td>
    <td>AWS SDK für PHP - Verwenden von Amazon Web Services in Ihrem PHP-Projekt</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/opentelemetry-php/api">open-telemetry/api</a>
    </td>
    <td>Bibliothek</td>
    <td>API für OpenTelemetry PHP.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/opentelemetry-php/context">open-telemetry/context</a>
    </td>
    <td>Bibliothek</td>
    <td>Kontext-Implementierung für OpenTelemetry PHP.</td>
  </tr>
  <tr>
    <td>
      PayPal/Modul-Braintree
    </td>
    <td>Metapaket</td>
    <td>Braintree Magento</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/wikimedia/less.php">wikimedia/less.php</a>
    </td>
    <td>Bibliothek</td>
    <td>PHP-Port des LESS-Prozessors</td>
  </tr>
  </tbody>
</table>

### BSD-2-Satz

<table>
  <thead>
    <tr>
      <th>-Name</th>
      <th>Typ</th>
      <th>Beschreibung</th>
    </tr>
  </thead>
  <tbody>
  <tr>
    <td>
      <a href="https://github.com/Bacon/BaconQrCode">bacon/bacon-qr-code</a>
    </td>
    <td>Bibliothek</td>
    <td>BaconQrCode ist ein QR-Code-Generator für PHP.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/DASPRiD/Enum">Dasprid/Enum</a>
    </td>
    <td>Bibliothek</td>
    <td>PHP 7.1 Enum-Implementierung</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/webimpress/safe-writer">WebImpress/Safe-Writer</a>
    </td>
    <td>Bibliothek</td>
    <td>Tool zum sicheren Schreiben von Dateien, um Wettlaufsituationen zu vermeiden</td>
  </tr>
  </tbody>
</table>

### BSD-3-Satz

<table>
  <thead>
    <tr>
      <th>-Name</th>
      <th>Typ</th>
      <th>Beschreibung</th>
    </tr>
  </thead>
  <tbody>
  <tr>
    <td>
      <a href="https://github.com/colinmollenhour/Cm_Cache_Backend_File">colinmollenhour/cache-backend-file</a>
    </td>
    <td>Magento-module</td>
    <td>Das Backend der Stock-Zend_Cache_Backend_File-Datei hat eine extrem schlechte Leistung für die Reinigung von Tags, wodurch es unbrauchbar wird, wenn die Anzahl der zwischengespeicherten Elemente steigt. Dieses Backend nimmt viele Änderungen vor, die zu einer enormen Leistungssteigerung führen, insbesondere bei der Tag-Reinigung.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/colinmollenhour/php-redis-session-abstract">colinmollenhour/php-redis-session-abstract</a>
    </td>
    <td>Bibliothek</td>
    <td>Ein Redis-basierter Sitzungs-Handler mit optimistischer Sperrung</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/duosecurity/duo_universal_php">duosecurity/duo_universal_php</a>
    </td>
    <td>Bibliothek</td>
    <td>Eine PHP-Implementierung des Duo Universal SDK.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/firebase/php-jwt">Firebase/php-jwt</a>
    </td>
    <td>Bibliothek</td>
    <td>Eine einfache Bibliothek zum Codieren und Decodieren von JSON Web Tokens (JWT) in PHP. Sollte der aktuellen Spezifikation entsprechen.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-captcha">laminas/laminas-captcha</a>
    </td>
    <td>Bibliothek</td>
    <td>Generieren und Validieren von CAPTCHAs mit Fillets, Bildern, ReCAPTCHA und mehr</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-code">laminas/laminas-code</a>
    </td>
    <td>Bibliothek</td>
    <td>Erweiterungen der PHP Reflection API, statisches Codescannen und Codegenerierung</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-config">laminas/laminas-config</a>
    </td>
    <td>Bibliothek</td>
    <td>Stellt eine auf verschachtelten Objekteigenschaften basierende Benutzeroberfläche für den Zugriff auf diese Konfigurationsdaten im Anwendungscode bereit</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-di">laminas/laminas-di</a>
    </td>
    <td>Bibliothek</td>
    <td>Automatisierte Injektion von Abhängigkeiten für PSR-11-Container</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-escaper">Laminas/Laminas-Escaper</a>
    </td>
    <td>Bibliothek</td>
    <td>Sicheres und sicheres Maskieren von HTML, HTML-Attributen, JavaScript, CSS und URLs</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-eventmanager">laminas/laminas-eventManager</a>
    </td>
    <td>Bibliothek</td>
    <td>Trigger und Überwachen von Ereignissen in einer PHP-Anwendung</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-feed">laminas/laminas-feed</a>
    </td>
    <td>Bibliothek</td>
    <td>bietet Funktionen zum Erstellen und Verwenden von RSS- und Atom-Feeds</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-filter">LAMINAS/LAMINAS-FILTER</a>
    </td>
    <td>Bibliothek</td>
    <td>Programmgesteuertes Filtern und Normalisieren von Daten und Dateien</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-http">laminas/laminas-http</a>
    </td>
    <td>Bibliothek</td>
    <td>Bietet eine einfache Schnittstelle zum Ausführen von HTTP-Anfragen (Hyper-Text Transfer Protocol)</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-i18n">LAMINAS/LAMINAS-I18N</a>
    </td>
    <td>Bibliothek</td>
    <td>Übersetzungen für Ihre Anwendung bereitstellen und internationalisierte Werte filtern und validieren</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-json">laminas/laminas-json</a>
    </td>
    <td>Bibliothek</td>
    <td>bietet praktische Methoden zum Serialisieren von nativem PHP zu JSON und zum Dekodieren von JSON zu nativem PHP</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-loader">LAMINAS/LAMINAS-LOADER</a>
    </td>
    <td>Bibliothek</td>
    <td>Strategien zum automatischen Laden und Laden von Plug-ins</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-modulemanager">laminas/laminas-modulemanager</a>
    </td>
    <td>Bibliothek</td>
    <td>Modulares Applikationssystem für Laminas-MVC-Anwendungen</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-mvc">LAMINAS/LAMINAS-MVC</a>
    </td>
    <td>Bibliothek</td>
    <td>Die ereignisgesteuerte MVC-Schicht von Laminas, einschließlich MVC-Anwendungen, Controller und Plug-ins</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-permissions-acl">laminas/laminas-permissions-acl</a>
    </td>
    <td>Bibliothek</td>
    <td>Bietet eine einfache und flexible Implementierung der Zugriffssteuerungsliste (ACL) für die Verwaltung von Berechtigungen</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-recaptcha">laminas/laminas-reCAPTCHA</a>
    </td>
    <td>Bibliothek</td>
    <td>OOP-Wrapper für den ReCaptcha-Webservice</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-router">laminas/laminas-router</a>
    </td>
    <td>Bibliothek</td>
    <td>Flexibles Routing-System für HTTP- und Konsolenanwendungen</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-server">LAMINAS/LAMINAS-SERVER</a>
    </td>
    <td>Bibliothek</td>
    <td>Erstellen von Reflection-basierten RPC-Servern</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-servicemanager">laminas/laminas-serviceManager</a>
    </td>
    <td>Bibliothek</td>
    <td>werkseitiger Injektor für die Injektion von Abhängigkeiten</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-session">laminas/laminas-session</a>
    </td>
    <td>Bibliothek</td>
    <td>Objektorientierte Schnittstelle zu PHP-Sitzungen und -Speicher</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-soap">laminas/laminas-soap</a>
    </td>
    <td>Bibliothek</td>
    <td></td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-stdlib">laminas/laminas-stdlib</a>
    </td>
    <td>Bibliothek</td>
    <td>SPL-Erweiterungen, Array-Dienstprogramme, Fehler-Handler und mehr</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-text">laminas/laminas-text</a>
    </td>
    <td>Bibliothek</td>
    <td>Erstellen von Feigenblättern und textbasierten Tabellen</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-translator">laminas/laminas-translator</a>
    </td>
    <td>Bibliothek</td>
    <td>Schnittstellen für die Übersetzerkomponente von laminas-i18n</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-uri">laminas/laminas-uri</a>
    </td>
    <td>Bibliothek</td>
    <td>Eine Komponente, die bei der Bearbeitung und Validierung von „URIs“ (Uniform Resource Identifiers) hilft</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-validator">laminas/laminas-validator</a>
    </td>
    <td>Bibliothek</td>
    <td>Validierungsklassen für eine Vielzahl von Domains und die Möglichkeit, Validatoren zu verketten, um komplexe Validierungskriterien zu erstellen</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-view">laminas/laminas-view</a>
    </td>
    <td>Bibliothek</td>
    <td>Flexible Ansichtsebene unterstützt und bietet mehrere Ansichtsebenen, Helper und mehr</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/marc-mabe/php-enum">marc-mabe/php-enum</a>
    </td>
    <td>Bibliothek</td>
    <td>Einfache und schnelle Implementierung von Auflistungen mit nativem PHP</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/nikic/PHP-Parser">nikic/php-parser</a>
    </td>
    <td>Bibliothek</td>
    <td>Ein in PHP geschriebener PHP-Parser</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/phpfui/recaptcha">phpfui/reCAPTCHA</a>
    </td>
    <td>Bibliothek</td>
    <td>Client-Bibliothek für reCAPTCHA von Google für PHP 8.4 und höher</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/tedious/JShrink">tedivm/jsShrink</a>
    </td>
    <td>Bibliothek</td>
    <td>In PHP eingebauter JavaScript-Minimierer</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/tubalmartin/YUI-CSS-compressor-PHP-port">tubalmartin/cssmin</a>
    </td>
    <td>Bibliothek</td>
    <td>Ein PHP-Port des YUI CSS-Kompressors</td>
  </tr>
  </tbody>
</table>

### BSD-3-Clause-Modifikation

<table>
  <thead>
    <tr>
      <th>-Name</th>
      <th>Typ</th>
      <th>Beschreibung</th>
    </tr>
  </thead>
  <tbody>
  <tr>
    <td>
      <a href="https://github.com/colinmollenhour/Cm_Cache_Backend_Redis">colinmollenhour/cache-backend-redis</a>
    </td>
    <td>Magento-module</td>
    <td>Zend_Cache-Backend mit Redis mit voller Unterstützung für Tags.</td>
  </tr>
  </tbody>
</table>

### ISC

<table>
  <thead>
    <tr>
      <th>-Name</th>
      <th>Typ</th>
      <th>Beschreibung</th>
    </tr>
  </thead>
  <tbody>
  <tr>
    <td>
      <a href="https://github.com/paragonie/sodium_compat">Paragonie/Natrium_compat</a>
    </td>
    <td>Bibliothek</td>
    <td>Reine PHP-Implementierung von libnati; verwendet die PHP-Erweiterung, falls vorhanden</td>
  </tr>
  </tbody>
</table>

### LGPL-2.1-or-later

<table>
  <thead>
    <tr>
      <th>-Name</th>
      <th>Typ</th>
      <th>Beschreibung</th>
    </tr>
  </thead>
  <tbody>
  <tr>
    <td>
      <a href="https://github.com/ezyang/htmlpurifier">ezyang/htmlPurifier</a>
    </td>
    <td>Bibliothek</td>
    <td>Standardkonformer HTML-Filter in PHP</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/php-amqplib/php-amqplib">php-amqplib/php-amqplib</a>
    </td>
    <td>Bibliothek</td>
    <td>Vormals videlalvaro/php-amqplib.  Diese Bibliothek ist eine reine PHP-Implementierung des AMQP-Protokolls. Es wurde gegen RabbitMQ getestet.</td>
  </tr>
  </tbody>
</table>

### MIT

<table>
  <thead>
    <tr>
      <th>-Name</th>
      <th>Typ</th>
      <th>Beschreibung</th>
    </tr>
  </thead>
  <tbody>
  <tr>
    <td>
      <a href="https://github.com/braintree/braintree_php">braintree/braintree_php</a>
    </td>
    <td>Bibliothek</td>
    <td>Braintree PHP-Client-Bibliothek</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/brick/math">Stein/Mathematik</a>
    </td>
    <td>Bibliothek</td>
    <td>Arithmetische Bibliothek mit beliebiger Genauigkeit</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/brick/varexporter">brick/varexporter</a>
    </td>
    <td>Bibliothek</td>
    <td>Eine leistungsstarke Alternative zu var_export(), die Schließungen und Objekte ohne __set_state() exportieren kann</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/ChristianRiesen/base32">Christian-Riesen/base32</a>
    </td>
    <td>Bibliothek</td>
    <td>Base32 Encoder/Decoder nach RFC 4648</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/colinmollenhour/credis">colinmollenhour/credis</a>
    </td>
    <td>Bibliothek</td>
    <td>Credis ist eine einfache Schnittstelle zum Redis-Schlüssel-Wert-Store, der die phpredis-Bibliothek umschließt, wenn sie für eine bessere Leistung verfügbar ist.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/composer/ca-bundle">composer/ca-bundle</a>
    </td>
    <td>Bibliothek</td>
    <td>Ermöglicht die Suche nach einem Pfad zum System-CA-Bundle und beinhaltet ein Fallback zum Mozilla CA-Bundle.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/composer/class-map-generator">composer/class-map-generator</a>
    </td>
    <td>Bibliothek</td>
    <td>Dienstprogramme zum Scannen von PHP-Code und Generieren von Klassenzuordnungen.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/composer/composer">Komponist/Komponist</a>
    </td>
    <td>Bibliothek</td>
    <td>Composer unterstützt Sie beim Deklarieren, Verwalten und Installieren von Abhängigkeiten von PHP-Projekten. Dadurch wird sichergestellt, dass Sie überall den richtigen Stack haben.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/composer/metadata-minifier">composer/metadata-minifier</a>
    </td>
    <td>Bibliothek</td>
    <td>Kleine Dienstprogrammbibliothek, die für die Minimierung und Erweiterung von Metadaten zuständig ist.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/composer/pcre">Composer/PCRE</a>
    </td>
    <td>Bibliothek</td>
    <td>PCRE Wrapping-Bibliothek, die typsichere Preg_*-Ersetzungen bietet.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/composer/semver">Komponist/Semver</a>
    </td>
    <td>Bibliothek</td>
    <td>Server-Bibliothek, die Dienstprogramme, das Analysieren von Versionsbeschränkungen und die Validierung bietet.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/composer/spdx-licenses">composer/spdx-licenses</a>
    </td>
    <td>Bibliothek</td>
    <td>SPDX-Lizenzliste und Validierungsbibliothek.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/composer/xdebug-handler">composer/xdebug-handler</a>
    </td>
    <td>Bibliothek</td>
    <td>Startet einen Prozess ohne Xdebug neu.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/doctrine/lexer">Doktrin/Lexer</a>
    </td>
    <td>Bibliothek</td>
    <td>PHP Doctrine Lexer Parser-Bibliothek, die in rekursiven Top-Down-Parsern verwendet werden kann.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/egulias/EmailValidator">egulias/email-validator</a>
    </td>
    <td>Bibliothek</td>
    <td>Eine Bibliothek zum Validieren von E-Mails mit mehreren RFCs</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/elastic/elastic-transport-php">Elastisch/Transport</a>
    </td>
    <td>Bibliothek</td>
    <td>HTTP-Transport-PHP-Bibliothek für Elastic-Produkte</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/elastic/elasticsearch-php">elasticsearch/elasticsearch</a>
    </td>
    <td>Bibliothek</td>
    <td>PHP-Client für Elasticsearch</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/endroid/qr-code">endroid/qr-code</a>
    </td>
    <td>Bibliothek</td>
    <td>Endroid-QR-Code</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/ezimuel/guzzlestreams">ezimuel/guzzlestreams</a>
    </td>
    <td>Bibliothek</td>
    <td>Abspaltung von Guzzle/Streams (aufgegeben) zur Verwendung mit Elasticsearch-php</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/ezimuel/ringphp">ezimuel/ringphp</a>
    </td>
    <td>Bibliothek</td>
    <td>Abspaltung von guzzle/RingPHP (aufgegeben) zur Verwendung mit elasticsearch-php</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/guzzle/guzzle">guzzlehttp/guzzle</a>
    </td>
    <td>Bibliothek</td>
    <td>Guzzle ist eine PHP HTTP Client-Bibliothek</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/guzzle/promises">guzzlehttp/promises</a>
    </td>
    <td>Bibliothek</td>
    <td>Guzzle-Versprechensbibliothek</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/guzzle/psr7">guzzlehttp/psr7</a>
    </td>
    <td>Bibliothek</td>
    <td>PSR-7-Nachrichtenimplementierung, die auch gängige Dienstprogrammmethoden bereitstellt</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/jsonrainbow/json-schema">JustInRainbow/JSON-Schema</a>
    </td>
    <td>Bibliothek</td>
    <td>Eine Bibliothek zum Überprüfen eines JSON-Schemas.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/thephpleague/flysystem">League/Flysystem</a>
    </td>
    <td>Bibliothek</td>
    <td>Dateispeicherabstraktion für PHP</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/thephpleague/flysystem-aws-s3-v3">League/Flysystem-AWS-S3-V3</a>
    </td>
    <td>Bibliothek</td>
    <td>AWS S3-Dateisystemadapter für Flysystem.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/thephpleague/flysystem-local">League/Flysystem-local</a>
    </td>
    <td>Bibliothek</td>
    <td>Lokaler Dateisystemadapter für Flysystem.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/thephpleague/mime-type-detection">League/MIME-Typ-Erkennung</a>
    </td>
    <td>Bibliothek</td>
    <td>MIME-Erkennung für Flysystem</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/Seldaek/monolog">monolog/monolog</a>
    </td>
    <td>Bibliothek</td>
    <td>Sendet Ihre Protokolle an Dateien, Sockets, Posteingänge, Datenbanken und verschiedene Web-Services</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/jmespath/jmespath.php">mtdowling/jmespath.php</a>
    </td>
    <td>Bibliothek</td>
    <td>Deklarativ angeben, wie Elemente aus einem JSON-Dokument extrahiert werden sollen</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/paragonie/constant_time_encoding">paragonie/constant_time_encoding</a>
    </td>
    <td>Bibliothek</td>
    <td>Implementierungen der RFC-4648-Codierung in konstanten Zeiten (Base-64, Base-32, Base-16)</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/paragonie/random_compat">paragonie/random_compat</a>
    </td>
    <td>Bibliothek</td>
    <td>PHP 5.x Polyfill für random_bytes() und random_int() von PHP 7</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/MyIntervals/emogrifier">pelago/emogrifier</a>
    </td>
    <td>Bibliothek</td>
    <td>Konvertiert CSS-Stile in HTML-Code in Inline-Stilattribute</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/php-http/discovery">php-http/discovery</a>
    </td>
    <td>Composer-Plug-in</td>
    <td>Findet und installiert PSR-7-, PSR-17-, PSR-18- und HTTPlug-Implementierungen</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/php-http/httplug">php-http/httplug</a>
    </td>
    <td>Bibliothek</td>
    <td>HTTPlug, die HTTP-Client-Abstraktion für PHP</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/php-http/promise">PHP-HTTP/Promise</a>
    </td>
    <td>Bibliothek</td>
    <td>Promise für asynchrone HTTP-Anfragen</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/PhpGt/CssXPath">phpgt/cssxpath</a>
    </td>
    <td>Bibliothek</td>
    <td>Konvertieren von CSS-Selektoren in XPath-Abfragen.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/PhpGt/Dom">phpgt/dom</a>
    </td>
    <td>Bibliothek</td>
    <td>Moderne DOM-API.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/PhpGt/PropFunc">phpgt/propfunc</a>
    </td>
    <td>Bibliothek</td>
    <td>Eigenschaftenaccessor- und -mutatorfunktionen.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/phpseclib/mcrypt_compat">phpseclib/mcrypt_compat</a>
    </td>
    <td>Bibliothek</td>
    <td>PHP 5.x-8.x Polyfill für mcrypt Erweiterung</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/phpseclib/phpseclib">phpseclib/phpseclib</a>
    </td>
    <td>Bibliothek</td>
    <td>PHP Secure Communications Library - Pure-PHP-Implementierungen von RSA, AES, SSH2, SFTP, X.509 etc.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/php-fig/cache">PSR/Cache</a>
    </td>
    <td>Bibliothek</td>
    <td>Allgemeine Schnittstelle zum Zwischenspeichern von Bibliotheken</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/php-fig/clock">PSR/CLOCK</a>
    </td>
    <td>Bibliothek</td>
    <td>Gemeinsame Schnittstelle zum Lesen der Uhr.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/php-fig/container">PSR/Container</a>
    </td>
    <td>Bibliothek</td>
    <td>Common Container Interface (PHP-Abb. PSR-11)</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/php-fig/event-dispatcher">PSR/event-dispatcher</a>
    </td>
    <td>Bibliothek</td>
    <td>Standardschnittstellen für die Ereignisbehandlung.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/php-fig/http-client">PSR/HTTP-Client</a>
    </td>
    <td>Bibliothek</td>
    <td>Gemeinsame Schnittstelle für HTTP-Clients</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/php-fig/http-factory">PSR/HTTP-Factory</a>
    </td>
    <td>Bibliothek</td>
    <td>PSR-17: Gemeinsame Schnittstellen für PSR-7-HTTP-Nachrichten-Factories</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/php-fig/http-message">PSR/HTTP-Nachricht</a>
    </td>
    <td>Bibliothek</td>
    <td>Gemeinsame Schnittstelle für HTTP-Nachrichten</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/php-fig/log">PSR/LOG</a>
    </td>
    <td>Bibliothek</td>
    <td>Allgemeine Benutzeroberfläche für die Protokollierung von Bibliotheken</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/ralouphie/getallheaders">ralouphie/getAllHeaders</a>
    </td>
    <td>Bibliothek</td>
    <td>Ein Polyfill für getAllHeaders.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/ramsey/collection">Ramsey/Collection</a>
    </td>
    <td>Bibliothek</td>
    <td>Eine PHP-Bibliothek zur Darstellung und Bearbeitung von Sammlungen.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/ramsey/uuid">Ramsey/UUID</a>
    </td>
    <td>Bibliothek</td>
    <td>Eine PHP-Bibliothek zum Generieren und Verwenden von Universally Unique Identifiers (UUIDs).</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/reactphp/promise">React/Promise</a>
    </td>
    <td>Bibliothek</td>
    <td>Eine einfache Implementierung von CommonJS Promises/A für PHP</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/MyIntervals/PHP-CSS-Parser">sabberworm/php-css-parser</a>
    </td>
    <td>Bibliothek</td>
    <td>Parser für in PHP geschriebene CSS-Dateien</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/Seldaek/jsonlint">seld/jsonlint</a>
    </td>
    <td>Bibliothek</td>
    <td>JSON-Linter</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/Seldaek/phar-utils">seld/phar-utils</a>
    </td>
    <td>Bibliothek</td>
    <td>PHAR-Dateiformat-Dienstprogramme, für den Fall, dass PHP Sie startet</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/Seldaek/signal-handler">SELD/Signal-Handler</a>
    </td>
    <td>Bibliothek</td>
    <td>Einfacher Unix-Signal-Handler, der im Hintergrund ausfällt, wenn Signale nicht unterstützt werden, um eine einfache plattformübergreifende Entwicklung zu ermöglichen</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/Spomky-Labs/aes-key-wrap">spomky-labs/aes-key-wrap</a>
    </td>
    <td>Bibliothek</td>
    <td>AES Key Wrap für PHP.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/Spomky-Labs/otphp">spomky-labs/otphp</a>
    </td>
    <td>Bibliothek</td>
    <td>Eine PHP-Bibliothek zur Erzeugung von Einmalkennwörtern nach RFC 4226 (HOTP-Algorithmus) und RFC 6238 (TOTP-Algorithmus), die mit dem Google Authenticator kompatibel sind</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/Spomky-Labs/pki-framework">spomky-labs/pki-framework</a>
    </td>
    <td>Bibliothek</td>
    <td>Ein PHP-Framework für die Verwaltung von Public-Key-Infrastrukturen. Sie umfasst X.509-Zertifikate mit öffentlichem Schlüssel, Attributzertifikate, Zertifizierungsanfragen und die Validierung des Zertifizierungspfads.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/config">symfony/config</a>
    </td>
    <td>Bibliothek</td>
    <td>Hilft Ihnen beim Suchen, Laden, Kombinieren, automatischen Ausfüllen und Überprüfen von Konfigurationswerten jeglicher Art</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/console">symfony/console</a>
    </td>
    <td>Bibliothek</td>
    <td>Erleichtert die Erstellung von schönen und testbaren Befehlszeilenschnittstellen</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/css-selector">symfony/css-selector</a>
    </td>
    <td>Bibliothek</td>
    <td>Konvertiert CSS-Selektoren in XPath-Ausdrücke</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/dependency-injection">symfony/dependency-jection</a>
    </td>
    <td>Bibliothek</td>
    <td>Ermöglicht die Standardisierung und Zentralisierung der Objekterstellung in der Anwendung</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/deprecation-contracts">Symfony/Deprecation-Contracts</a>
    </td>
    <td>Bibliothek</td>
    <td>Eine generische Funktion und Konvention für Hinweise zum Verwerfen von Triggern</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/error-handler">symfony/error-handler</a>
    </td>
    <td>Bibliothek</td>
    <td>Bietet Tools zur Fehlerverwaltung und einfacheren Fehlerbehebung in PHP-Code</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/event-dispatcher">symfony/event-dispatcher</a>
    </td>
    <td>Bibliothek</td>
    <td>Stellt Tools bereit, mit denen Ihre Anwendungskomponenten miteinander kommunizieren können, indem Ereignisse gesendet und überwacht werden</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/event-dispatcher-contracts">symfony/event-dispatcher-Contracts</a>
    </td>
    <td>Bibliothek</td>
    <td>Allgemeine Abstraktionen im Zusammenhang mit dem Dispatching-Ereignis</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/filesystem">symfony/filesystem</a>
    </td>
    <td>Bibliothek</td>
    <td>Stellt grundlegende Dienstprogramme für das Dateisystem bereit</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/finder">symfony/finder</a>
    </td>
    <td>Bibliothek</td>
    <td>Findet Dateien und Verzeichnisse über eine intuitive, flüssige Oberfläche</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/http-client">symfony/http-client</a>
    </td>
    <td>Bibliothek</td>
    <td>Bietet leistungsstarke Methoden zum synchronen oder asynchronen Abrufen von HTTP-Ressourcen</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/http-client-contracts">symfony/http-client-Contracts</a>
    </td>
    <td>Bibliothek</td>
    <td>Allgemeine Abstraktionen in Bezug auf HTTP-Clients</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/http-foundation">symfony/http-foundation</a>
    </td>
    <td>Bibliothek</td>
    <td>Definiert eine objektorientierte Ebene für die HTTP-Spezifikation</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/http-kernel">symfony/http-kernel</a>
    </td>
    <td>Bibliothek</td>
    <td>Stellt einen strukturierten Prozess zum Konvertieren einer Anfrage in eine Antwort bereit</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/intl">symfony/intl</a>
    </td>
    <td>Bibliothek</td>
    <td>Ermöglicht den Zugriff auf die Lokalisierungsdaten der ICU-Bibliothek</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/mailer">symfony/mailer</a>
    </td>
    <td>Bibliothek</td>
    <td>Hilft beim Senden von E-Mails</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/mime">symfony/mime</a>
    </td>
    <td>Bibliothek</td>
    <td>Ermöglicht die Bearbeitung von MIME-Nachrichten</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/polyfill-ctype">symfony/polyfill-ctype</a>
    </td>
    <td>Bibliothek</td>
    <td>Symfony Polyfill für ctype-Funktionen</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/polyfill-intl-grapheme">symfony/polyfill-intl-grapheme</a>
    </td>
    <td>Bibliothek</td>
    <td>Symfony Polyfill für intl's grapheme_* Funktionen</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/polyfill-intl-idn">symfony/polyfill-intl-idn</a>
    </td>
    <td>Bibliothek</td>
    <td>Symfony Polyfill für die Funktionen „idn_to_ascii“ und „idn_to_utf8“ von Intl</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/polyfill-intl-normalizer">symfony/polyfill-intl-normalizer</a>
    </td>
    <td>Bibliothek</td>
    <td>Symfony Polyfill für Intl's Normalizer-Klasse und zugehörige Funktionen</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/polyfill-mbstring">symfony/polyfill-mbstring</a>
    </td>
    <td>Bibliothek</td>
    <td>Symfony Polyfill für die MBstring-Erweiterung</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/polyfill-php73">symfony/polyfill-php73</a>
    </td>
    <td>Bibliothek</td>
    <td>Symfony Polyfill unterstützt einige PHP 7.3+ Funktionen zur Reduzierung von PHP-Versionen</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/polyfill-php80">symfony/polyfill-php80</a>
    </td>
    <td>Bibliothek</td>
    <td>Symfony Polyfill unterstützt einige PHP 8.0+ Funktionen zur Reduzierung von PHP-Versionen</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/polyfill-php81">symfony/polyfill-php81</a>
    </td>
    <td>Bibliothek</td>
    <td>Symfony Polyfill unterstützt einige PHP 8.1+ Funktionen zur Reduzierung von PHP-Versionen</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/polyfill-php82">symfony/polyfill-php82</a>
    </td>
    <td>Bibliothek</td>
    <td>Symfony Polyfill unterstützt einige PHP 8.2+-Funktionen zur Reduzierung von PHP-Versionen</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/polyfill-php83">symfony/polyfill-php83</a>
    </td>
    <td>Bibliothek</td>
    <td>Symfony Polyfill unterstützt einige PHP 8.3+ Funktionen zu niedrigeren PHP-Versionen</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/process">symfony/process</a>
    </td>
    <td>Bibliothek</td>
    <td>Führt Befehle in Teilprozessen aus</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/service-contracts">symfony/service-Contracts</a>
    </td>
    <td>Bibliothek</td>
    <td>Allgemeine Abstraktionen im Zusammenhang mit Schreibdiensten</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/string">symfony/string</a>
    </td>
    <td>Bibliothek</td>
    <td>Bietet eine objektorientierte API für Zeichenfolgen und verarbeitet Bytes, UTF-8-Code-Punkte und Graphem-Cluster einheitlich</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/var-dumper">symfony/var-dumper</a>
    </td>
    <td>Bibliothek</td>
    <td>Stellt Mechanismen bereit, um beliebige PHP-Variablen zu durchlaufen</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/var-exporter">symfony/var-Exporter</a>
    </td>
    <td>Bibliothek</td>
    <td>Ermöglicht den Export jeder serialisierbaren PHP-Datenstruktur in reinen PHP-Code</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/yaml">symfony/yaml</a>
    </td>
    <td>Bibliothek</td>
    <td>Lädt YAML-Dateien und gibt deren Speicherinhalt aus</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/web-token/jwt-framework">Web-Token/JWT-Framework</a>
    </td>
    <td>symfony-bundle</td>
    <td>JSON Object Signing and Encryption Library für PHP und Symfony Bundle.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/webonyx/graphql-php">webonyx/graphql-php</a>
    </td>
    <td>Bibliothek</td>
    <td>Ein PHP-Port der GraphQL-Referenzimplementierung</td>
  </tr>
  </tbody>
</table>

### OSL-3.0, AFL-3.0

<table>
  <thead>
    <tr>
      <th>-Name</th>
      <th>Typ</th>
      <th>Beschreibung</th>
    </tr>
  </thead>
  <tbody>
  <tr>
    <td>
      paypal/module-braintree-customer-balance
    </td>
    <td>Magento2-module</td>
    <td>Nicht zutreffend</td>
  </tr>
  <tr>
    <td>
      paypal/module-braintree-gift-card
    </td>
    <td>Magento2-module</td>
    <td>Nicht zutreffend</td>
  </tr>
  <tr>
    <td>
      paypal/module-braintree-gift-card-account
    </td>
    <td>Magento2-module</td>
    <td>Nicht zutreffend</td>
  </tr>
  <tr>
    <td>
      paypal/module-braintree-gift-wrapping
    </td>
    <td>Magento2-module</td>
    <td>Nicht zutreffend</td>
  </tr>
  <tr>
    <td>
      paypal/module-braintree-graph-ql
    </td>
    <td>Magento2-module</td>
    <td>Nicht zutreffend</td>
  </tr>
  <tr>
    <td>
      PayPal/Modul-Braintree-Belohnung
    </td>
    <td>Magento2-module</td>
    <td>Nicht zutreffend</td>
  </tr>
  </tbody>
</table>

### OSL-3.0

<table>
  <thead>
    <tr>
      <th>-Name</th>
      <th>Typ</th>
      <th>Beschreibung</th>
    </tr>
  </thead>
  <tbody>
  </tbody>
</table>

### PHP

<table>
  <thead>
    <tr>
      <th>-Name</th>
      <th>Typ</th>
      <th>Beschreibung</th>
    </tr>
  </thead>
  <tbody>
  <tr>
    <td>
      <a href="https://github.com/2tvenom/CBOREncode">2tvenom/cborencode</a>
    </td>
    <td>Bibliothek</td>
    <td>CBOR-Encoder für PHP</td>
  </tr>
  </tbody>
</table>

### proprietär

<table>
  <thead>
    <tr>
      <th>-Name</th>
      <th>Typ</th>
      <th>Beschreibung</th>
    </tr>
  </thead>
  <tbody>
  </tbody>
</table>

### geschützt

<table>
  <thead>
    <tr>
      <th>-Name</th>
      <th>Typ</th>
      <th>Beschreibung</th>
    </tr>
  </thead>
  <tbody>
  <tr>
    <td>
      paypal/module-braintree-core
    </td>
    <td>Magento2-module</td>
    <td>Verzweigung aus dem Magento Braintree 2.2.0 Modul von Gene Commerce für PayPal.</td>
  </tr>
  </tbody>
</table>
