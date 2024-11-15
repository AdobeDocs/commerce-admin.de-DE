---
title: Einhaltung von Cookie-Rechtsvorschriften
description: Um mit den Rechtsvorschriften in vielen Ländern in Bezug auf die Verwendung von Cookies Schritt zu halten, bieten Adobe Commerce und Magento Open Source den Händlern die Möglichkeit, die Zustimmung des Kunden einzuholen.
exl-id: 42df20cd-50a7-4618-98fd-9ced936e305b
feature: Compliance
source-git-commit: 04e8fe7cf303f434bab748df447eef8ac1097196
workflow-type: tm+mt
source-wordcount: '1825'
ht-degree: 0%

---

# Einhaltung von Cookie-Rechtsvorschriften

Cookies sind kleine Dateien, die auf dem Computer jedes Besuchers Ihrer Site gespeichert und als temporäre Speicherorte für Informationen verwendet werden. Informationen, die in Cookies gespeichert werden, werden verwendet, um das Einkaufserlebnis zu personalisieren, Besucher mit ihrem Warenkorb zu verknüpfen, Traffic-Muster zu messen und die Effektivität von Promotions zu verbessern. Um mit den Rechtsvorschriften in vielen Ländern in Bezug auf die Verwendung von Cookies Schritt zu halten, bieten Adobe Commerce und Magento Open Source den Händlern die Möglichkeit, die Zustimmung des Kunden einzuholen. Eine Liste der Standard-Cookies in Adobe Commerce und Magento Open Source finden Sie in der [Cookie-Referenz](#default-cookies).

>[!NOTE]
>
>Wenn Sie die standardmäßigen [Datenschutzeinstellungen von Google](../merchandising-promotions/google-tools.md#google-privacy-settings) ändern, um die [Datenschutz-Grundverordnung](compliance-gdpr.md) einzuhalten, ist es nicht erforderlich, die Benutzerzustimmung für die Verwendung von Google Analytics-Cookies einzuholen.

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

1. Wenn Sie aufgefordert werden, den Cache zu aktualisieren, klicken Sie in der Systemmeldung auf den Link **[!UICONTROL Cache Management]** und aktualisieren Sie jeden ungültigen Cache.

### Schritt 2: Datenschutzrichtlinie aktualisieren

Aktualisieren Sie Ihre [Datenschutzrichtlinie](privacy-policy.md), sodass sie die von Ihrem Unternehmen erfassten Informationen und deren Verwendung widerspiegelt.

## Standard-Cookies

Die Standard-Cookies in Adobe Commerce und Magento Open Source werden als &quot;Ausgenommen/Nicht-Ausgenommen&quot;klassifiziert, um Händlern zu helfen, die Anforderungen von Datenschutzbestimmungen wie der [DSGVO](compliance-gdpr.md) zu erfüllen. Händler sollten diese Informationen als Anleitung verwenden und sich mit Rechtsberatern beraten, um ihre Datenschutz- und Cookie-Richtlinien im Rahmen einer umfassenden Strategie zur Einhaltung von Datenschutzbestimmungen zu aktualisieren.

Die folgenden Cookies werden von [!DNL Commerce] &quot;vorkonfiguriert&quot;für On-Premise- und Cloud-Installationen verwendet. Diese Cookies können durch Funktionen erforderlich sein, die vom Kunden ausdrücklich angefordert werden. Weitere Informationen zur Lebensdauer von Sitzungs-Cookies finden Sie unter [Sitzungslebensdauer](../customers/customer-online-options.md).

Einige dieser Cookies bieten Konfigurationsoptionen, einschließlich der Aktivierung/Deaktivierung nach Bedarf.

### Angeforderte Funktions-Cookies (ausgenommen)

#### `add_to_cart`

![Adobe Commerce](../assets/adobe-logo.svg) (nur Adobe Commerce) Erfasst die Produkt-SKU, den Namen, den Preis und die Menge, die aus dem Warenkorb entfernt wurden. Ermöglicht Google Analytics zu erfahren, wann einem Warenkorb ein Produkt hinzugefügt wurde.

#### `guest-view`

Verknüpft eine Gastbestellung mit einem Gast (da kein Konto für den Gast vorhanden ist).

#### `login_redirect`

Speichert die Umleitungs-URL für den Weiterleitungsbenutzer bei erfolgreicher Anmeldung und Benutzerregistrierung. Speichert die Seite, auf der sich ein Benutzer vor der Anmeldung befand (um den Ort zu bestimmen, zu dem er nach der Anmeldung zurückkehren wird).

#### `mage-banners-cache-storage`

![Adobe Commerce](../assets/adobe-logo.svg) (nur Adobe Commerce) Speichert Bannerinhalte lokal, um die Leistung zu verbessern. Bannerinhalte sind alle Inhalte, die ein Händler auf seiner Website anzeigen würde.

#### `mage-messages`

Verfolgt Fehlermeldungen und andere dem Benutzer angezeigte Benachrichtigungen, z. B. die Zustimmungsmeldung für Cookies und verschiedene Fehlermeldungen. Die Nachricht wird aus dem Cookie gelöscht, nachdem sie dem Käufer angezeigt wurde. Es gibt keine Option, dieses Cookie zu deaktivieren. So werden dem Benutzer einmalige Informationen wie Fehlermeldungen übermittelt.

#### `product_data_storage` (lokaler Speicher)

Speichert die Konfiguration für Produktdaten, die zur Verwendung der Funktionen &quot;Kürzlich angesehen&quot;und &quot;Produkte vergleichen&quot;verwendet werden. Speichert die spezifischen Einstellungen eines Benutzers (z. B. wenn er kürzlich ein Produkt oder ein vergleichbares Produkt angesehen hat).

#### `recently_compared_product` (lokaler Speicher)

Speichert Produkt-IDs von kürzlich verglichenen Produkten.

#### `recently_compared_product_previous` (lokaler Speicher)

Speichert Produkt-IDs von zuvor verglichenen Produkten zur einfachen Navigation.

#### `recently_viewed_product` (lokaler Speicher)

Speichert Produkt-IDs kürzlich angesehener Produkte zur einfachen Navigation.

#### `recently_viewed_product_previous` (lokaler Speicher)

Speichert Produkt-IDs kürzlich angesehener Produkte zur einfachen Navigation.

#### `remove_from_cart`

![Adobe Commerce](../assets/adobe-logo.svg) (nur Adobe Commerce) Ermöglicht Google Analytics zu erfahren, wann ein Produkt aus dem Warenkorb entfernt wurde.

#### `stf`

Zeichnet die Zeit auf, zu der Nachrichten vom Modul SendFriend ([E-Mail an einen Freund](../stores-purchase/email-a-friend.md)) gesendet werden. Wenn ein Käufer einen Link zu einem Produkt sendet, zeichnet dieses Cookie einen Zeitstempel auf und verwaltet eine Zählung.

#### `X-Magento-Vary`

Gibt an, wann eine neue Version einer Seite aus dem Cache bereitgestellt werden muss. Unterstützt die Leistung von Websites.

#### `form_key`

Ein Sicherheitsmechanismus, der einen zufällig generierten Wert enthält, um Cross Site Request Forgery-Angriffe (CSRF) zu verhindern, indem festgestellt werden kann, ob eine Anforderung von einer echten Quelle oder von einem falschen Akteur stammt. Dies ist eine branchenübliche Vorgehensweise, um CSRF-Angriffe zu verhindern.

#### `mage-cache-sessid`

Nützlich bei der Bestimmung, wann der lokale Speicher im Browser nach Ablauf der Sitzung gereinigt werden soll. Damit wird bestimmt, ob der lokale Speicher bereinigt werden muss. Das Fehlen dieses Cookies Trigger die Bereinigung des lokalen Datenspeichers.

#### `mage-cache-storage`

Lokaler Speicher besucherspezifischer Inhalte, die E-Commerce-Funktionen ermöglichen. Standardmäßig nicht verwendet, aber wenn sie verwendet wird, wird sie verwendet, um den Checkout zu beschleunigen, sodass grundlegende Benutzerinformationen verfügbar sind, wenn ein Benutzer verlässt und zurückkehrt.

#### `mage-cache-storage-section-invalidation`

Speichert Informationen darüber, welche Abschnitte der Seite invalidiert und entfernt werden müssen.

#### `persistent_shopping_cart`

Speichert die Schlüssel-ID eines beständigen Warenkorbs, um die Wiederherstellung des Warenkorbs für einen anonymen Käufer zu ermöglichen.

#### `private_content_version`

Hängt eine zufällige, eindeutige Nummer und Uhrzeit an Seiten mit Kundeninhalt an, um zu verhindern, dass diese auf dem Server zwischengespeichert werden. Es wird an mehreren Stellen festgelegt: in PHP, in JavaScript als Cookie und in JavaScript zum lokalen Speicher.

#### `section_data_ids`

Speichert kundenspezifische Informationen zu von Käufern initiierten Aktionen, z. B. Anzeige der Wunschliste und Checkout-Informationen.

#### `store`

Verfolgt die vom Käufer ausgewählte Store-Ansicht/Gebietsschema.

#### `mage-banners-cache-storage`

![Adobe Commerce](../assets/adobe-logo.svg) (nur Adobe Commerce) Lokaler Speicher für Bannerfunktionen. Banner bezeichnet allgemeine Website-Assets mit allen Informationen, die einem Käufer angezeigt werden.

#### `PHPSESSID`

Verfolgt Benutzersitzungen auf der Storefront. Das sind die Käufer, die die Endprodukte verwenden.

#### `admin`

Verfolgt Benutzersitzungen auf Admin-Seite.

#### `loggedOutReasonCode`

Wird festgelegt, wenn ein Admin-Benutzer nach einer bestimmten Anzahl nicht erfolgreicher Kennwortversuche gesperrt wird.

#### `section_data_clean`

Wird festgelegt, wenn ein Benutzer die Store-Ansicht wechselt. Durch das Vorhandensein dieses Cookies wird JavaScript Trigger, bestimmte Bereiche auf der Seite neu zu laden, um die richtige Store-Ansicht widerzuspiegeln.

#### `lang`

Wird indirekt vom Admin Analytics-Modul eingestellt. Wird nur in einem Verwaltungsbereich eines Stores verwendet. Gilt nicht für Käufer.

#### `s_fid`

Wird indirekt vom Admin Analytics-Modul eingestellt. Fallback-Unique Visitor-ID - Zeitstempel/Datumsstempel. Sie wird zur Identifizierung eines Unique Visitors verwendet, wenn das standardmäßige `s_vi` -Cookie aufgrund von Beschränkungen für Drittanbieter-Cookies nicht verfügbar ist. Wird nur in einem Verwaltungsbereich eines Stores verwendet. Gilt nicht für Käufer.

#### `s_cc`

Wird indirekt vom Admin Analytics-Modul eingestellt. Sie wird vom JavaScript-Code festgelegt und gelesen, um zu bestimmen, ob Cookies aktiviert sind. Wird nur in einem Verwaltungsbereich eines Stores verwendet. Gilt nicht für Käufer.

#### `apt.sid`

Wird von der PX-Bibliothek von Gainsight festgelegt, die indirekt vom Admin Analytics-Modul verwendet wird. Das Ziel dieses Cookies besteht darin, das persistente Sitzungs-ID-Tracking unter der Domäne der obersten Ebene des Produkts zu ermöglichen und wird als Referenz-ID für die aktive Sitzung verwendet. Wird nur in einem Verwaltungsbereich eines Stores verwendet. Gilt nicht für Käufer.

#### `apt.uid`

Wird von der PX-Bibliothek von Gainsight festgelegt, die indirekt vom Admin Analytics-Modul verwendet wird. Das Ziel dieses Cookies ist es, ein beständiges ID-Tracking unter der Domäne der obersten Ebene des Produkts zu ermöglichen und wird als Referenz-ID für die Benutzerentität verwendet. Wird nur in einem Verwaltungsbereich eines Stores verwendet. Gilt nicht für Käufer.

#### `s_sq`

Wird indirekt vom Admin Analytics-Modul eingestellt. Wird von der ClickMap-Funktion verwendet, mit der Daten darüber erfasst werden, wohin Besucher klicken und worauf sie klicken. Speichert Informationen aus jedem Klick. Wird nur in einem Verwaltungsbereich eines Stores verwendet. Gilt nicht für Käufer.

#### `pagebuilder_modal_dismissed`

Festgelegt durch das Seitenaufbau-Modul. Enthält ein Flag, das verhindert, dass nachfolgende Aufforderungen an einen Administrator gesendet werden, um zu bestätigen, dass eine bestimmte Aktion geöffnet wird, wenn der Administrator sie zuvor ausdrücklich verworfen hat. Wird nur in einem Verwaltungsbereich eines Stores verwendet. Gilt nicht für Käufer.

#### `pagebuilder_template_apply_confirm`

Festgelegt durch das Seitenaufbau-Modul. Enthält ein Flag, das verhindert, dass nachfolgende Aufforderungen an einen Administrator gesendet werden, um zu bestätigen, dass eine bestimmte Aktion geöffnet wird, wenn der Administrator sie zuvor ausdrücklich verworfen hat. Wird nur in einem Verwaltungsbereich eines Stores verwendet. Gilt nicht für Käufer.

#### `accordion-{VARIABLE}-{VARIABLE}`

Wird als Teil der Implementierung von Registerkarten-Funktionen nur in einem Verwaltungsbereich eines Stores verwendet. Gilt nicht für Käufer.

## Cookies in Recommendations

![Adobe Commerce](../assets/adobe-logo.svg) (nur Adobe Commerce) Die folgenden Cookies werden von Product Recommendations für Adobe Commerce-Kunden verwendet. Diese Cookies werden mit dem [DataServices-Modul](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/product-recommendations/getting-started/install-configure) installiert.

- `mg_dnt`: Ermöglicht Ihnen die [Einschränkung der Adobe Commerce-Datenerfassung](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/product-recommendations/developer/setting-cookie), wenn Sie über benutzerdefinierten Code verfügen, um die Cookie-Zustimmung auf Ihrer Site zu verwalten.
- `user_allowed_save_cookie`: Wird für den [Cookie-Einschränkungsmodus](#cookie-restriction-mode) verwendet.
- `authentication_flag`: Gibt an, ob sich ein Käufer angemeldet oder abgemeldet hat. Dieses Cookie wird gleichzeitig mit dem `dataservices_customer_id` -Cookie aktualisiert.
- `dataservices_customer_id`: Gibt an, ob sich ein Käufer angemeldet oder abgemeldet hat. Dieses Cookie enthält die eindeutige ID des Kunden im System.
- `dataservices_customer_group`: Gibt die Gruppe eines Kunden an. Dieses Cookie wird als Prüfsumme [sha1](https://en.wikipedia.org/wiki/SHA-1) der Gruppen-ID des Kunden gespeichert.
- `dataservices_cart_id`: Identifiziert die Warenkorbaktionen eines Käufers. Dieses Cookie enthält die eindeutige Warenkorb-ID des Kunden im System.
- `dataservices_product_context`: Identifiziert die Produktinteraktionen eines Käufers. Dieses Cookie enthält die eindeutige Angebots-ID des Kunden im System.

## Zusätzliche Cookies

![Adobe Commerce](../assets/adobe-logo.svg) (nur Adobe Commerce) Die folgenden Cookies werden für Adobe Commerce-Kunden gesetzt. Diese Cookies werden mit dem [DataServices-Modul](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/product-recommendations/getting-started/install-configure) installiert.

- `mg`: Wird durch den Snowplom-JavaScript-Tracker festgelegt. Weitere Informationen finden Sie in der Dokumentation zu [Snowplow](https://docs.snowplow.io/docs/collecting-data/collecting-from-own-applications/javascript-trackers/web-tracker/tracker-setup/initialization-options) .
- `com.adobe.alloy.getTld`: Bei dem Hostnamen der aktuellen Webseite handelt es sich um die oberste Domäne, bei der es sich nicht um ein &quot;öffentliches Suffix&quot;handelt, wie in https://publicsuffix.org beschrieben. Im Wesentlichen ist dies die Domäne mit der höchsten Priorität, die Cookies akzeptieren kann. Dieses Cookie ist Teil des [Alloy Web SDK](https://github.com/adobe/alloy).

[1]: https://developers.google.com/analytics/devguides/collection/analyticsjs/cookie-usage
[2]: https://support.google.com/adwords/answer/7521212
