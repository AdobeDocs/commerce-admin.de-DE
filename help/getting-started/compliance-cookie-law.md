---
title: Einhaltung von Cookie-Rechtsvorschriften
description: Um mit den Rechtsvorschriften in vielen Ländern in Bezug auf die Verwendung von Cookies Schritt zu halten, bieten Adobe Commerce und Magento Open Source den Händlern die Möglichkeit, die Zustimmung des Kunden einzuholen.
exl-id: 42df20cd-50a7-4618-98fd-9ced936e305b
feature: Compliance
source-git-commit: ae43d97bb3031a06ce6a0211ee304aae53e4eb08
workflow-type: tm+mt
source-wordcount: '2105'
ht-degree: 0%

---

# Einhaltung von Cookie-Rechtsvorschriften

Cookies sind kleine Dateien, die auf dem Computer jedes Besuchers Ihrer Site gespeichert und als temporäre Speicherorte für Informationen verwendet werden. Informationen, die in Cookies gespeichert werden, werden verwendet, um das Einkaufserlebnis zu personalisieren, Besucher mit ihrem Warenkorb zu verknüpfen, Traffic-Muster zu messen und die Effektivität von Promotions zu verbessern. Um mit den Rechtsvorschriften in vielen Ländern in Bezug auf die Verwendung von Cookies Schritt zu halten, bieten Adobe Commerce und Magento Open Source den Händlern die Möglichkeit, die Zustimmung des Kunden einzuholen. Eine Liste der Standard-Cookies in Adobe Commerce und Magento Open Source finden Sie in der [Cookie-Referenz](#default-cookies).

>[!NOTE]
>
>Wenn Sie die standardmäßigen [Datenschutzeinstellungen von Google](../merchandising-promotions/google-tools.md#google-privacy-settings) ändern, um die [Datenschutz-Grundverordnung](compliance-gdpr.md) einzuhalten, ist es nicht erforderlich, die Benutzerzustimmung für die Verwendung von Google Analytics-Cookies einzuholen.

## Methode 1: Implizite Zustimmung

Das implizite Einverständnis bedeutet, dass Besucher Ihres Stores klar verstehen, dass Cookies ein notwendiger Bestandteil der Vorgänge sind, und dass sie durch die Verwendung Ihrer Site indirekt die Berechtigung zur Verwendung erteilt haben. Der Schlüssel zum Erlangen einer impliziten Zustimmung besteht darin, genügend Informationen bereitzustellen, damit ein Besucher eine fundierte Entscheidung treffen kann. Viele Stores zeigen oben auf allen Standardseiten eine Meldung an, die einen kurzen Überblick über die Verwendung von Cookies bietet und einen Link zur Datenschutzrichtlinie des Stores enthält. In der Datenschutzrichtlinie sollte beschrieben werden, welche Art von Informationen Ihr Store erfasst und wie sie verwendet werden.

## Methode 2: Einverständniserklärung

Wenn Sie Ihren Store im _Cookie-Einschränkungsmodus_ betreiben, müssen Besucher ihre Zustimmung erteilen, bevor Cookies auf ihren Computern gespeichert werden können. Sofern die Zustimmung nicht erteilt wurde, sind viele Funktionen Ihres Stores nicht verfügbar. Wenn beispielsweise Google Analytics für Ihren Store verfügbar sind, kann sie erst aufgerufen werden, nachdem der Besucher die Verwendung von Cookies genehmigt hat.

## Cookie-Einschränkungsmodus

Wenn der Cookie-Einschränkungsmodus aktiviert ist, werden Besucher in Ihrem Store darüber informiert, dass Cookies für Vorgänge mit vollem Funktionsumfang erforderlich sind. Je nach Design kann die Nachricht über der Kopfzeile, unter der Fußzeile oder an einer anderen Stelle auf der Seite angezeigt werden. Die Nachricht enthält einen Link zu Ihrer Datenschutzrichtlinie für weitere Informationen und ermutigt Besucher, auf die Schaltfläche Zulassen zu klicken, um die Zustimmung zu erteilen. Nachdem die Einwilligung erteilt wurde, verschwindet die Nachricht.

Ihre [Datenschutzrichtlinien](privacy-policy.md)) sollten den Namen Ihres Stores und die Kontaktinformationen enthalten und den Zweck jedes Cookies erläutern, das von Ihrem Store verwendet wird. Weitere Informationen finden Sie unter [Cookie-Referenz](#default-cookies).

>[!NOTE]
>
>Wenn Sie den URL-Schlüssel der Datenschutzrichtlinie ändern, müssen Sie auch eine benutzerdefinierte URL-Umschreibung erstellen, um den Traffic zum neuen URL-Schlüssel umzuleiten. Andernfalls gibt der Link in der Meldung &quot;Cookie-Einschränkungsmodus&quot;den Wert `404 Page Not Found` zurück.

![Beispiel-Storefront - Hinweis zur Cookie-Einschränkung](./assets/storefront-cookie-restriction-message.png){width="600"}

### Schritt 1: Aktivieren des Cookie-Einschränkungsmodus

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Wählen Sie im linken Navigationsbereich unter **[!UICONTROL General]** die Option **[!UICONTROL Web]**.

1. Erweitern Sie den Abschnitt **[!UICONTROL Default Cookie Settings]** und führen Sie die folgenden Schritte aus:

   ![Webkonfiguration - standardmäßige Cookie-Einstellungen](./assets/web-default-cookie-settings.png){width="600"}

   - Geben Sie den Wert **[!UICONTROL Cookie Lifetime]** in Sekunden ein.

   - Wenn Sie Cookies für andere Ordner verfügbar machen möchten, geben Sie den Wert **[!UICONTROL Cookie Path]** ein. Um die Cookies überall auf der Site verfügbar zu machen, geben Sie einen Schrägstrich (`/`) ein. Dieser Wert kann nur den Cookie-Pfad enthalten und **_kann_** keine anderen Cookie-Parameter enthalten.

   - Um die Cookies für eine Subdomain verfügbar zu machen, geben Sie den Namen der Subdomain in das Feld **[!UICONTROL Cookie Domain]** (`subdomain.yourdomain.com`) ein. Um Cookies für alle Subdomains verfügbar zu machen, geben Sie den Domänennamen gefolgt von einem Punkt (`.yourdomain.com`) ein. Dieser Wert kann nur die Cookie-Domäne enthalten und **_kann_** keine anderen Cookie-Parameter enthalten.

   - Um zu verhindern, dass Skriptsprachen wie JavaScript Zugriff auf Cookies erhalten, stellen Sie sicher, dass **Nur HTTP verwenden** auf `Yes` gesetzt ist.

   - Setzen Sie **[!UICONTROL Cookie Restriction Mode]** auf `Yes`.

     Deaktivieren Sie bei Bedarf das Kontrollkästchen und klicken Sie auf **[!UICONTROL OK]** , um den Perimeterwechsel zu bestätigen.

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save Config]**.

1. Wenn Sie aufgefordert werden, den Cache zu aktualisieren, klicken Sie in der Systemmeldung auf den Link **[!UICONTROL Cache Management]** . Aktualisieren Sie dann jeden ungültigen Cache.

### Schritt 2: Datenschutzrichtlinie aktualisieren

Aktualisieren Sie Ihre [Datenschutzrichtlinie](privacy-policy.md), sodass sie die von Ihrem Unternehmen erfassten Informationen und deren Verwendung widerspiegelt.

## Standard-Cookies

Die Standard-Cookies in Adobe Commerce und Magento Open Source werden als ausnahmsweise/nicht befreit klassifiziert, damit Händler die Anforderungen von Datenschutzbestimmungen wie der [DSGVO](compliance-gdpr.md) erfüllen können. Händler sollten diese Informationen als Anleitung verwenden und sich mit Rechtsberatern beraten, um ihre Datenschutz- und Cookie-Richtlinien im Rahmen einer umfassenden Strategie zur Einhaltung von Datenschutzbestimmungen zu aktualisieren.

Die folgenden Cookies werden von [!DNL Commerce] &quot;vorkonfiguriert&quot;für On-Premise- und Cloud-Installationen verwendet. Diese Cookies können durch Funktionen erforderlich sein, die vom Kunden ausdrücklich angefordert werden. Weitere Informationen zur Lebensdauer von Sitzungs-Cookies finden Sie unter [Sitzungslebensdauer](../customers/customer-online-options.md).

Einige dieser Cookies bieten Konfigurationsoptionen, einschließlich der Aktivierung/Deaktivierung nach Bedarf.

### Angeforderte Funktions-Cookies (ausgenommen)


#### `add_to_cart`

![Adobe Commerce](../assets/adobe-logo.svg) (nur Adobe Commerce) Wird vom Google Tag-Manager verwendet. Erfasst die Produkt-SKU, den Namen, den Preis und die Menge, die aus dem Warenkorb entfernt wurden, und stellt die Informationen für die zukünftige Integration durch Skripte von Drittanbietern zur Verfügung.

#### `guest-view`

Speichert die Bestell-ID, die Gastkäufer zum Abrufen ihres Bestellstatus verwenden. Ansicht der Gastbestellungen. Wird in _[!DNL Orders and Returns]_-Widgets verwendet.

- Ist sicher? Nein
- Nur HTTP: Ja
- Ablaufrichtlinie: Sitzung
- Modul: `Magento_Sales`

#### `login_redirect`

Behält die Zielseite bei, die geladen wurde, bevor der Kunde zum Anmelden angewiesen wurde. Eine Login-Umleitung wird mit dem Mini-Warenkorb für angemeldete Kunden verwendet, wenn die Konfigurationsoption [Mini-Warenkorb anzeigen](../stores-purchase/cart-configuration.md#mini-cart) auf `Yes` eingestellt ist.

- Ist sicher? Nein
- Nur HTTP: Nein
- Ablaufrichtlinie: Sitzung
- Modul: `Magento_Customer`

#### `mage-banners-cache-storage`

![Adobe Commerce](../assets/adobe-logo.svg) (nur Adobe Commerce) Speichert Bannerinhalte lokal, um die Leistung zu verbessern.

#### `mage-messages`

Verfolgt Fehlermeldungen und andere dem Benutzer angezeigte Benachrichtigungen, z. B. die Zustimmungsmeldung für Cookies und verschiedene Fehlermeldungen. Die Nachricht wird aus dem Cookie gelöscht, nachdem sie dem Käufer angezeigt wurde.

Es gibt keine Option, dieses Cookie zu deaktivieren.

- Ist sicher? Nein
- Nur HTTP: Nein
- Ablaufrichtlinie: Dauer 1 Jahr. Wird am Frontend gelöscht, wenn die Nachricht dem Benutzer angezeigt wird.
- Modul: `Magento_Theme`

#### `mage-translation-storage` (lokaler Speicher)

Speichert übersetzte Inhalte auf Anforderung des Käufers. Wird verwendet, wenn [Übersetzungsstrategie](../configuration-reference/advanced/developer.md) als &quot;Wörterbuch (Übersetzung auf Storefront-Seite)&quot;konfiguriert ist.

- Ist sicher? Nein
- Nur HTTP: Nein
- Ablaufrichtlinie: Nach lokalen Speicherregeln
- Modul: `Magento_Translation`

#### `mage-translation-file-version` (lokaler Speicher)

Verfolgt die Version der Übersetzungen im lokalen Speicher. Wird verwendet, wenn [Übersetzungsstrategie](../configuration-reference/advanced/developer.md) als `Dictionary (Translation on Storefront side)` konfiguriert ist.

- Ist sicher? Nein
- Nur HTTP: Nein
- Ablaufrichtlinie: Nach lokalen Speicherregeln
- Modul: `Magento_Translation`

#### `product_data_storage` (lokaler Speicher)

Speichert die Konfiguration für Produktdaten zu kürzlich angezeigten/vergleichbaren Produkten.

- Ist sicher? Nein
- Nur HTTP: Nein
- Ablaufrichtlinie: Nach lokalen Speicherregeln
- Modul: `Magento_Catalog`

#### `recently_compared_product` (lokaler Speicher)

Speichert Produkt-IDs von kürzlich verglichenen Produkten.

- Ist sicher? Nein
- Nur HTTP: Nein
- Ablaufrichtlinie: Nach lokalen Speicherregeln
- Modul: `Magento_Catalog`

#### `recently_compared_product_previous` (lokaler Speicher)

Speichert Produkt-IDs von zuvor verglichenen Produkten zur einfachen Navigation.

- Ist sicher? Nein
- Nur HTTP: Nein
- Ablaufrichtlinie: Nach lokalen Speicherregeln
- Modul: `Magento_Catalog`

#### `recently_viewed_product` (lokaler Speicher)

Speichert Produkt-IDs kürzlich angesehener Produkte zur einfachen Navigation.

- Ist sicher? Nein
- Nur HTTP: Nein
- Ablaufrichtlinie: Nach lokalen Speicherregeln
- Modul: `Magento_Catalog`

#### `recently_viewed_product_previous` (lokaler Speicher)

Speichert Produkt-IDs von kürzlich angezeigten Produkten zur einfachen Navigation.

- Ist sicher? Nein
- Nur HTTP: Nein
- Ablaufrichtlinie: Nach lokalen Speicherregeln
- Modul: `Magento_Catalog`

#### `remove_from_cart`

![Adobe Commerce](../assets/adobe-logo.svg) (nur Adobe Commerce), verwendet von [Google Tag Manager](../merchandising-promotions/google-tag-manager.md). Erfasst die Produkt-SKU, den Namen, den Preis und die Menge, die dem Warenkorb hinzugefügt werden, und stellt die Informationen für die zukünftige Integration durch Skripte von Drittanbietern zur Verfügung.

#### `stf`

Zeichnet die Zeit auf, zu der Nachrichten vom Modul SendFriend ([E-Mail an einen Freund](../stores-purchase/email-a-friend.md)) gesendet werden.

- Ist sicher? Ja
- Nur HTTP: Ja
- Ablaufrichtlinie: Sitzung
- Modul: `Magento_SendFriend`

#### `X-Magento-Vary`

Konfigurationseinstellung, die die Leistung bei Verwendung der Zwischenspeicherung von statischen Inhalten mit varianten Werten verbessert.

- Ist sicher? Ja
- Nur HTTP: Ja
- Ablaufrichtlinie: Basiert auf PHP-Einstellung session.cookie_lifetime
- Modul: `Magento_PageCache`

#### `form_key`

Eine Sicherheitsmaßnahme, die eine zufällige Zeichenfolge an alle Formularübermittlungen anhängt, um die Daten vor Cross-Site Request Forgery (CSRF) zu schützen.

- Ist sicher? Nein
- Nur HTTP: Nein
- Ablaufrichtlinie:
   - PHP: Basiert auf der PHP-Einstellung session.cookie_lifetime
   - JS: Sitzung
- Modul: Seiten-Cache

#### `mage-cache-sessid`

Der Wert dieses Cookies Trigger die Bereinigung des lokalen Cache-Speichers. Wenn das Cookie vom Backend-Programm entfernt wird, löscht der Administrator den lokalen Speicher und setzt den Cookie-Wert auf `true`.

- Ist sicher? Nein
- Nur HTTP: Nein
- Ablaufrichtlinie: Sitzung
- Modul: `Magento_Customer`

#### `mage-cache-storage`

Lokaler Speicher besucherspezifischer Inhalte, die E-Commerce-Funktionen ermöglichen.

- Ist sicher? Nein
- Nur HTTP: Nein
- Ablaufrichtlinie: Sitzung
- Modul: `Magento_Customer`, `Magento_Persistent`

#### `mage-cache-storage` (lokaler Speicher)

Lokaler Speicher besucherspezifischer Inhalte, die E-Commerce-Funktionen ermöglichen.

- Ist sicher? Nein
- Nur HTTP: Nein
- Ablaufrichtlinie: Sitzung
- Modul: `Magento_Customer`, `Magento_Persistent`, `Magento_NegotiableQuote`

#### `mage-cache-storage-section-invalidation` (lokaler Speicher)

Erzwingt die lokale Speicherung bestimmter Inhaltsabschnitte, die ungültig gemacht werden sollen.

- Ist sicher? Nein
- Nur HTTP: Nein
- Ablaufrichtlinie: Pro lokalem Speicher
- Modul: `Magento_Customer`

#### `persistent_shopping_cart`

Speichert den Schlüssel (ID) des beständigen Warenkorbs, um die Wiederherstellung des Warenkorbs für einen anonymen Käufer zu ermöglichen.

- Ist sicher? Ja
- Nur HTTP: Ja
- Ablaufrichtlinie: basierend auf der Konfiguration [Persistenter Warenkorb](../stores-purchase/cart-persistent.md) - Persistenz-Lebensdauer (Sekunden)
- Modul: `Magento_Persistent`

#### `private_content_version`

Hängt eine zufällige, eindeutige Nummer und Uhrzeit an Seiten mit Kundeninhalt an, um zu verhindern, dass diese auf dem Server zwischengespeichert werden.

Es wird an mehreren Stellen festgelegt: in PHP, in JavaScript als Cookie und in JavaScript zum lokalen Speicher.

Für HTTP Only=`Yes` (basierend auf Anfrage) bedeutet dies, dass das Cookie sicher ist, wenn es während der HTTPS-Anforderung gesetzt wird, und nicht sicher, wenn es während der HTTP-Anforderung gesetzt wird.

- Ist sicher? `Yes` (je nach Anforderung), `No`
- Nur HTTP: `No`
- Ablaufrichtlinie: basierend auf der Konfiguration [Persistenter Warenkorb](../stores-purchase/cart-persistent.md) - Persistenz-Lebensdauer (Sekunden)
   - PHP: `1` Jahr / `315360000s` (zehn Jahre)
   - JS: `1` Tag
   - JS-lokaler Speicher: Pro lokalen Speicherregeln (für immer)
- Modul: `Magento_PageCache`, `Magento_Customer`

#### `section_data_ids`

Speichert kundenspezifische Informationen zu von Käufern initiierten Aktionen, z. B. Anzeige der Wunschliste und Checkout-Informationen.

- Ist sicher? `No`
- Nur HTTP: `No`
- Ablaufrichtlinie: `Session`
- Modul: `Magento_Customer`

#### `store`

Verfolgt die vom Käufer ausgewählte Store-Ansicht/Gebietsschema.

- Ist sicher? `No`
- Nur HTTP: `Yes`
- Ablaufrichtlinie: `1` Jahr
- Modul: `Magento_Store`

#### `mage-banners-cache-storage` - lokaler Speicher

![Adobe Commerce](../assets/adobe-logo.svg) (nur Adobe Commerce) Lokaler Speicher für Bannerfunktionen.

- Ist sicher? `No`
- Nur HTTP: `No`
- Ablaufrichtlinie: Nach lokalen Speicherregeln
- Modul: `Magento_Banner`

## Google Analytics-Cookies

Die folgenden Cookies werden verwendet, wenn [Google Analytics](../merchandising-promotions/google-analytics.md) oder Google Universal Analytics vollständig für Ihre Installation aktiviert ist. Informationen zum Deaktivieren dieser Cookies für die Einhaltung von Datenschutzbestimmungen finden Sie unter [Google-Datenschutzeinstellungen](../merchandising-promotions/google-tools.md#google-privacy-settings). Weitere Informationen finden Sie unter [Verwendung von Google Analytics-Cookies auf Websites][1].

### Google Universal Analytics-Cookies - nicht von der Steuer befreit

![Adobe Commerce](../assets/adobe-logo.svg) (nur Adobe Commerce) JavaScript-Bibliotheken: `gtag.js` und `analytics.js`

- `_ga`: Entfernt Besucher Ihrer Site.
- `_gid`: Entfernt Besucher Ihrer Site.
- `gat`: Wird verwendet, um die Anforderungsrate zu drosseln.
- `dc_gtm_<property-id>`: Die Anforderungsrate für &quot;Titel&quot;bei der Bereitstellung von Google Analytics mit dem [Google Tag Manager](../merchandising-promotions/google-tag-manager.md).
- `AMP_TOKEN`: Enthält ein Token, das zum Abrufen einer Client-ID vom AMP Client-ID-Dienst verwendet werden kann. Andere mögliche Werte sind Opt-out, Inflight-Anfragen oder Fehler beim Abrufen einer Client-ID vom AMP-Client-ID-Dienst.
- `_gac_<property-id>`: Enthält kampagnenbezogene Informationen für den Benutzer. Google AdWords-Konversions-Tags lesen dieses Cookie, wenn Google Analytics mit Ihrem [AdWords][2] -Konto verknüpft ist.

### Google Analytics-Cookies - nicht ausgenommen

![Adobe Commerce](../assets/adobe-logo.svg) (nur Adobe Commerce) JavaScript Library: `ga.js`

- `__utma`: Unterscheidet Käufer und Sitzungen. Dieses Cookie wird erstellt, wenn die JavaScript-Bibliothek ausgeführt wird und kein `__utma` -Cookie vorhanden ist. Das Cookie wird jedes Mal aktualisiert, wenn Daten an Google Analytics gesendet werden.
- `__utmt`: Wird verwendet, um die Anforderungsrate zu drosseln.
- `__utmb`: Stellt neue Sitzungen/Besuche fest. Dieses Cookie wird erstellt, wenn die JavaScript-Bibliothek ausgeführt wird und kein `__utmb` -Cookie vorhanden ist. Das Cookie wird jedes Mal aktualisiert, wenn Daten an Google Analytics gesendet werden.
- `_utmz`: Speichert die Traffic-Quelle oder Kampagne, aus der hervorgeht, wie der Käufer zu Ihrer Site gelangt ist. Das Cookie wird bei Ausführung der JavaScript-Bibliothek erstellt und jedes Mal aktualisiert, wenn Daten an Google Analytics gesendet werden.
- `__utmv`: Speichert benutzerdefinierte Variablendaten auf Besucherebene. Dieses Cookie wird erstellt, wenn ein Entwickler die `_setCustomVar` -Methode mit einer benutzerdefinierten Variablen auf Besucherebene verwendet. Dieses Cookie wird jedes Mal aktualisiert, wenn Daten an Google Analytics gesendet werden.

## Cookies in Recommendations

![Adobe Commerce](../assets/adobe-logo.svg) (nur Adobe Commerce) Die folgenden Cookies werden von Product Recommendations für Adobe Commerce-Kunden verwendet. Diese Cookies werden mit dem [DataServices-Modul](https://experienceleague.adobe.com/docs/commerce-merchant-services/product-recommendations/getting-started/install-configure.html) installiert.

- `mg_dnt`: Ermöglicht Ihnen die [Einschränkung der Adobe Commerce-Datenerfassung](https://experienceleague.adobe.com/docs/commerce-merchant-services/product-recommendations/developer/setting-cookie.html), wenn Sie über benutzerdefinierten Code verfügen, um die Cookie-Zustimmung auf Ihrer Site zu verwalten.
- `user_allowed_save_cookie`: Wird für den [Cookie-Einschränkungsmodus](#cookie-restriction-mode) verwendet.
- `authentication_flag`: Gibt an, ob sich ein Käufer angemeldet oder abgemeldet hat. Dieses Cookie wird gleichzeitig mit dem `dataservices_customer_id` -Cookie aktualisiert.
- `dataservices_customer_id`: Gibt an, ob sich ein Käufer angemeldet oder abgemeldet hat. Dieses Cookie enthält die eindeutige ID des Kunden im System.
- `dataservices_customer_group`: Gibt die Gruppe eines Kunden an. Dieses Cookie wird als Prüfsumme [sha1](https://en.wikipedia.org/wiki/SHA-1) der Gruppen-ID des Kunden gespeichert.
- `dataservices_cart_id`: Identifiziert die Warenkorbaktionen eines Käufers. Dieses Cookie enthält die eindeutige Warenkorb-ID des Kunden im System.
- `dataservices_product_context`: Identifiziert die Produktinteraktionen eines Käufers. Dieses Cookie enthält die eindeutige Angebots-ID des Kunden im System.

## Zusätzliche Cookies

![Adobe Commerce](../assets/adobe-logo.svg) (nur Adobe Commerce) Die folgenden Cookies werden für Adobe Commerce-Kunden gesetzt. Diese Cookies werden mit dem [DataServices-Modul](https://experienceleague.adobe.com/docs/commerce-merchant-services/product-recommendations/getting-started/install-configure.html) installiert.

- `mg`: Wird durch den Snowplom-JavaScript-Tracker festgelegt. Weitere Informationen finden Sie in der Dokumentation zu [Snowplow](https://docs.snowplow.io/docs/collecting-data/collecting-from-own-applications/javascript-trackers/javascript-tracker/javascript-tracker-v3/tracker-setup/initialization-options) .
- `com.adobe.alloy.getTld`: Bei dem Hostnamen der aktuellen Webseite handelt es sich um die oberste Domäne, bei der es sich nicht um ein &quot;öffentliches Suffix&quot;handelt, wie in https://publicsuffix.org beschrieben. Im Wesentlichen ist dies die Domäne mit der höchsten Priorität, die Cookies akzeptieren kann. Dieses Cookie ist Teil des [Alloy Web SDK](https://github.com/adobe/alloy).

[1]: https://developers.google.com/analytics/devguides/collection/analyticsjs/cookie-usage
[2]: https://support.google.com/adwords/answer/7521212
