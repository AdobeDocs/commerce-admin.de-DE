---
title: Cookie-Gesetzestreue
description: Um mit der Gesetzgebung in vielen Ländern bezüglich der Verwendung von Cookies Schritt zu halten, bieten Adobe Commerce und Magento Open Source Händlern eine Auswahl an Methoden, um das Einverständnis des Kunden einzuholen.
exl-id: 42df20cd-50a7-4618-98fd-9ced936e305b
feature: Compliance
source-git-commit: 04e8fe7cf303f434bab748df447eef8ac1097196
workflow-type: tm+mt
source-wordcount: '1825'
ht-degree: 0%

---

# Cookie-Gesetzestreue

Cookies sind kleine Dateien, die auf dem Computer jedes Besuchers Ihrer Website gespeichert werden und als temporäre Speicherorte für Informationen verwendet werden. Die in Cookies gespeicherten Informationen werden verwendet, um das Einkaufserlebnis zu personalisieren, Besucher mit ihrem Warenkorb zu verknüpfen, Traffic-Muster zu messen und die Effektivität von Werbeaktionen zu verbessern. Um mit der Gesetzgebung in vielen Ländern bezüglich der Verwendung von Cookies Schritt zu halten, bieten Adobe Commerce und Magento Open Source Händlern eine Auswahl an Methoden, um das Einverständnis des Kunden einzuholen. Eine Liste der Standard-Cookies in Adobe Commerce und Magento Open Source finden Sie unter [Cookie-Referenz](#default-cookies).

>[!NOTE]
>
>Wenn Sie die standardmäßigen [Google-Datenschutzeinstellungen](../merchandising-promotions/google-tools.md#google-privacy-settings) ändern, um die [Datenschutz-Grundverordnung](compliance-gdpr.md) einzuhalten, ist es nicht erforderlich, die Zustimmung der Benutzenden zur Verwendung von Google Analytics-Cookies einzuholen.

## Cookie-Einschränkungsmodus

Wenn der Cookie-Einschränkungsmodus aktiviert ist, werden Besucher Ihres Stores benachrichtigt, dass Cookies für Vorgänge mit vollem Funktionsumfang erforderlich sind. Je nach Design kann die Nachricht über der Kopfzeile, unter der Fußzeile oder an einer anderen Stelle auf der Seite angezeigt werden. Die Nachricht verweist auf Ihre Datenschutzrichtlinie, um weitere Informationen zu erhalten, und ermutigt Besuchende, auf die Schaltfläche „Zulassen“ zu klicken, um ihr Einverständnis zu erteilen. Nachdem das Einverständnis erteilt wurde, verschwindet die Nachricht.

Ihre [Datenschutzrichtlinie](privacy-policy.md) sollte den Namen Ihres Stores und Kontaktinformationen enthalten und den Zweck jedes Cookies erklären, das von Ihrem Store verwendet wird. Weitere Informationen finden Sie unter [Cookie-Referenz](#default-cookies).

>[!NOTE]
>
>Wenn Sie den URL-Schlüssel der Datenschutzrichtlinie ändern, müssen Sie auch eine benutzerdefinierte URL-Umschreibung erstellen, um Traffic zum neuen URL-Schlüssel umzuleiten. Andernfalls gibt der Link in der Nachricht Cookie-Einschränkungsmodus `404 Page Not Found` zurück.

![Beispiel für Storefront - Hinweis zu Cookie-Einschränkungen](./assets/storefront-cookie-restriction-message.png){width="600"}

### Schritt 1: Aktivieren des Cookie-Einschränkungsmodus

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Wählen Sie im linken Navigationsbereich unter **[!UICONTROL General]** die Option **[!UICONTROL Web]** aus.

1. Erweitern Sie den Abschnitt **[!UICONTROL Default Cookie Settings]** und gehen Sie folgendermaßen vor:

   ![Web-Konfiguration - Standard-Cookie-Einstellungen](./assets/web-default-cookie-settings.png){width="600"}

   - Geben Sie die **[!UICONTROL Cookie Lifetime]** in Sekunden ein.

   - Wenn Sie Cookies für andere Ordner verfügbar machen möchten, geben Sie den **[!UICONTROL Cookie Path]** ein. Um die Cookies an einer beliebigen Stelle auf der Website verfügbar zu machen, geben Sie einen Schrägstrich (`/`) ein. Dieser Wert kann nur den Cookie-Pfad enthalten und **_keine_** Cookie-Parameter enthalten.

   - Um die Cookies für eine Subdomain verfügbar zu machen, geben Sie den Namen der Subdomain in das Feld **[!UICONTROL Cookie Domain]** ein (`subdomain.yourdomain.com`). Um Cookies für alle Subdomains verfügbar zu machen, geben Sie den Domain-Namen mit vorangestelltem Punkt ein (`.yourdomain.com`). Dieser Wert kann nur die Cookie-Domain enthalten und **_kann_** keine anderen Cookie-Parameter enthalten.

   - Um zu verhindern, dass Skriptsprachen wie JavaScript Zugriff auf Cookies erhalten, stellen Sie sicher, dass **Nur HTTP verwenden** auf `Yes` gesetzt ist.

   - Legen Sie **[!UICONTROL Cookie Restriction Mode]** auf `Yes` fest.

     Deaktivieren Sie bei Bedarf das Kontrollkästchen und klicken Sie auf **[!UICONTROL OK]** , um den Wechsel des Umfangs zu bestätigen.

1. Klicken Sie abschließend auf **[!UICONTROL Save Config]**.

1. Wenn Sie aufgefordert werden, den Cache zu aktualisieren, klicken Sie auf den Link **[!UICONTROL Cache Management]** in der Systemmeldung und aktualisieren Sie jeden ungültigen Cache.

### Schritt 2: Aktualisieren Sie Ihre Datenschutzrichtlinie

Aktualisieren Sie Ihre [Datenschutzrichtlinie](privacy-policy.md) so, dass sie die von Ihrem Unternehmen erfassten Informationen und deren Verwendung widerspiegelt.

## Standard-Cookies

Die standardmäßigen Cookies in Adobe Commerce und Magento Open Source werden als „Frei/Nicht frei“ klassifiziert, um Händlern bei der Erfüllung der Anforderungen von Datenschutzbestimmungen wie der [DSGVO](compliance-gdpr.md) zu helfen. Händler sollten diese Informationen als Leitfaden verwenden und sich mit Rechtsberatern beraten, um ihre Datenschutz- und Cookie-Richtlinien im Rahmen einer umfassenden Strategie zur Einhaltung von Datenschutzbestimmungen zu aktualisieren.

Die folgenden Cookies werden von [!DNL Commerce] „Out-of-the-Box“ für On-Premise- und Cloud-Installationen verwendet. Diese Cookies können aufgrund von Funktionen erforderlich sein, die vom Kunden explizit angefordert werden. Weitere Informationen zur Lebensdauer von Sitzungs-Cookies finden Sie unter [Sitzungslebensdauer](../customers/customer-online-options.md).

Einige dieser Cookies können Konfigurationsoptionen bereitstellen, einschließlich Aktivieren/Deaktivieren bei Bedarf.

### Angeforderte Funktionalität - Cookies (ausgenommen)

#### `add_to_cart`

![Adobe Commerce](../assets/adobe-logo.svg) (nur Adobe Commerce) Erfasst die Produkt-SKU, den Namen, den Preis und die Menge, die aus dem Warenkorb entfernt wurden. Ermöglicht Google Analytics zu wissen, wann ein Produkt zu einem Warenkorb hinzugefügt wurde.

#### `guest-view`

Verknüpft einen Gastauftrag mit einem Gast (da kein Konto für einen Gast vorhanden ist).

#### `login_redirect`

Speichert die Umleitungs-URL für den Routing-Benutzer bei erfolgreicher Anmeldung und Benutzerregistrierung. Speichert die Seite, auf der sich ein Benutzer vor der Anmeldung befand (um zu bestimmen, an welchen Speicherort er nach der Anmeldung zurückkehren wird).

#### `mage-banners-cache-storage`

![Adobe Commerce](../assets/adobe-logo.svg) (nur Adobe Commerce) speichert Bannerinhalte lokal, um die Leistung zu verbessern. Bannerinhalte sind alle Inhalte, die ein Händler auf seiner Website anzeigen würde.

#### `mage-messages`

Verfolgt Fehlermeldungen und andere Benachrichtigungen, die Benutzenden angezeigt werden, wie z. B. die Cookie-Einverständnismeldung und verschiedene Fehlermeldungen. Die Nachricht wird aus dem Cookie gelöscht, nachdem sie dem Käufer angezeigt wurde. Es gibt keine Option, um dieses Cookie zu deaktivieren. So werden dem Benutzer einmalige Informationen, z. B. Fehlermeldungen, übermittelt.

#### `product_data_storage` (lokaler Speicher)

Speichert die Konfiguration für Produktdaten, die für die Verwendung der Funktionen „Kürzlich angezeigt“ und „Produkte vergleichen“ verwendet werden. Speichert die spezifischen Einstellungen eines Benutzers (z. B. wenn er kürzlich ein Produkt angesehen oder Produkte verglichen hat).

#### `recently_compared_product` (lokaler Speicher)

Speichert Produkt-IDs von kürzlich verglichenen Produkten.

#### `recently_compared_product_previous` (lokaler Speicher)

Speichert Produkt-IDs zuvor vergleichbarer Produkte für eine einfache Navigation.

#### `recently_viewed_product` (lokaler Speicher)

Speichert Produkt-IDs von kürzlich angezeigten Produkten für eine einfache Navigation.

#### `recently_viewed_product_previous` (lokaler Speicher)

Speichert Produkt-IDs von kürzlich angezeigten Produkten für eine einfache Navigation.

#### `remove_from_cart`

![Adobe Commerce](../assets/adobe-logo.svg) (nur Adobe Commerce) Ermöglicht Google Analytics zu wissen, wann ein Produkt aus dem Warenkorb entfernt wurde.

#### `stf`

Zeichnet auf, wann Nachrichten vom SendFriend-Modul (E[Mail an einen Freund](../stores-purchase/email-a-friend.md) gesendet werden. Wenn ein Käufer einen Link zu einem Produkt sendet, zeichnet dieses Cookie einen Zeitstempel auf und verwaltet eine Zählung.

#### `X-Magento-Vary`

Gibt an, wann eine neue Version einer Seite aus dem Cache bereitgestellt werden muss. Unterstützt die Leistung von Websites.

#### `form_key`

Ein Sicherheitsmechanismus mit einem zufällig generierten Wert, der CSRF (Cross Site Request Forgery)-Angriffe verhindert, indem ermittelt wird, ob eine Anfrage von einer echten Quelle oder einem fehlerhaften Akteur stammt. Dies ist eine branchenübliche Vorgehensweise, um CSRF-Angriffe zu verhindern.

#### `mage-cache-sessid`

Hilfreich bei der Bestimmung, wann der lokale Speicher im Browser nach Ablauf der Sitzung bereinigt werden soll. Auf diese Weise wird bestimmt, ob der lokale Speicher bereinigt werden muss. Trigger Durch das Fehlen dieses Cookies wird der lokale Speicher bereinigt.

#### `mage-cache-storage`

Lokale Speicherung besucherspezifischer Inhalte, die E-Commerce-Funktionen ermöglichen. Standardmäßig nicht verwendet, aber wenn es verwendet wird, wird es verwendet, um den Checkout zu beschleunigen, sodass grundlegende Benutzerinformationen verfügbar sind, wenn jemand geht und zurückkehrt.

#### `mage-cache-storage-section-invalidation`

Speichert Informationen darüber, welche Abschnitte der Seite ungültig gemacht und entfernt werden müssen.

#### `persistent_shopping_cart`

Speichert die Schlüssel-ID eines beständigen Warenkorbs, um es zu ermöglichen, den Warenkorb für einen anonymen Käufer wiederherzustellen.

#### `private_content_version`

Hängt Seiten mit Kundeninhalten eine zufällige, eindeutige Anzahl und Zeit an, um zu verhindern, dass sie auf dem Server zwischengespeichert werden. Es wird an mehreren Stellen festgelegt: in PHP, in JavaScript als Cookie und in JavaScript als lokaler Speicher.

#### `section_data_ids`

Speichert kundenspezifische Informationen zu von Käufern initiierten Aktionen, wie z. B. die Anzeige von Wunschlisten und Checkout-Informationen.

#### `store`

Verfolgt die spezifische Store-Ansicht/das spezifische Gebietsschema, die bzw. das vom Einkäufer ausgewählt wurde.

#### `mage-banners-cache-storage`

![Adobe Commerce](../assets/adobe-logo.svg) (nur Adobe Commerce) Lokaler Speicher für Bannerfunktionen. Banner bedeutet, dass allgemeine Website-Assets alle Informationen enthalten, die einem Käufer angezeigt werden.

#### `PHPSESSID`

Verfolgt Benutzersitzungen auf der Storefront. Dies sind die Käufer, die die Endprodukte verwenden.

#### `admin`

Verfolgt Benutzersitzungen auf der Administratorseite.

#### `loggedOutReasonCode`

Wird festgelegt, wenn ein Admin-Benutzer nach einer bestimmten Anzahl erfolgloser Passwortversuche gesperrt wird.

#### `section_data_clean`

Festlegen, wenn ein Benutzer die Store-Ansicht wechselt. Durch das Vorhandensein dieses Cookies wird JavaScript dazu Trigger, bestimmte Abschnitte auf der Seite neu zu laden, um die richtige Store-Ansicht widerzuspiegeln.

#### `lang`

Indirekt durch das Analytics-Admin-Modul festgelegt. Wird nur in einem administrativen Bereich eines Geschäfts verwendet. Gilt nicht für Käufer.

#### `s_fid`

Indirekt durch das Analytics-Admin-Modul festgelegt. Fallback-Unique-Visitor-ID: Zeit-/Datumsstempel. Er wird verwendet, um einen Unique Visitor zu identifizieren, wenn das Standard-`s_vi`-Cookie aufgrund von Beschränkungen für Drittanbieter-Cookies nicht verfügbar ist. Wird nur in einem administrativen Bereich eines Geschäfts verwendet. Gilt nicht für Käufer.

#### `s_cc`

Indirekt durch das Analytics-Admin-Modul festgelegt. Sie wird vom JavaScript-Code festgelegt und gelesen, um zu bestimmen, ob Cookies aktiviert sind. Wird nur in einem administrativen Bereich eines Geschäfts verwendet. Gilt nicht für Käufer.

#### `apt.sid`

Wird durch die Gainsight PX-Bibliothek festgelegt, die indirekt vom Admin Analytics-Modul verwendet wird. Der Zweck dieses Cookies ist es, ein persistentes Sitzungs-ID-Tracking unter der Top-Level-Domain des Produkts zu ermöglichen und als Referenz-ID für die aktive Sitzung zu verwenden. Wird nur in einem administrativen Bereich eines Geschäfts verwendet. Gilt nicht für Käufer.

#### `apt.uid`

Wird durch die Gainsight PX-Bibliothek festgelegt, die indirekt vom Admin Analytics-Modul verwendet wird. Der Zweck dieses Cookies ist es, ein persistentes ID-Tracking unter der Top-Level-Domain des Produkts zu ermöglichen und als Referenz-ID für die Benutzerentität zu verwenden. Wird nur in einem administrativen Bereich eines Geschäfts verwendet. Gilt nicht für Käufer.

#### `s_sq`

Indirekt durch das Analytics-Admin-Modul festgelegt. Wird von der ClickMap-Funktion verwendet, die Daten darüber erfasst, wo Besuchende klicken und worauf sie klicken. Speichert Informationen zu jedem Klick. Wird nur in einem administrativen Bereich eines Geschäfts verwendet. Gilt nicht für Käufer.

#### `pagebuilder_modal_dismissed`

Wird durch das Page Builder-Modul festgelegt. Enthält ein Flag, das verhindert, dass nachfolgende Aufforderungen an einen Administrator, eine bestimmte Aktion zu bestätigen, geöffnet werden, wenn der Administrator sie zuvor ausdrücklich abgelehnt hat. Wird nur in einem administrativen Bereich eines Geschäfts verwendet. Gilt nicht für Käufer.

#### `pagebuilder_template_apply_confirm`

Wird durch das Page Builder-Modul festgelegt. Enthält ein Flag, das verhindert, dass nachfolgende Aufforderungen an einen Administrator, eine bestimmte Aktion zu bestätigen, geöffnet werden, wenn der Administrator sie zuvor ausdrücklich abgelehnt hat. Wird nur in einem administrativen Bereich eines Geschäfts verwendet. Gilt nicht für Käufer.

#### `accordion-{VARIABLE}-{VARIABLE}`

Wird als Teil der Implementierung der Registerkarten-Funktionen nur in einem administrativen Bereich eines Stores verwendet. Gilt nicht für Käufer.

## Cookies in Recommendations für Produkte

![Adobe Commerce](../assets/adobe-logo.svg) (nur Adobe Commerce) Die folgenden Cookies werden von Produkt-Recommendations für Adobe Commerce-Kunden verwendet. Diese Cookies werden mit dem Modul [DataServices“ ](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/product-recommendations/getting-started/install-configure).

- `mg_dnt`: Ermöglicht es Ihnen[ die Datenerfassung in Adobe Commerce einzuschränken, ](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/product-recommendations/developer/setting-cookie) Sie benutzerdefinierten Code zur Verwaltung des Cookie-Einverständnisses auf Ihrer Site haben.
- `user_allowed_save_cookie`: Wird für den [Cookie-Einschränkungsmodus](#cookie-restriction-mode) verwendet.
- `authentication_flag`: Zeigt an, ob sich ein Käufer angemeldet oder abgemeldet hat. Dieses Cookie wird gleichzeitig mit dem `dataservices_customer_id`-Cookie aktualisiert.
- `dataservices_customer_id`: Zeigt an, ob sich ein Käufer angemeldet oder abgemeldet hat. Dieses Cookie enthält die eindeutige ID des Kunden im System.
- `dataservices_customer_group`: Gibt die Gruppe eines Kunden an. Dieses Cookie wird als [sha1](https://en.wikipedia.org/wiki/SHA-1) Prüfsumme der Gruppen-ID des Kunden gespeichert.
- `dataservices_cart_id`: Identifiziert Warenkorbaktionen eines Käufers. Dieses Cookie enthält die eindeutige Warenkorb-ID des Kunden im System.
- `dataservices_product_context`: Identifiziert die Produktinteraktionen eines Käufers. Dieses Cookie enthält die eindeutige Angebots-ID des Kunden im System.

## Zusätzliche Cookies

![Adobe Commerce](../assets/adobe-logo.svg) (nur Adobe Commerce) Die folgenden Cookies werden für Adobe Commerce-Kunden festgelegt. Diese Cookies werden mit dem Modul [DataServices“ ](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/product-recommendations/getting-started/install-configure).

- `mg`: Set von Snowplow JavaScript Tracker. Weitere Informationen finden Sie in der [Schneepflug-Dokumentation](https://docs.snowplow.io/docs/collecting-data/collecting-from-own-applications/javascript-trackers/web-tracker/tracker-setup/initialization-options).
- `com.adobe.alloy.getTld`: Angesichts des Hostnamens der aktuellen Web-Seite ist dies die oberste Domain, die kein „öffentliches Suffix“ ist, wie in https://publicsuffix.org beschrieben. Im Wesentlichen ist dies die Domain, die Cookies akzeptieren kann. Dieses Cookie ist Teil von [Alloy Web SDK](https://github.com/adobe/alloy).

[1]: https://developers.google.com/analytics/devguides/collection/analyticsjs/cookie-usage
[2]: https://support.google.com/adwords/answer/7521212
