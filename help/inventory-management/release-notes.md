---
title: '''[!DNL Inventory Management] Versionshinweise'
description: In den Versionshinweisen finden Sie Informationen zu allen [!DNL Inventory Management] veröffentlicht.
exl-id: 856b9503-7621-4beb-ac2f-3eb1a240cebc
feature: Inventory, Release Notes
source-git-commit: 01d8a1d50f574330f3ce7e8bf03a018f0079f5db
workflow-type: tm+mt
source-wordcount: '3445'
ht-degree: 0%

---

# [!DNL Inventory Management] Versionshinweise

Diese Versionshinweise beschreiben Versionen von [!DNL Inventory Management] und umfassen:

![Neu](../assets/new.svg) Neue Funktionen
![Problem behoben](../assets/fix.svg) Fehlerbehebungen und Verbesserungen
![Bekanntes Problem](../assets/bug.svg) Bekannte Probleme

[!DNL Inventory Management] ist ein Spezialprojekt der Magento Open Source Community Engineering, das Beitragenden offen steht. Informationen zur Teilnahme und zum Beitrag finden Sie im Abschnitt [GitHub-Projekt](https://github.com/magento/inventory) Repository und [Wiki](https://github.com/magento/inventory/wiki) um zu beginnen. Um das Projekt zu besprechen, nehmen Sie an der [Slack](https://magentocommeng.slack.com/?redir=%2Farchives%2FC5FU5E2HY) channel ([self-signup](https://opensource.magento.com/slack)).

[Veröffentlichungszeitplan](https://experienceleague.adobe.com/docs/commerce-operations/release/planning/schedule.html){target="_blank"} für unterstützte und kompatible Versionen.

## v1.2.7

[!DNL Inventory Management] 1.2.7 Versionshinweise sind im Abschnitt [Versionshinweise zu Core 2.4.7](https://experienceleague.adobe.com/en/docs/commerce-operations/release/notes/adobe-commerce/2-4-7#inventory-management-1).

## v1.2.6

[!DNL Inventory Management] 1.2.6 (Modulversion: `magento/inventory-metapackage = 1.2.6`) wird mit Version 2.4.6 unterstützt und ist mit Version 2.4.0 von Adobe Commerce, Adobe Commerce über Cloud-Infrastruktur und der Magento Open Source-Codebasis kompatibel.

![Problem behoben](../assets/fix.svg) Die Storefront zeigt jetzt zusammengesetzte Produkte (konfigurierbar, gebündelt und gruppiert) als vorrätig an, wenn untergeordnete Produkte, die ausverkauft waren, wieder vorrätig sind. Zuvor wurde in der Storefront darauf hingewiesen, dass das zusammengesetzte Produkt unter diesen Bedingungen nicht vorrätig war. <!-- ACP2E-1106-->

![Problem behoben](../assets/fix.svg) Konfigurierbare Produktoptionen werden jetzt wie erwartet auf der Storefront als nicht auf Lager angezeigt, wenn die Option mit einer auf 0 gesetzten Menge erstellt wurde und **[!UICONTROL Display out-of-stock products]** aktiviert ist. <!-- ACP2E-1148-->

![Problem behoben](../assets/fix.svg) Kategorieseiten-Caches werden nicht mehr invalidiert, wenn sich die Lagerbestandsmenge ändert und das Produkt noch auf Lager ist. Adobe Commerce lädt jetzt Seiten aus dem Cache, anstatt sie neu zu generieren, wenn sich die Produktmenge (und nichts anderes) auf der Seite &quot;Storefront-Kategorie&quot;ändert. <!-- ACP2E-118-->

![Problem behoben](../assets/fix.svg) Die Produktanzahl der Kategorielisten ist jetzt korrekt, wenn der Lagerbestand im Einzelquellenmodus mit der Variablen **[!UICONTROL Display Out-Of-Stock Products]** -Einstellung aktiviert. Adobe Commerce überprüft jetzt, ob ein Produkt beim Zählen verkauft werden kann. <!-- ACP2E-1033-->

![Problem behoben](../assets/fix.svg) Regeln zum Warenkorbpreis für die Bereitstellung im Store funktionieren jetzt erwartungsgemäß, wenn die Option &quot;Bestand&quot;aktiviert ist. Zuvor wurden durch Warenkorbpreisregeln generierte Rabatte unter diesen Bedingungen nicht angewendet. <!-- ACP2E-1015-->

![Problem behoben](../assets/fix.svg) Beim Aktualisieren des Produktinventars im terminierten Modus werden nicht mehr alle Caches gelöscht. Zuvor wurden alle Konfigurations-Caches vom Inventsindex gelöscht. <!-- ACP2E-1003-->

![Problem behoben](../assets/fix.svg) Der Wert für **[!UICONTROL Allow Multiple Boxes for Shipping]** -Attribut für ein Produkt im erweiterten Bestand wird jetzt erwartungsgemäß gespeichert. <!-- ACP2E-992-->

![Problem behoben](../assets/fix.svg) Adobe Commerce gibt nun eine genaue Reservierungsentschädigung nach einer teilweisen Rückerstattungskreditmeldung für eine Bestellung aus, die mit der Abholung im Geschäft aufgegeben wurde. Zuvor wurde eine falsche Reservierung im `inventory_reservation` Tabelle, wenn ein Admin-Benutzer ein Kreditmemwort erstellt hat, ohne die **[!UICONTROL Return to Stock]** aktivieren. <!-- ACP2E-979-->

![Problem behoben](../assets/fix.svg) Adobe Commerce zeigt konfigurierbare Produkte nicht mehr als vorrätig im Storefront an, wenn eine der Varianten in Implementierungen, die das Inventar aus mehreren Quellen implementieren, manuell auf Lager zurückgegeben wurde. <!-- ACP2E-952-->

![Problem behoben](../assets/fix.svg) Spaltenposition im Produktraster (**[!UICONTROL Catalog]** > **[!UICONTROL Products]**) wird nicht mehr auf die vorherige Position zurückgesetzt, nachdem die Seite in Implementierungen mit mehreren konfigurierten Inventarquellen neu geladen wurde. <!-- ACP2E-925-->

![Problem behoben](../assets/fix.svg) Die Lagermenge ist nun korrekt, nachdem ein Kreditmemo für ein virtuelles Produkt ausgestellt wurde, wenn die Variable **[!UICONTROL Back to stock]** nicht aktiviert ist. <!-- ACP2E-908-->

![Problem behoben](../assets/fix.svg) Sie können jetzt Kategorien mit automatischer Produktsortierung und Perimeter speichern, die nicht standardmäßigen Lagern zugewiesen sind. Zuvor hat Adobe Commerce die Kategorie nicht gespeichert und diesen Fehler angezeigt: `Something went wrong while saving the category`. <!-- ACP2E-859-->

![Problem behoben](../assets/fix.svg) Der konfigurierbare Status des Produktbestands wird jetzt erwartungsgemäß aktualisiert, wenn das Produkt mit allen konfigurierbaren nicht vorrätigen Varianten erstellt wird. <!-- ACP2E-813-->

![Problem behoben](../assets/fix.svg) Das Analyzer-Tool für inkonsistente Reservierungen funktioniert jetzt ordnungsgemäß mit teilweise versandten Bestellungen, die konfigurierbare, gebündelte und gruppierte Produkte enthalten. Zusammengesetzte Produktarten werden nun analysiert. Bisher wurden Stornierungen und Erstattungen nur für übergeordnete Produkte gespeichert, nicht für Teilproduktaufträge von konfigurierbaren und versandübergreifenden Bundle-Produkten. <!-- ACP2E-924-->

![Problem behoben](../assets/fix.svg) Adobe Commerce zeigt keinen Fehler mehr an, wenn ein Admin-Benutzer versucht, einem Lager oder Produkt 200 oder mehr Inventarquellen zuzuweisen. <!-- ACP2E-1180-->

![Problem behoben](../assets/fix.svg) Adobe Commerce unterstützt jetzt die Erstellung eines Kreditmemo für eine Bestellung, aus der ein Produkt gelöscht wurde. Zuvor konnten Händler kein Kreditmemo erstellen, wenn Produkte nach der Erstellung einer Rechnung aus der Bestellung gelöscht worden waren. Der Fehler wurde in der Anwendung angezeigt: `Following products with requested skus were not found: s00001`. t. <!-- ACP2E-1138-->

![Problem behoben](../assets/fix.svg) Stores werden jetzt sowohl anhand einzelner als auch anhand mehrerer Store-IDs gefiltert. Die `event` Der Liste der reservierten Attributcodes wurde der Produktattributcode hinzugefügt. Zuvor gab der Bericht &quot;Geringer Lagerbestand&quot;eine Ausnahme aus, wenn das Lagerbestandsmodul installiert wurde. <!-- ACP2E-1017-->

![Problem behoben](../assets/fix.svg) Layerte Navigationsfilter funktionieren jetzt erwartungsgemäß und nicht vorrätige Produkte werden jetzt an die Produktliste der Storefront-Kategorie angehängt. Die neue `is_out_of_stock` Sortierattribut verwendet das dynamische Elasticsearch-Feld-Mapper für die Storefront-Produktsammlung. <!-- ACP2E-748-->

![Problem behoben](../assets/fix.svg) Der Status des zusammengesetzten Produkts (Bundle, gruppiert und konfigurierbar) wird erwartungsgemäß aktualisiert, wenn der Status des untergeordneten Produktbestands durch ein REST geändert wird. `POST /rest/V1/inventory/source-items` aufrufen. <!-- ACP2E-1209-->

## v1.2.5

[!DNL Inventory Management] 1.2.5 (Modulversion: `magento/inventory-metapackage = 1.2.5`) wird mit Version 2.4.5 unterstützt und ist mit Version 2.4.0 von Adobe Commerce, Adobe Commerce über Cloud-Infrastruktur und der Magento Open Source-Codebasis kompatibel.

![Problem behoben](../assets/fix.svg) Der standardmäßige Lagerbestandsstatus von Bundles und gruppierten Produkten wird jetzt erwartungsgemäß aktualisiert, wenn ein Händler eine Sendung vom Administrator erstellt. Zuvor blieb der Status dieser Produkte nach der Entstehung einer Sendung unverändert. <!--- ACP2E-418-->

![Problem behoben](../assets/fix.svg) Konfigurierbare Produkte werden jetzt wieder auf Lager gebracht, wenn eine der folgenden Bedingungen erfüllt ist: 1. Das übergeordnete Produkt hat mindestens ein gespeichertes Kind auf Lager. 2. Das konfigurierbare Produkt selbst wurde aktualisiert und als **auf Lager** und hatte mindestens ein Kind auf Lager. <!--- ACP2E-443-->

![Problem behoben](../assets/fix.svg) Über die REST-API implementierte Lagerbestandsänderungen werden nun wie erwartet auf Produktdetailseiten angezeigt. Der Cache für Katalogprodukte wird jetzt bereinigt, nachdem der letzte und der aktuelle Lagerstatus verglichen wurden. Zuvor führte das Auslassen der Rückruffunktion zu einer fehlerhaften Bewertung von Bestandsstatusänderungen, wodurch die erforderliche Cache-Bereinigung nicht Trigger wurde. Infolgedessen spiegelt die Storefront die Bestandsänderungen nicht wider. <!--- ACP2E-161-->

![Problem behoben](../assets/fix.svg) Produkte, die dem Standardbestand zugewiesen sind und zuvor nicht vorrätig waren, sind jetzt auf der Storefront sichtbar, nachdem das Quellelement mit `/V1/inventory/source-items`. Zuvor hatte dieser REST-API-Endpunkt die falsche Einstellung festgelegt `stock_status`. <!--- ACP2E-562-->

![Problem behoben](../assets/fix.svg) Aufheben der Zuweisung von Inventarquellen durch Massenaktionen (**[!UICONTROL Catalog]** > **[!UICONTROL Products]** > **[!UICONTROL Select Products]** > **[!UICONTROL Actions - Unassign Inventory Source]**) funktioniert nun erwartungsgemäß, wenn Quellen SKUs enthalten, die mit Ausnahme einer vorangestellten Null Dubletten sind (z. B. `01234` und `1234`). Zuvor hat die Anwendung die Zuweisung von Inventarquellen nicht aufgehoben und einen Fehler ausgegeben. <!--- ACP2E-2641-->

![Problem behoben](../assets/fix.svg) Der Status des Produktbestands ist jetzt immer **auf Lager** auf der Storefront, wenn unendliche Rückbestellungen aktiviert sind und das Produkt einem benutzerdefinierten Lager zugewiesen wird, unabhängig von der zurückbestellten Menge. Zuvor waren die Produkte nicht mehr vorrätig, selbst wenn rückwirkende Bestellungen aktiviert waren. <!--- ACP2E-664-->

![Problem behoben](../assets/fix.svg) Konfigurierbarer übergeordneter und untergeordneter Produktbestand wird jetzt korrekt aktualisiert, nachdem das Quellelement mit `POST /V1/inventory/source-items`. Nachdem das untergeordnete Produkt über die API aktualisiert wurde, wird ein neues Inventar-Plug-in für standardmäßige Bestandskontrollen erstellt und die konfigurierbare Produktmenge und -status aktualisiert. <!--- ACP2E-442-->

![Problem behoben](../assets/fix.svg) Nicht vorrätige gruppierte Produkte werden nicht mehr auf der Seite &quot;Storefront-Kategorie&quot;aufgeführt. <!--- ACP2E-2082-->

![Problem behoben](../assets/fix.svg) Der Paketname in wurde korrigiert. `CatalogInventory` `composer.json`. <!--- ACP2E-2914-->

![Problem behoben](../assets/fix.svg) Der Status der Rückbestellung wird jetzt im Admin korrekt angezeigt, nachdem ein Produkt mit null Menge in einer Bereitstellung mit mehreren Quellen/Lagern bestellt wurde. [GitHub-33756](https://github.com/magento/magento2/issues/33756) <!--- ACP2E-713-->

![Problem behoben](../assets/fix.svg) Nicht vorrätige Bundle-Produkte werden nicht mehr auf der Seite &quot;Storefront-Kategorie&quot;angezeigt, wenn das Bundle-Produkt über den Abschnitt &quot;Lager&quot;aktualisiert wird. <!--- ACP2E-2012-->

![Problem behoben](../assets/fix.svg) Kompatibilitätsprobleme mit PHP 7.4 wurden behoben. <!--- AC-3192-->

![Problem behoben](../assets/fix.svg) Die Leistung von Speichervorgängen, die Bundle-Produkte mit vielen Optionen enthalten (mehrere 100), wurde verbessert. Bisher dauerte das Speichern dieser großen Bundle-Produkte einige Minuten und führte manchmal zu Zeitüberschreitungen bei Implementierungen mit aktivierten Lagerbestandsdiensten. [GitHub-34732](https://github.com/magento/magento2/issues/34732) <!--- AC-1901-->

![Problem behoben](../assets/fix.svg) Das Massen-Aktionstool für Produkte (**[!UICONTROL Select Products]** > **[!UICONTROL Actions]** > **[!UICONTROL Assign Inventory Source]**) funktioniert jetzt erwartungsgemäß bei der Zuweisung einer Inventarquelle zu mehreren Produkten, wenn SKUs dupliziert werden, mit Ausnahme einer führenden `0` (zum Beispiel: `01234` und `1234`). Zuvor wurde nur einem Produkt eine Lagerbestandsquelle zugewiesen. [GitHub-35171](https://github.com/magento/magento2/issues/35171) <!--- AC-2584-->

![Problem behoben](../assets/fix.svg) Die `ProductInterface.only_x_left_in_stock` -Feld gibt jetzt 0 zurück, wenn der Bestand 0 ist. Zuvor wurde null zurückgegeben. [GitHub-29932](https://github.com/magento/magento2/issues/29932) <!--- AC-1806-->

![Problem behoben](../assets/fix.svg) Sie können jetzt den Standardbestand über den Administrator bearbeiten **[!UICONTROL Stores]** > **[!UICONTROL Inventory]** > **[!UICONTROL Stocks]**. Zuvor wurde in der Konsole ein JavaScript-Fehler angezeigt, als Sie versuchten, Quellen aus dem Standardbestand hinzuzufügen oder daraus zu entfernen. Sie konnten jedoch Websites einem Standardbestand zuweisen. <!--- ACP2E-545-->

![Problem behoben](../assets/fix.svg) <!--- ACP2E-274--> Die Produktanzahl der Kategorielisten ist jetzt korrekt, wenn der Inventar-Einzelquellenmodus mit der **[!UICONTROL Display Out-Of-Stock Products]** -Einstellung aktiviert. Ein neues Plug-in verwendet jetzt `AreProductsSalableInterface` und `StockConfigurationInterface` zur Bestimmung der Gesamtanzahl der Produkte. Zuvor gab die Produktliste der Kategorie die falsche Produktmenge zurück.

![Problem behoben](../assets/fix.svg) <!--- ACP2E-322--> Konfigurierbare Produkte werden jetzt an die letzte Position in der Produktliste verschoben, nachdem der Lagerbestand aktualisiert wurde. **[!UICONTROL Move out of stock to the bottom]** -Einstellung aktiviert ist. Eine neue benutzerdefinierte Datenbankabfrage wird implementiert, um die Sortierreihenfolge von Elasticsearch-Indizes zu umkehren, wodurch die Admin-aktivierte Sortierreihenfolge ignoriert wird. Zuvor wurden konfigurierbare Produkte und ihre untergeordneten Produkte nicht an den unteren Rand der Liste verschoben, wenn diese Einstellung aktiviert war.

## v1.2.4

Inventory management 1.2.4 (Modulversion: `magento/inventory-metapackage = 1.2.4`) wird mit Version 2.4.4 unterstützt und ist mit Version 2.4.0 von Adobe Commerce, Adobe Commerce über Cloud-Infrastruktur und der Magento Open Source-Codebasis kompatibel.

![Problem behoben](../assets/fix.svg) In der Admin-Produktlistenansicht zeigt Commerce jetzt einen genauen Wert für die Verkaufsmenge aller Produkte an. Zuvor wurde ein leerer Wert für die verkaufbare Menge von Produkten auf Lager mit SKUs angezeigt, die Sonderzeichen enthielten. <!--- MC-41936-->

![Problem behoben](../assets/fix.svg) Die Leistung wurde bei Warenkorb- und Checkout-Aktionen verbessert, z. B. beim Hinzufügen von Produkten zum Warenkorb in Bereitstellungen mit vielen (etwa 10.000) Inventarquellen. <!--- MC-42570-->

![Problem behoben](../assets/fix.svg) Die `bin/magento inventory:reservation:list-inconsistencies` -Befehl verarbeitet jetzt Bestellungen mit Teillieferungen korrekt, auch wenn die Reservierungen aus der Datenbank fehlen und der Cache gelöscht wurde. Zuvor wurde bei der Ausführung dieses Befehls mit einem vorab geleerten Cache der folgende Fehler in Commerce angezeigt: `Area code is not set`. <!--- MC-42142-->

![Problem behoben](../assets/fix.svg) Inkrementelle Indizierung von gruppierten Produkt-Kindprodukten führt nicht mehr dazu, dass andere gruppierte Produkte falsch indiziert werden, wenn untergeordnete Elemente freigegeben werden. <!--- MC-41963-->

![Problem behoben](../assets/fix.svg) Auf der Seite zur Storefront-Kategorie wird nun die richtige Produktanzahl angezeigt, nachdem ein Produkt nach API aus einer Kategorie entfernt wurde. Zuvor war die Produktanzahl der Kategorieseiten bis zur Neuindizierung falsch. <!--- MC-42287-->

![Problem behoben](../assets/fix.svg) Konfigurierbare Produkte können jetzt beim Erstellen eines Kreditmemos an Lager zurückgegeben werden, wenn die Variable **[!UICONTROL Manage Stock]** deaktiviert ist. Zuvor zeigte Commerce nicht die **Zurück zum Lager** auf der Seite zur Erstellung von Credit Memos, wenn diese Option deaktiviert war. <!--- MC-42002-->

![Problem behoben](../assets/fix.svg) Die Verwaltung des Lagerbestands, der mehr als 10.000 Artikel umfasst, wurde verbessert. Bisher konnten Kaufleute aufgrund von Leistungsproblemen manchmal keine Lagerbestände in der Admin-Konsole bearbeiten, bevor sie ihre Website aufriefen. <!--- MC-42643-->

![Problem behoben](../assets/fix.svg) Die **[!UICONTROL User Roles]** -Seite in Admin aktualisiert, um Administratoren eingeschränkten Zugriff auf die Konfiguration der Versandmethoden zu gewähren. Die _Versandmethoden_ wurde in _[!UICONTROL Delivery methods]_, und_[!UICONTROL In-Store Pickup]_ wird unter dem _[!UICONTROL Delivery methods]_Abschnitt. [GitHub-30053](https://github.com/magento/magento2/issues/30053)  <!--- MC-41545-->

![Problem behoben](../assets/fix.svg) Adobe Commerce erstellt keine doppelte Produktreservierung mehr, nachdem ein Kreditmemo von der API aktualisiert wurde. <!--- MC-41757-->

![Problem behoben](../assets/fix.svg) Wechseln von der _[!UICONTROL Pick up in Store]_zum_[!UICONTROL Shipping]_ im Checkout-Workflow wird kein JavaScript-Fehler mehr Trigger, wenn nur die In-Store-Abruf-Bereitstellung verfügbar ist. <!--- MC-42808-->

![Problem behoben](../assets/fix.svg) Verkaufbare Produktmenge und Lagerproduktmenge werden jetzt korrekt synchronisiert. Zuvor wurde die Bestandserhaltungskompensation für stornierte Bestellungen nicht neu erstellt. <!--- MC-42485-->

![Problem behoben](../assets/fix.svg) Die Leistung des Validators wurde optimiert, um zu verhindern, dass dem untergeordneten Produkt eines gebündelten Produkts eine neue Quelle mit dem Versandtyp hinzugefügt wird. `Ship Together`. <!--- MC-43039-->

## 1.2.3

[!DNL Inventory Management] 1.2.3 (Modulversion: `magento/inventory-metapackage = 1.2.3`) wird mit Version 2.4.3 unterstützt und ist mit Version 2.4.0 von Adobe Commerce, Adobe Commerce über Cloud-Infrastruktur und der Magento Open Source-Codebasis kompatibel.

![Problem behoben](../assets/fix.svg) Fehlerkorrektur - diverse Probleme im Zusammenhang mit der Sichtbarkeit von zusammengesetzten Produkten auf der Vorderseite wurden behoben.

![Problem behoben](../assets/fix.svg) Verbesserte Leistung bei der Verwaltung von Warenkorbseiten mit der erforderlichen Mindestmenge.

![Problem behoben](../assets/fix.svg) Verschiedene Fehlerbehebungen wurden vorgenommen, um Probleme mit der Quellerstellung, nicht vorrätigen Artikeln, der Lagerbestandsbeschaffung, der Sortierung zugewiesener Quellen, der In-Store-Bereitstellung und den Lagerbestandsbefehlen zu beheben.

![Problem behoben](../assets/fix.svg) [!DNL Commerce] unterstützt jetzt dreistellige kanadische Postleitzahlen für den In-store-Versand. Sechstellige Codes werden aufgrund von Einschränkungen, die durch `geonames.org`.

![Problem behoben](../assets/fix.svg) Der Administrator zeigt nun die richtige Menge an Standardbestand für deaktivierte Produkte auf der **Produkte** und **Produkt bearbeiten** Seite für Bereitstellungen mit mehreren Stores.

![Problem behoben](../assets/fix.svg) [!DNL Commerce] aktualisiert jetzt den Kategorieprodukt-Cache, wenn ein Bundle-Produkt wieder vorrätig ist.

## 1.2.2

[!DNL Inventory Management] 1.2.2 (Modulversion: `magento/inventory-metapackage = 1.2.2`) wird mit Version 2.4.2 unterstützt und ist mit Version 2.4.0 von Adobe Commerce, Adobe Commerce über Cloud-Infrastruktur und der Magento Open Source-Codebasis kompatibel.

![Problem behoben](../assets/fix.svg) Fehlerkorrektur - diverse Probleme im Zusammenhang mit der Sichtbarkeit von zusammengesetzten Produkten auf der Vorderseite wurden behoben.

![Problem behoben](../assets/fix.svg) Verbesserte Leistung der Warenkorbseiten bei der Mengenaktualisierung auf B2B.

![Problem behoben](../assets/fix.svg) Verschiedene Fehlerbehebungen zur Behebung von Problemen bei der In-Store-Übernahme, Massenaktualisierung und Inventarschwelle.

![Neu](../assets/new.svg) **Funktionstests.** Es wurden neue Funktionstests eingeführt und Fehlerbehebungen für bestehende Tests bereitgestellt, um sie stabiler zu machen.

## 1.2.1

[!DNL Inventory Management] 1.2.1 (Modulversion: `magento/inventory-metapackage = 1.2.1`) wird mit Version 2.4.1 unterstützt und ist mit Version 2.4.0 von Adobe Commerce, Adobe Commerce über Cloud-Infrastruktur und der Magento Open Source-Codebasis kompatibel.

![Problem behoben](../assets/fix.svg) Es wurde ein bekanntes Problem im Zusammenhang mit der `inventory_cleanup_reservations` Cron-Auftrag und ein Problem im Zusammenhang mit der In-Store-Abholfunktion für Bundle-Produkte behoben. Dieses Update umfasst auch allgemeine Verbesserungen bei der Berechnung von Lagerbeständen, der Unterstützung von Bundle-Produkten und der Backorder-Funktionalität.

![Neu](../assets/new.svg) **Funktionstests.** Es wurden neue Funktionstests eingeführt, die zusätzliche Unterstützung für die In-Store-Abruf-Funktion bieten.

## 1,2,0

[!DNL Inventory Management] 1.2.0 (Modulversion: `magento/inventory-metapackage = 1.2.0`) wird in Version 2.4.0 von Adobe Commerce, Adobe Commerce in der Cloud-Infrastruktur und der Magento Open Source-Codebasis unterstützt.

![Problem behoben](../assets/fix.svg) Zahlreiche Fehlerbehebungen zur Lösung von Problemen mit der Quellzuweisung, der Unterstützung skalierbarer Umgebungsfunktionen und der Kompatibilität mit PHP 7.4, MySQL 8 und PHPUNIT 9.

![Neu](../assets/new.svg) **Versandmethode im Store.** Es wurde eine Option hinzugefügt, mit der Benutzer eine Quelle auswählen können, die beim Checkout als Abmeldeort verwendet werden soll. Siehe [In-store-Bereitstellung](../stores-purchase/shipping-in-store-delivery.md) im _Handbuch für Verkaufs- und Kauferlebnisse_.

![Neu](../assets/new.svg) **Bundle-Produktunterstützung für den Multi-Source-Modus.** Das Inventar unterstützt alle Produktarten mit mehreren Quellen.

![Neu](../assets/new.svg) **Asynchrone Neuindizierung des Lagers.** Die Möglichkeit zur asynchronen Neuindizierung von Lagern wurde hinzugefügt und die Leistung verschiedener kritischer Szenarien wurde verbessert.

![Neu](../assets/new.svg) **Massenschnittstellen.** Neue Bulk-Schnittstellen für die Veräußerbarkeitsprüfung eingeführt: `\Magento\InventorySalesApi\Api\AreProductsSalableInterface`, `\Magento\InventorySalesApi\Api\AreProductsSalableForRequestedQtyInterface`.

![Neu](../assets/new.svg) **Verbesserte Testabdeckung.** Die neue Funktionalität wird durch automatisierte Tests abgedeckt, einschließlich erweiterter Abdeckung für erkannte und behobene Probleme.

![Bekanntes Problem](../assets/bug.svg) **Bekanntes Problem.** Das Fehlen der `object_id` -Feld in den Metadaten der Vorbehalte verhindert die `inventory_cleanup_reservations` Cron-Auftrag funktioniert nicht ordnungsgemäß. Dieses Problem wurde in [magento/inventory#3046](https://github.com/magento/inventory/pull/3046).

**Problemumgehung:** Führen Sie die folgenden MySQL-Abfragen aus, um Reservierungen manuell zu bereinigen:

```sql
SELECT GROUP_CONCAT(reservation_id) FROM inventory_reservation GROUP BY stock_id, sku HAVING SUM(quantity) = 0;
DELETE FROM inventory_reservation where reservation_id IN (result_of_the_first_query);
```

## 1.1.6

[!DNL Inventory Management] 1.1.6 (Modulversion: `inventory-composer-metapackage = 1.1.6`) wird mit Version 2.3.6 unterstützt und ist mit den Versionen 2.3.5, 2.3.4, 2.3.3, 2.3.2, 2.3.1 und 2.3.0 von Adobe Commerce, Adobe Commerce auf Cloud-Infrastruktur und der Magento Open Source-Codebasis kompatibel.

![Problem behoben](../assets/fix.svg) Fehlerbehebungen im Zusammenhang mit Rückständen, Kreditmemos, einem Raster für niedrige Lagerbestände, Fehlerbehebungen im Zusammenhang mit dem CLI-Tool &quot;Inkonsistenzen aufheben&quot;und allgemeinen Verbesserungen.

![Neu](../assets/new.svg) **Asynchrone Neuindizierung des Lagers.** Die Möglichkeit zur asynchronen Neuindizierung von Lagern wurde hinzugefügt und die Leistung verschiedener kritischer Szenarien wurde verbessert.

## 1,1,5

[!DNL Inventory Management] 1.1.5 (Modulversion: `inventory-composer-metapackage = 1.1.5`) wird mit Version 2.3.5 unterstützt und ist mit den Versionen 2.3.4, 2.3.3, 2.3.2, 2.3.1 und 2.3.0 von Adobe Commerce, Adobe Commerce über die Cloud-Infrastruktur und die Magento Open Source-Codebasis kompatibel.

![Neu](../assets/new.svg) **Aktualisieren Sie den Bestand, sobald die Produkt-SKU geändert wurde.** Es wurde eine neue Konfigurationseinstellung eingeführt, um zum neuen Verhalten zu wechseln: &quot;Mit Katalog synchronisieren&quot;.

![Neu](../assets/new.svg) **Funktionstests.** Einführung neuer Funktionstests zur Beseitigung der Testabdeckung. Fehlerkorrektur - Tests sind jetzt stabiler und zuverlässiger.

![Bekanntes Problem](../assets/bug.svg) Fehlerbehebungen, die verhindern sollen, dass Produkte überverkauft werden, die auf der Storefront sichtbar sind, und zahlreiche Fehlerbehebungen für skalierbare Umgebungsunterstützung sowie Verbesserungen der Benutzeroberfläche.

## 1.1.4

[!DNL Inventory Management] 1.1.4 (Modulversion: `inventory-composer-metapackage = 1.1.4`) wird in Version 2.3.4 unterstützt und ist mit den Versionen 2.3.3, 2.3.2, 2.3.1 und 2.3.0 von Adobe Commerce, Adobe Commerce in der Cloud-Infrastruktur und der Magento Open Source-Codebasis kompatibel.

![Problem behoben ](../assets/fix.svg)**Verbesserte Leistung.** Es wurde eine Bundching-Logik für den CLI-Befehl &quot;Inventarreservierungen&quot;eingeführt, um die Speichernutzung zu reduzieren und Fälle zu vermeiden, in denen der Prozess ohne Antwort blockiert wird.

![Neu ](../assets/new.svg)**Verbesserte Testabdeckung.** Es wurden viele neue Funktionstests eingeführt. Fast alle manuellen Inventarszenarien werden mit automatisierten Tests abgedeckt.

![Bekanntes Problem](../assets/bug.svg) Zahlreiche Fehlerbehebungen zur Behebung von Problemen mit Kreditmemos, gruppierten Produkten sowie Massenaktionen von Quelle und Lager.

## 1.1.3

[!DNL Inventory Management] 1.1.3 (Modulversion: `inventory-composer-metapackage = 1.1.3`) wird mit Version 2.3.3 unterstützt und ist mit den Versionen 2.3.2, 2.3.1 und 2.3.0 von Adobe Commerce, Adobe Commerce über die Cloud-Infrastruktur und die Magento Open Source-Codebasis kompatibel.

![Problem behoben ](../assets/fix.svg)**Bessere Integration in Adobe Commerce- und B2B-Funktionen.** [!DNL Inventory Management] funktioniert jetzt ordnungsgemäß mit den folgenden Funktionen für Websites, die nicht standardmäßige Inventarquellen und -bestände verwenden:

- Bestellung nach SKU (Adobe Commerce)
- Schnellbestellung (B2B)
- Anforderungslisten (B2B)

![Neu ](../assets/new.svg)**Verbesserte Leistung.** Die Browserleistung des Storefront-Katalogs wurde für Websites verbessert, auf denen der standardmäßige Lagerbestand und die Standardquelle ausgeführt werden.

![Neu ](../assets/new.svg)**Verbesserte Testabdeckung.** Die automatisierte Funktions- und Integrationstest-Abdeckung wurde deutlich erhöht.

## 1.1.2

[!DNL Inventory Management] 1.1.2 (Modulversion: `inventory-composer-metapackage = 1.1.2`) wird mit Version 2.3.2 unterstützt und ist mit den Versionen 2.3.1 und 2.3.0 von Adobe Commerce, Adobe Commerce über Cloud-Infrastruktur und der Magento Open Source-Codebasis kompatibel.

![Problem behoben](../assets/fix.svg) hinzugefügt `source_code` auf die Antwort für die GET `/V1/shipments` REST-Endpunkt. <!-- https://github.com/magento/inventory/pull/2142 -->

![Problem behoben](../assets/fix.svg) Es wurde ein Problem behoben, das dazu führte, dass Reservierungen korrekt gelöscht und die Produktmengen aktualisiert wurden, nachdem ein Kreditmemo für eine nicht versandte Bestellung ausgestellt wurde. Wenn Sie die Option zum <!-- https://github.com/magento/inventory/pull/2179 -->

![Problem behoben](../assets/fix.svg) Es wurde ein Problem behoben, durch das beim Eingeben von Mengen während der Produkterstellung Menge für konfigurierbare untergeordnete Produkte korrekt gespart wurde. <!-- https://github.com/magento/inventory/pull/2158 -->

Neue Module für [!DNL Inventory Management] 1.1.2 Beta beinhaltet:

```php
        'Magento_InventoryGraphQl' => 1,
        'Magento_InventoryReservations' => 1,
        'Magento_InventoryReservationsApi' => 1,
        'Magento_InventoryReservationCli' => 1,
        'Magento_InventoryExportStock' => 0,
        'Magento_InventoryExportStockApi' => 0,
```

![Neu](../assets/new.svg) **Es wurde ein Batch-Teilbestand-Transfer-Endpunkt hinzugefügt** - Aktuelle Massen-Transfer-Endpunkte verschieben alle zugewiesenen Mengen von einer Quelle in eine Zielquelle. Die neue `/rest/V1/inventory/bulk-partial-source-transfer` -Endpunkt ermöglicht Händlern die Übertragung eines Teilbestands von der Quelle an die Quelle als Massenvorgang. Um eine bestimmte Menge zu übertragen, geben Sie eine Anfrage an den -Endpunkt mit der `sku`, `qty`, `origin_source_code`, und `destination_source_code`. Übertragungen überprüfen, ob die Quelle der `sku`, gibt es genügend Menge für die Übertragung usw. Siehe [Massenaktionen im Inventar](https://developer.adobe.com/commerce/webapi/rest/inventory/bulk-inventory/){target="_blank"} in der REST-API-Dokumentation. <!-- https://github.com/magento/inventory/pull/2117 -->

![Neu](../assets/new.svg) **Reservierungs-CLI hinzugefügt** - Neue Befehle geben Ihnen Optionen, um Reservierungsinkonsistenzen zu erkennen und zu beheben. Wenn Bestellungen übermittelt werden und sich der Status ändert, [!DNL Inventory Management] generiert erste Reservierungen und Aktualisierungen durch Ausgleichsreservierungen. Diese Befehle geben eine Liste der erkannten Inkonsistenzen nach Bestell-ID, SKU und Lager-ID zurück und erstellen Vorbehalte, die aufgelöst werden können. Siehe [CLI-Referenz](cli.md) für weitere Informationen. <!-- https://github.com/magento/inventory/pull/2199 https://github.com/magento/inventory/pull/2184 https://github.com/magento/inventory/pull/2171 https://github.com/magento/inventory/pull/2148  -->

![Neu](../assets/new.svg) **Leistungsverbesserungen für Quellen und SSA-Optionen** - Die Sortierung und Auswahl von Quellen während des Versands führte zu Leistungseinbußen bei Beständen mit einer hohen Anzahl von Quellen. Diese Version bietet wesentliche Leistungsverbesserungen bei der Auflistung und Sortierung der verfügbaren Quellen bei der Überprüfung und Auswahl von SSA-Optionen in Sendungen. <!-- https://github.com/magento/inventory/pull/2056 https://github.com/magento/inventory/pull/2090 -->

![Neu](../assets/new.svg) **GraphQL-Unterstützung für Inventory management hinzugefügt** - Mit dieser Version wird eine neue `magento/module-inventory-graph-ql` -Modul. Die GraphQL [ProductInterface-Attribute](https://developer.adobe.com/commerce/webapi/graphql/schema/products/interfaces/attributes/){target="_blank"} enthält jetzt `only_x_left_in_stock` und `stock_status` -Attribute für [!DNL Inventory Management] unterstützen. <!-- https://github.com/magento/inventory/pull/2124 -->

![Neu](../assets/new.svg) **Vereinfachte Benutzeroberfläche für zugewiesene Quellen** - Die Tabelle Zugewiesene Quellen auf Produktseiten enthält vereinfachte Inhalte für einfachere Aktualisierungen und verbesserte Leistung bei der Anzeige vieler Quellen. Liste aller Quellen nach Quellname (Bewegen Sie den Mauszeiger über `source_code`).

![Neu](../assets/new.svg) **Export Aggregated Stock Service** - Diese Version bietet einen neuen exportaggregierten Lagerdienst (Reservierungen im System beibehalten), der externe Sales Channel wie Amazon, eBay und Google Shopping-Anzeigen unterstützt.  <!-- https://github.com/magento/inventory/pull/2067 -->

## 1.1.0

[!DNL Inventory Management] 1.1.0 (Modulversion: `inventory-composer-metapackage = 1.1.0`) wird unterstützt und ist mit Version 2.3.0 von Adobe Commerce, Adobe Commerce über die Cloud-Infrastruktur und der Magento Open Source-Codebasis kompatibel. [!DNL Inventory Management] 1.1.1 wird nur als Update für Paketnamen veröffentlicht, unterstützt für Version 2.3.1 und kompatibel mit Version 2.3.0 von Adobe Commerce, Adobe Commerce in der Cloud-Infrastruktur und der Magento Open Source-Codebasis.

![Problem behoben](../assets/fix.svg) **Zusätzliche Unterstützung für Elasticsearch für Einzel- und Multi-Source-Modi** — Sie können jetzt Elasticsearch mit benutzerdefinierten Lagern konfigurieren und verwenden. Siehe [Elasticsearch-Dienst einrichten](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure/service/elasticsearch.html){target="_blank"} für Installationsinformationen. <!-- PR https://github.com/magento/inventory/pull/1943 -->

![Problem behoben](../assets/fix.svg) Es wurden Leistungsprobleme mit Standard Stock behoben, um die Leistung bei zahlreichen Vorgängen drastisch zu steigern. Verbesserungen verbessern die Leistung für Einzelquellenmodi, Übertragen des Bestands an die Quelle, Storefront-Kategorieseiten und Berechnungen der Verkaufsmenge.

<!-- All Performance Track issues resolved https://github.com/magento/inventory/issues?q=is%3Aopen+is%3Aissue+label%3APerformance -->

![Problem behoben](../assets/fix.svg) Es wurden Probleme mit dem Status &quot;Nicht auf Lager&quot;und der Massenbestandsübertragung auf Lager für konfigurierbare und gruppierte Produkte behoben. Die Auswahl der übergeordneten Produkte und die Durchführung von Massenaktionen wirken sich nicht auf den Produktstatus aus. Wenn das übergeordnete Produkt auf Lager war, bleibt es auf Lager.

<!-- PR https://github.com/magento/inventory/pull/1972 -->

![Neu](../assets/new.svg) **Distance Priority Algorithm** — Der Distance Priority Algorithm ist ein neuer, vordefinierter Quellauswahlalgorithmus für entfernungsbasierte Versandempfehlungen. Dieser Algorithmus vergleicht den Speicherort der Lieferzieladresse mit den Quellspeicherorten, um die nächstgelegene Quelle zu bestimmen, aus der Sendungen durchgeführt werden können. Der Abstand kann entweder durch die physische Entfernung oder die auf Reisen von einem Ort zum anderen verbrachte Zeit bestimmt werden, indem importierte Geocode-Standortdaten oder Google-Anweisungen (Fahren, Gehen oder Fahrradfahren) verwendet werden.

![Neu](../assets/new.svg) **Erweiterte Liste der Quellmengen** — Händler mit einer großen Anzahl von Quellen können einfach alle Quellen pro Produkt über das Produktraster bewegen und anzeigen. Jedes Produkt zeigt mindestens fünf Quellen und entsprechende Mengen an. Wenn Sie den Mauszeiger über die Quellen bewegen, können Sie durch die gesamte Liste der Quellen und aktuellen Mengen blättern.

![Bekanntes Problem](../assets/bug.svg) Bekanntes Problem mit Magento Open Source und Adobe Commerce v2.3.1 - Beim asynchronen Migrieren von Daten zwischen Quellen treten Probleme auf, die auf Änderungen in asynchronen APIs zurückzuführen sind, bei denen Themennamen die PHP-Klasse und Methodennamen widerspiegeln. Verwenden synchroner Vorgänge, Festlegen von **[!UICONTROL Run asynchronously]** nach `No`wird empfohlen.
