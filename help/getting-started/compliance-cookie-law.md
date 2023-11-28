---
title: Einhaltung von Cookie-Rechtsvorschriften
description: Um mit den Rechtsvorschriften in vielen Ländern in Bezug auf die Verwendung von Cookies Schritt zu halten, bieten Adobe Commerce und Magento Open Source den Händlern die Möglichkeit, die Zustimmung des Kunden einzuholen.
exl-id: 42df20cd-50a7-4618-98fd-9ced936e305b
feature: Compliance
source-git-commit: ae43d97bb3031a06ce6a0211ee304aae53e4eb08
workflow-type: tm+mt
source-wordcount: '2145'
ht-degree: 0%

---

# Einhaltung von Cookie-Rechtsvorschriften

Cookies sind kleine Dateien, die auf dem Computer jedes Besuchers Ihrer Site gespeichert und als temporäre Speicherorte für Informationen verwendet werden. Informationen, die in Cookies gespeichert werden, werden verwendet, um das Einkaufserlebnis zu personalisieren, Besucher mit ihrem Warenkorb zu verknüpfen, Traffic-Muster zu messen und die Effektivität von Promotions zu verbessern. Um mit den Rechtsvorschriften in vielen Ländern in Bezug auf die Verwendung von Cookies Schritt zu halten, bieten Adobe Commerce und Magento Open Source den Händlern die Möglichkeit, die Zustimmung des Kunden einzuholen. Eine Liste der Standard-Cookies in Adobe Commerce und Magento Open Source erhalten Sie mit der Variablen [Cookie-Referenz](#default-cookies).

>[!NOTE]
>
>Wenn Sie die Standardeinstellung [Datenschutzeinstellungen für Google](../merchandising-promotions/google-tools.md#google-privacy-settings) , um [Die Datenschutz-Grundverordnung](compliance-gdpr.md)ist es nicht erforderlich, die Zustimmung des Nutzers für die Verwendung von Google Analytics-Cookies einzuholen.

## Methode 1: Implizite Zustimmung

Das implizite Einverständnis bedeutet, dass Besucher Ihres Stores klar verstehen, dass Cookies ein notwendiger Bestandteil der Vorgänge sind, und dass sie durch die Verwendung Ihrer Site indirekt die Berechtigung zur Verwendung erteilt haben. Der Schlüssel zum Erlangen einer impliziten Zustimmung besteht darin, genügend Informationen bereitzustellen, damit ein Besucher eine fundierte Entscheidung treffen kann. Viele Stores zeigen oben auf allen Standardseiten eine Meldung an, die einen kurzen Überblick über die Verwendung von Cookies bietet und einen Link zur Datenschutzrichtlinie des Stores enthält. In der Datenschutzrichtlinie sollte beschrieben werden, welche Art von Informationen Ihr Store erfasst und wie sie verwendet werden.

## Methode 2: Einverständniserklärung

Laden in Betrieb nehmen _Cookie-Einschränkungsmodus_ verlangt von Besuchern, ihre Zustimmung zu geben, bevor Cookies auf ihren Computern gespeichert werden können. Sofern die Zustimmung nicht erteilt wurde, sind viele Funktionen Ihres Stores nicht verfügbar. Wenn beispielsweise Google Analytics für Ihren Store verfügbar sind, kann sie erst aufgerufen werden, nachdem der Besucher die Verwendung von Cookies genehmigt hat.

## Cookie-Einschränkungsmodus

Wenn der Cookie-Einschränkungsmodus aktiviert ist, werden Besucher in Ihrem Store darüber informiert, dass Cookies für Vorgänge mit vollem Funktionsumfang erforderlich sind. Je nach Design kann die Nachricht über der Kopfzeile, unter der Fußzeile oder an einer anderen Stelle auf der Seite angezeigt werden. Die Nachricht enthält einen Link zu Ihrer Datenschutzrichtlinie für weitere Informationen und ermutigt Besucher, auf die Schaltfläche Zulassen zu klicken, um die Zustimmung zu erteilen. Nachdem die Einwilligung erteilt wurde, verschwindet die Nachricht.

Ihre [Datenschutzrichtlinie](privacy-policy.md)) sollte den Namen Ihres Stores und Ihre Kontaktinformationen enthalten und den Zweck der einzelnen Cookies erklären, die von Ihrem Store verwendet werden. Weitere Informationen finden Sie unter [Cookie-Referenz](#default-cookies).

>[!NOTE]
>
>Wenn Sie den URL-Schlüssel der Datenschutzrichtlinie ändern, müssen Sie auch eine benutzerdefinierte URL-Umschreibung erstellen, um den Traffic zum neuen URL-Schlüssel umzuleiten. Andernfalls gibt der Link in der Meldung &quot;Cookie-Einschränkungsmodus&quot;zurück `404 Page Not Found`.

![Beispiel-Storefront - Hinweis zur Cookie-Einschränkung](./assets/storefront-cookie-restriction-message.png){width="600"}

### Schritt 1: Aktivieren des Cookie-Einschränkungsmodus

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Im linken Navigationsbereich unter **[!UICONTROL General]** auswählen **[!UICONTROL Web]**.

1. Erweitern Sie die **[!UICONTROL Default Cookie Settings]** und führen Sie folgende Schritte aus:

   ![Webkonfiguration - standardmäßige Cookie-Einstellungen](./assets/web-default-cookie-settings.png){width="600"}

   - Geben Sie die **[!UICONTROL Cookie Lifetime]** in Sekunden.

   - Wenn Sie Cookies für andere Ordner verfügbar machen möchten, geben Sie die **[!UICONTROL Cookie Path]**. Geben Sie einen Schrägstrich (`/`). Dieser Wert kann nur den Cookie-Pfad enthalten und **_cannot_** enthält alle anderen Cookie-Parameter.

   - Um die Cookies für eine Subdomain verfügbar zu machen, geben Sie den Namen der Subdomain in das Feld **[!UICONTROL Cookie Domain]** field (`subdomain.yourdomain.com`). Um Cookies für alle Subdomains verfügbar zu machen, geben Sie den Domänennamen gefolgt von einem Punkt ein (`.yourdomain.com`). Dieser Wert kann nur die Cookie-Domäne enthalten und **_cannot_** enthält alle anderen Cookie-Parameter.

   - Um zu verhindern, dass Skriptsprachen wie JavaScript Zugriff auf Cookies erhalten, müssen Sie Folgendes sicherstellen: **Nur HTTP verwenden** auf `Yes`.

   - Satz **[!UICONTROL Cookie Restriction Mode]** nach `Yes`.

     Deaktivieren Sie bei Bedarf das Kontrollkästchen und klicken Sie auf **[!UICONTROL OK]** zur Bestätigung des Bereichswechsels.

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save Config]**.

1. Wenn Sie aufgefordert werden, den Cache zu aktualisieren, klicken Sie auf die **[!UICONTROL Cache Management]** in der Systemmeldung. Aktualisieren Sie dann jeden ungültigen Cache.

### Schritt 2: Datenschutzrichtlinie aktualisieren

Aktualisieren Sie Ihre [Datenschutzrichtlinie](privacy-policy.md) , sodass sie die von Ihrem Unternehmen erfassten Informationen und deren Verwendung widerspiegelt.

## Standard-Cookies

Die Standard-Cookies in Adobe Commerce und Magento Open Source werden als ausnahmsweise/nicht befreit klassifiziert, damit Händler die Anforderungen von Datenschutzbestimmungen wie dem [DSGVO](compliance-gdpr.md). Händler sollten diese Informationen als Anleitung verwenden und sich mit Rechtsberatern beraten, um ihre Datenschutz- und Cookie-Richtlinien im Rahmen einer umfassenden Strategie zur Einhaltung von Datenschutzbestimmungen zu aktualisieren.

Die folgenden Cookies werden von [!DNL Commerce] &quot;vorkonfiguriert&quot;für On-Premise- und Cloud-Installationen. Diese Cookies können durch Funktionen erforderlich sein, die vom Kunden ausdrücklich angefordert werden. Informationen zur Lebensdauer von Sitzungs-Cookies finden Sie unter [Sitzungslebensdauer](../customers/customer-online-options.md).

Einige dieser Cookies bieten Konfigurationsoptionen, einschließlich der Aktivierung/Deaktivierung nach Bedarf.

### Angeforderte Funktions-Cookies (ausgenommen)


#### `add_to_cart`

![Adobe Commerce](../assets/adobe-logo.svg) (Nur Adobe Commerce) Wird vom Google Tag-Manager verwendet. Erfasst die Produkt-SKU, den Namen, den Preis und die Menge, die aus dem Warenkorb entfernt wurden, und stellt die Informationen für die zukünftige Integration durch Skripte von Drittanbietern zur Verfügung.

#### `guest-view`

Speichert die Bestell-ID, die Gastkäufer zum Abrufen ihres Bestellstatus verwenden. Ansicht der Gastbestellungen. Verwendet in _[!DNL Orders and Returns]_Widgets.

- Ist sicher? Nein
- Nur HTTP: Ja
- Ablaufrichtlinie: Sitzung
- Modul: `Magento_Sales`

#### `login_redirect`

Behält die Zielseite bei, die geladen wurde, bevor der Kunde zum Anmelden angewiesen wurde. Eine Login-Umleitung wird mit dem Mini-Warenkorb für angemeldete Kunden verwendet, wenn die Variable [Display Mini Cart](../stores-purchase/cart-configuration.md#mini-cart) Konfigurationsoption auf `Yes`.

- Ist sicher? Nein
- Nur HTTP: Nein
- Ablaufrichtlinie: Sitzung
- Modul: `Magento_Customer`

#### `mage-banners-cache-storage`

![Adobe Commerce](../assets/adobe-logo.svg) (Nur Adobe Commerce) Speichert Bannerinhalte lokal, um die Leistung zu verbessern.

#### `mage-messages`

Verfolgt Fehlermeldungen und andere dem Benutzer angezeigte Benachrichtigungen, z. B. die Zustimmungsmeldung für Cookies und verschiedene Fehlermeldungen. Die Nachricht wird aus dem Cookie gelöscht, nachdem sie dem Käufer angezeigt wurde.

Es gibt keine Option, dieses Cookie zu deaktivieren.

- Ist sicher? Nein
- Nur HTTP: Nein
- Ablaufrichtlinie: Dauer 1 Jahr. Wird am Frontend gelöscht, wenn die Nachricht dem Benutzer angezeigt wird.
- Modul: `Magento_Theme`

#### `mage-translation-storage` (lokale Datenspeicherung)

Speichert übersetzte Inhalte auf Anforderung des Käufers. Wird verwendet, wenn [Übersetzungsstrategie](../configuration-reference/advanced/developer.md) ist als &quot;Wörterbuch (Übersetzung auf Storefront Side)&quot;konfiguriert.

- Ist sicher? Nein
- Nur HTTP: Nein
- Ablaufrichtlinie: Nach lokalen Speicherregeln
- Modul: `Magento_Translation`

#### `mage-translation-file-version` (lokale Datenspeicherung)

Verfolgt die Version der Übersetzungen im lokalen Speicher. Wird verwendet, wenn [Übersetzungsstrategie](../configuration-reference/advanced/developer.md) konfiguriert ist als `Dictionary (Translation on Storefront side)`.

- Ist sicher? Nein
- Nur HTTP: Nein
- Ablaufrichtlinie: Nach lokalen Speicherregeln
- Modul: `Magento_Translation`

#### `product_data_storage` (lokale Datenspeicherung)

Speichert die Konfiguration für Produktdaten zu kürzlich angezeigten/vergleichbaren Produkten.

- Ist sicher? Nein
- Nur HTTP: Nein
- Ablaufrichtlinie: Nach lokalen Speicherregeln
- Modul: `Magento_Catalog`

#### `recently_compared_product` (lokale Datenspeicherung)

Speichert Produkt-IDs von kürzlich verglichenen Produkten.

- Ist sicher? Nein
- Nur HTTP: Nein
- Ablaufrichtlinie: Nach lokalen Speicherregeln
- Modul: `Magento_Catalog`

#### `recently_compared_product_previous` (lokale Datenspeicherung)

Speichert Produkt-IDs von zuvor verglichenen Produkten zur einfachen Navigation.

- Ist sicher? Nein
- Nur HTTP: Nein
- Ablaufrichtlinie: Nach lokalen Speicherregeln
- Modul: `Magento_Catalog`

#### `recently_viewed_product` (lokale Datenspeicherung)

Speichert Produkt-IDs kürzlich angesehener Produkte zur einfachen Navigation.

- Ist sicher? Nein
- Nur HTTP: Nein
- Ablaufrichtlinie: Nach lokalen Speicherregeln
- Modul: `Magento_Catalog`

#### `recently_viewed_product_previous` (lokale Datenspeicherung)

Speichert Produkt-IDs von kürzlich angezeigten Produkten zur einfachen Navigation.

- Ist sicher? Nein
- Nur HTTP: Nein
- Ablaufrichtlinie: Nach lokalen Speicherregeln
- Modul: `Magento_Catalog`

#### `remove_from_cart`

![Adobe Commerce](../assets/adobe-logo.svg) (Nur Adobe Commerce) Verwendet von [Google Tag Manager](../merchandising-promotions/google-tag-manager.md). Erfasst die Produkt-SKU, den Namen, den Preis und die Menge, die dem Warenkorb hinzugefügt werden, und stellt die Informationen für die zukünftige Integration durch Skripte von Drittanbietern zur Verfügung.

#### `stf`

Zeichnet die Zeit auf, zu der Nachrichten von SendFriend gesendet werden ([E-Mail an einen Freund](../stores-purchase/email-a-friend.md)).

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

Der Wert dieses Cookies Trigger die Bereinigung des lokalen Cache-Speichers. Wenn das Cookie von der Backend-Anwendung entfernt wird, bereinigt der Administrator den lokalen Speicher und setzt den Cookie-Wert auf `true`.

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

#### `mage-cache-storage` (lokale Datenspeicherung)

Lokaler Speicher besucherspezifischer Inhalte, die E-Commerce-Funktionen ermöglichen.

- Ist sicher? Nein
- Nur HTTP: Nein
- Ablaufrichtlinie: Sitzung
- Modul: `Magento_Customer`, `Magento_Persistent`, `Magento_NegotiableQuote`

#### `mage-cache-storage-section-invalidation` (lokale Datenspeicherung)

Erzwingt die lokale Speicherung bestimmter Inhaltsabschnitte, die ungültig gemacht werden sollen.

- Ist sicher? Nein
- Nur HTTP: Nein
- Ablaufrichtlinie: Pro lokalem Speicher
- Modul: `Magento_Customer`

#### `persistent_shopping_cart`

Speichert den Schlüssel (ID) des beständigen Warenkorbs, um die Wiederherstellung des Warenkorbs für einen anonymen Käufer zu ermöglichen.

- Ist sicher? Ja
- Nur HTTP: Ja
- Ablaufrichtlinie: basierend auf [Persistenter Warenkorb](../stores-purchase/cart-persistent.md) - Konfiguration der Persistenz-Lebensdauer (Sekunden)
- Modul: `Magento_Persistent`

#### `private_content_version`

Hängt eine zufällige, eindeutige Nummer und Uhrzeit an Seiten mit Kundeninhalt an, um zu verhindern, dass diese auf dem Server zwischengespeichert werden.

Es wird an mehreren Stellen festgelegt: in PHP, in JavaScript als Cookie und in JavaScript auf lokalen Speicher.

Nur HTTP=`Yes` (basierend auf einer Anfrage) bedeutet dies, dass das Cookie sicher ist, wenn es während der HTTPS-Anforderung gesetzt wird, und nicht sicher ist, wenn es während der HTTP-Anforderung gesetzt wird.

- Ist sicher? `Yes` (auf Anfrage), `No`
- Nur HTTP: `No`
- Ablaufrichtlinie: basierend auf [Persistenter Warenkorb](../stores-purchase/cart-persistent.md) - Konfiguration der Persistenz-Lebensdauer (Sekunden)
   - PHP: `1` Jahr / `315360000s` (zehn Jahre)
   - JS: `1` day
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
- Ablaufrichtlinie: `1` year
- Modul: `Magento_Store`

#### `mage-banners-cache-storage` - lokale Datenspeicherung

![Adobe Commerce](../assets/adobe-logo.svg) (Nur Adobe Commerce) Lokaler Speicher für Bannerfunktionen.

- Ist sicher? `No`
- Nur HTTP: `No`
- Ablaufrichtlinie: Nach lokalen Speicherregeln
- Modul: `Magento_Banner`

## Google Analytics-Cookies

Die folgenden Cookies werden bei [Google Analytics](../merchandising-promotions/google-analytics.md) oder Google Universal Analytics vollständig für Ihre Installation aktiviert ist. Informationen zum Deaktivieren dieser Cookies für die Einhaltung der Datenschutzbestimmungen finden Sie unter [Google-Datenschutzeinstellungen](../merchandising-promotions/google-tools.md#google-privacy-settings). Weitere Informationen finden Sie unter [Nutzung von Google Analytics-Cookies auf Websites][1].

### Google Universal Analytics-Cookies - nicht von der Steuer befreit

![Adobe Commerce](../assets/adobe-logo.svg) (Nur Adobe Commerce) JavaScript-Bibliotheken: `gtag.js` und `analytics.js`

- `_ga`: Löscht die Besucher Ihrer Site.
- `_gid`: Löscht die Besucher Ihrer Site.
- `gat`: Wird verwendet, um die Anforderungsrate zu drosseln.
- `dc_gtm_<property-id>`: Verkleinert die Anforderungsrate, wenn Google Analytics mit bereitgestellt werden. [Google Tag Manager](../merchandising-promotions/google-tag-manager.md).
- `AMP_TOKEN`: Enthält ein Token, das zum Abrufen einer Client-ID vom AMP Client-ID-Dienst verwendet werden kann. Andere mögliche Werte sind Opt-out, Inflight-Anfragen oder Fehler beim Abrufen einer Client-ID vom AMP-Client-ID-Dienst.
- `_gac_<property-id>`: Enthält kampagnenbezogene Informationen für den Benutzer. Google AdWords-Konversions-Tags lesen dieses Cookie, wenn Google Analytics mit Ihrer [AdWord][2] -Konto.

### Google Analytics-Cookies - nicht ausgenommen

![Adobe Commerce](../assets/adobe-logo.svg) (Nur Adobe Commerce) JavaScript-Bibliothek: `ga.js`

- `__utma`: unterscheidet Käufer und Sitzungen. Dieses Cookie wird erstellt, wenn die JavaScript-Bibliothek ausgeführt wird und es keine vorhandenen `__utma` Cookie. Das Cookie wird jedes Mal aktualisiert, wenn Daten an Google Analytics gesendet werden.
- `__utmt`: Wird verwendet, um die Anforderungsrate zu drosseln.
- `__utmb`: Ermittelt neue Sitzungen/Besuche. Dieses Cookie wird erstellt, wenn die JavaScript-Bibliothek ausgeführt wird und es keine vorhandenen `__utmb` Cookie. Das Cookie wird jedes Mal aktualisiert, wenn Daten an Google Analytics gesendet werden.
- `_utmz`: Speichert die Traffic-Quelle oder die Kampagne, aus der hervorgeht, wie der Käufer zu Ihrer Site gelangt ist. Das Cookie wird bei Ausführung der JavaScript-Bibliothek erstellt und jedes Mal aktualisiert, wenn Daten an Google Analytics gesendet werden.
- `__utmv`: Speichert benutzerdefinierte Variablendaten auf Besucherebene. Dieses Cookie wird erstellt, wenn ein Entwickler die `_setCustomVar` -Methode mit einer benutzerdefinierten Variable auf Besucherebene verwendet. Dieses Cookie wird jedes Mal aktualisiert, wenn Daten an Google Analytics gesendet werden.

## Cookies in Recommendations

![Adobe Commerce](../assets/adobe-logo.svg) (Nur Adobe Commerce) Die folgenden Cookies werden von Product Recommendations für Adobe Commerce-Kunden verwendet. Diese Cookies werden mit dem [DataServices-Modul](https://experienceleague.adobe.com/docs/commerce-merchant-services/product-recommendations/getting-started/install-configure.html).

- `mg_dnt`: Ermöglicht Ihnen Folgendes: [Adobe Commerce-Datenerfassung einschränken](https://experienceleague.adobe.com/docs/commerce-merchant-services/product-recommendations/developer/setting-cookie.html) wenn Sie über benutzerdefinierten Code verfügen, um die Cookie-Zustimmung auf Ihrer Site zu verwalten.
- `user_allowed_save_cookie`: Wird verwendet für [Cookie-Einschränkungsmodus](#cookie-restriction-mode).
- `authentication_flag`: Gibt an, ob sich ein Käufer angemeldet oder abgemeldet hat. Dieses Cookie wird gleichzeitig mit dem `dataservices_customer_id` Cookie.
- `dataservices_customer_id`: Gibt an, ob sich ein Käufer angemeldet oder abgemeldet hat. Dieses Cookie enthält die eindeutige ID des Kunden im System.
- `dataservices_customer_group`: Gibt die Gruppe eines Kunden an. Dieses Cookie wird als [sha1](https://en.wikipedia.org/wiki/SHA-1) Prüfsumme der Gruppen-ID des Kunden.
- `dataservices_cart_id`: Identifiziert die Warenkorbaktionen eines Käufers. Dieses Cookie enthält die eindeutige Warenkorb-ID des Kunden im System.
- `dataservices_product_context`: Identifiziert die Produktinteraktionen eines Käufers. Dieses Cookie enthält die eindeutige Angebots-ID des Kunden im System.

## Zusätzliche Cookies

![Adobe Commerce](../assets/adobe-logo.svg) (Nur Adobe Commerce) Die folgenden Cookies werden für Adobe Commerce-Kunden gesetzt. Diese Cookies werden mit dem [DataServices-Modul](https://experienceleague.adobe.com/docs/commerce-merchant-services/product-recommendations/getting-started/install-configure.html).

- `mg`: Festgelegt durch Snowplom-JavaScript-Tracker. Weitere Informationen finden Sie im [Snowpflug-Dokumentation](https://docs.snowplow.io/docs/collecting-data/collecting-from-own-applications/javascript-trackers/javascript-tracker/javascript-tracker-v3/tracker-setup/initialization-options).
- `com.adobe.alloy.getTld`: Bei dem Hostnamen der aktuellen Webseite handelt es sich um die oberste Domäne, die kein &quot;öffentliches Suffix&quot;ist, wie in https://publicsuffix.org beschrieben. Im Wesentlichen ist dies die Domäne mit der höchsten Priorität, die Cookies akzeptieren kann. Dieses Cookie ist Teil der [Alloy Web SDK](https://github.com/adobe/alloy).

[1]: https://developers.google.com/analytics/devguides/collection/analyticsjs/cookie-usage
[2]: https://support.google.com/adwords/answer/7521212
