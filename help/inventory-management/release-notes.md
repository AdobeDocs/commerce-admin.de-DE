---
title: '[!DNL Inventory Management] Versionshinweise'
description: Informationen zu allen [!DNL Inventory Management] Versionen finden Sie in den Versionshinweisen .
exl-id: 856b9503-7621-4beb-ac2f-3eb1a240cebc
feature: Inventory, Release Notes
source-git-commit: 01d8a1d50f574330f3ce7e8bf03a018f0079f5db
workflow-type: tm+mt
source-wordcount: '3445'
ht-degree: 0%

---

# [!DNL Inventory Management] Versionshinweise

Diese Versionshinweise beschreiben die Versionen von [!DNL Inventory Management] und umfassen:

![Neu](../assets/new.svg) Neue Funktionen
![Korrektur des Problems](../assets/fix.svg) Fehlerbehebungen und Verbesserungen
![Bekanntes Problem](../assets/bug.svg) Bekannte Probleme

[!DNL Inventory Management] ist ein Magento Open Source Community Engineering-Sonderprojekt, das Beitragenden offen steht. Informationen zu den ersten Schritten finden Sie im Repository [GitHub-Projekt](https://github.com/magento/inventory) und im Repository [wiki](https://github.com/magento/inventory/wiki) , um sich daran zu beteiligen und beizutragen. Um das Projekt zu besprechen, schließen Sie sich dem Kanal [Slack](https://magentocommeng.slack.com/?redir=%2Farchives%2FC5FU5E2HY) an ([self-signup](https://opensource.magento.com/slack)).

[Veröffentlichungsplan](https://experienceleague.adobe.com/docs/commerce-operations/release/planning/schedule.html){target="_blank"} für unterstützte und kompatible Versionen.

## v1.2.7

[!DNL Inventory Management] 1.2.7 Versionshinweise sind in den [Core 2.4.7 Versionshinweisen](https://experienceleague.adobe.com/en/docs/commerce-operations/release/notes/adobe-commerce/2-4-7#inventory-management-1) enthalten.

## v1.2.6

[!DNL Inventory Management] 1.2.6 (Modulversion: `magento/inventory-metapackage = 1.2.6`) wird mit Version 2.4.6 unterstützt und ist mit Version 2.4.0 von Adobe Commerce, Adobe Commerce über die Cloud-Infrastruktur und der Magento Open Source-Codebasis kompatibel.

![Problem behoben](../assets/fix.svg) Die Storefront zeigt jetzt zusammengesetzte Produkte (konfigurierbar, gebündelt und gruppiert) als vorrätig an, wenn untergeordnete Produkte, die ausverkauft waren, wieder vorrätig sind. Zuvor wurde in der Storefront darauf hingewiesen, dass das zusammengesetzte Produkt unter diesen Bedingungen nicht vorrätig war. <!-- ACP2E-1106-->

![Korrektur des Fehlers](../assets/fix.svg) Konfigurierbare Produktoptionen werden jetzt wie erwartet auf der Storefront als nicht vorrätig angezeigt, wenn die Option mit einer auf 0 und 2 festgelegten Menge erstellt wurde. <!-- ACP2E-1148-->**[!UICONTROL Display out-of-stock products]**

![Problem behoben](../assets/fix.svg) Kategorieseitenzwischenspeicher werden nicht mehr invalidiert, wenn sich die Lagerbestandsmenge ändert und das Produkt noch auf Lager ist. Adobe Commerce lädt jetzt Seiten aus dem Cache, anstatt sie neu zu generieren, wenn sich die Produktmenge (und nichts anderes) auf der Seite &quot;Storefront-Kategorie&quot;ändert. <!-- ACP2E-118-->

![Problem behoben](../assets/fix.svg) Die Produktanzahl der Kategorienliste ist jetzt korrekt, wenn die Einstellung **[!UICONTROL Display Out-Of-Stock Products]** im Einzelquellenmodus verwendet wird. Adobe Commerce überprüft jetzt, ob ein Produkt beim Zählen verkauft werden kann. <!-- ACP2E-1033-->

![Korrektur des Fehlers](../assets/fix.svg) Regeln zum Warenkorbpreis für die In-Store-Bereitstellung funktionieren jetzt wie erwartet, wenn der Bestand aktiviert ist. Zuvor wurden durch Warenkorbpreisregeln generierte Rabatte unter diesen Bedingungen nicht angewendet. <!-- ACP2E-1015-->

![Korrektur des Problems](../assets/fix.svg) Beim Aktualisieren des Produktinventars im terminierten Modus werden nicht mehr alle Caches gelöscht. Zuvor wurden alle Konfigurations-Caches vom Inventsindex gelöscht. <!-- ACP2E-1003-->

![Problem behoben](../assets/fix.svg) Der Wert für das Attribut **[!UICONTROL Allow Multiple Boxes for Shipping]** für ein Produkt im erweiterten Bestand wird jetzt erwartungsgemäß gespeichert. <!-- ACP2E-992-->

![Korrektur des Fehlers](../assets/fix.svg) Adobe Commerce gibt jetzt nach einem Teil-Rückerstattungskreditvermerk für eine Bestellung, die mit der In-store-Abholung aufgegeben wurde, eine genaue Reservierungsentschädigung aus. Zuvor wurde eine falsche Reservierung in der Tabelle `inventory_reservation` gespeichert, wenn ein Admin-Benutzer ein Kreditmemo erstellt hat, ohne das Kontrollkästchen **[!UICONTROL Return to Stock]** zu aktivieren. <!-- ACP2E-979-->

![Korrektur des Fehlers](../assets/fix.svg) Adobe Commerce zeigt konfigurierbare Produkte nicht mehr als nicht vorrätig auf der Storefront an, wenn eine der Varianten in Implementierungen, die den Inventar aus mehreren Quellen implementieren, manuell auf Lager zurückgegeben wurde. <!-- ACP2E-952-->

![Korrektur des Problems](../assets/fix.svg): Die Spaltenposition im Produktraster (**[!UICONTROL Catalog]** > **[!UICONTROL Products]**) kehrt nicht mehr zur vorherigen Position zurück, nachdem die Seite in Bereitstellungen mit mehreren konfigurierten Inventarquellen neu geladen wurde. <!-- ACP2E-925-->

![Problem behoben](../assets/fix.svg) Die Lagermenge ist jetzt korrekt, nachdem ein Kreditmemo für ein virtuelles Produkt ausgestellt wurde, wenn das Kontrollkästchen **[!UICONTROL Back to stock]** nicht aktiviert ist. <!-- ACP2E-908-->

![Problem behoben](../assets/fix.svg) Sie können jetzt Kategorien mit automatischer Produktsortierung und Umfang speichern, die nicht standardmäßigen Beständen zugewiesen sind. Zuvor hat Adobe Commerce die Kategorie nicht gespeichert und diesen Fehler angezeigt: `Something went wrong while saving the category`. <!-- ACP2E-859-->

![Korrektur des Problems](../assets/fix.svg) Der konfigurierbare Status des Produktbestands wird jetzt erwartungsgemäß aktualisiert, wenn das Produkt mit allen konfigurierbaren nicht vorrätigen Varianten erstellt wird. <!-- ACP2E-813-->

![Korrektur des Fehlers](../assets/fix.svg) Das Analyzer für Reservierungsinkonsistenzen funktioniert jetzt ordnungsgemäß mit teilweise versandten Bestellungen, die konfigurierbare, gebündelte und gruppierte Produkte enthalten. Zusammengesetzte Produktarten werden nun analysiert. Bisher wurden Stornierungen und Erstattungen nur für übergeordnete Produkte gespeichert, nicht für Teilproduktaufträge von konfigurierbaren und versandübergreifenden Bundle-Produkten. <!-- ACP2E-924-->

![Korrektur des Problems](../assets/fix.svg) Adobe Commerce zeigt keinen Fehler mehr an, wenn ein Admin-Benutzer versucht, einem Lager oder Produkt 200 oder mehr Inventarquellen zuzuweisen. <!-- ACP2E-1180-->

![Problem behoben](../assets/fix.svg) Adobe Commerce unterstützt jetzt die Erstellung eines Kreditmemo für eine Bestellung, aus der ein Produkt gelöscht wurde. Zuvor konnten Händler kein Kreditmemo erstellen, wenn Produkte nach der Erstellung einer Rechnung aus der Bestellung gelöscht worden waren. Die Anwendung zeigte diesen Fehler an: `Following products with requested skus were not found: s00001`. t. <!-- ACP2E-1138-->

![Problem behoben](../assets/fix.svg) Stores werden jetzt sowohl anhand einzelner als auch mehrerer Store-IDs gefiltert. Der Produktattributcode `event` wurde zur Liste der reservierten Attributcodes hinzugefügt. Zuvor gab der Bericht &quot;Geringer Lagerbestand&quot;eine Ausnahme aus, wenn das Lagerbestandsmodul installiert wurde. <!-- ACP2E-1017-->

![Korrektur des Fehlers](../assets/fix.svg) Navigationsfilter mit Ebenen funktionieren jetzt erwartungsgemäß, und nicht vorrätige Produkte werden jetzt an die Produktliste der Storefront-Kategorie angehängt. Das neue Sortierungsattribut &quot;`is_out_of_stock`&quot; verwendet das dynamische Feldzuordnungsmodul für das Elasticsearch für die Storefront-Produktsammlung. <!-- ACP2E-748-->

![Korrektur des Problems](../assets/fix.svg) Der Status des zusammengesetzten Produkts (Bundle, gruppiert und konfigurierbar) wird wie erwartet aktualisiert, wenn der Status des untergeordneten Produktbestands durch einen REST `POST /rest/V1/inventory/source-items` -Aufruf geändert wird. <!-- ACP2E-1209-->

## v1.2.5

[!DNL Inventory Management] 1.2.5 (Modulversion: `magento/inventory-metapackage = 1.2.5`) wird in Version 2.4.5 unterstützt und ist mit Version 2.4.0 von Adobe Commerce, Adobe Commerce in der Cloud-Infrastruktur und der Magento Open Source-Codebasis kompatibel.

![Problem behoben](../assets/fix.svg) Der standardmäßige Lagerbestandsstatus von Bundles und gruppierten Produkten wird jetzt erwartungsgemäß aktualisiert, wenn ein Händler eine Sendung vom Administrator erstellt. Zuvor blieb der Status dieser Produkte nach der Entstehung einer Sendung unverändert. <!--- ACP2E-418-->

![Korrektur des Problems](../assets/fix.svg) Konfigurierbare Produkte werden jetzt wieder auf Lager gebracht, wenn eine der folgenden Bedingungen erfüllt ist: 1. Das übergeordnete Produkt hat mindestens ein gespeichertes Kind auf Lager. 2. Das konfigurierbare Produkt selbst wurde aktualisiert und als **auf Lager** festgelegt und hatte mindestens ein untergeordnetes Element auf Lager. <!--- ACP2E-443-->

![Problem behoben](../assets/fix.svg) Durch die REST-API implementierte Lagerbestandsänderungen werden nun wie erwartet auf Produktdetailseiten angezeigt. Der Cache für Katalogprodukte wird jetzt bereinigt, nachdem der letzte und der aktuelle Lagerstatus verglichen wurden. Zuvor führte das Auslassen der Rückruffunktion zu einer fehlerhaften Bewertung von Bestandsstatusänderungen, wodurch die erforderliche Cache-Bereinigung nicht Trigger wurde. Infolgedessen spiegelt die Storefront die Bestandsänderungen nicht wider. <!--- ACP2E-161-->

![Korrektur des Fehlers](../assets/fix.svg) Produkte, die dem Standardbestand zugewiesen sind und zuvor nicht vorrätig waren, sind jetzt auf der Storefront sichtbar, nachdem das Quellelement mit `/V1/inventory/source-items` aktualisiert wurde. Zuvor hat dieser REST-API-Endpunkt den falschen `stock_status` festgelegt. <!--- ACP2E-562-->

![Korrektur des Fehlers](../assets/fix.svg) Das Aufheben der Zuweisung von Inventarquellen über Massenaktionen (**[!UICONTROL Catalog]** > **[!UICONTROL Products]** > **[!UICONTROL Select Products]** > **[!UICONTROL Actions - Unassign Inventory Source]**) funktioniert jetzt erwartungsgemäß, wenn Quellen SKUs enthalten, die Duplikate sind, mit Ausnahme einer vorangestellten Null (z. B. `01234` und `1234`). Zuvor hat die Anwendung die Zuweisung von Inventarquellen nicht aufgehoben und einen Fehler ausgegeben. <!--- ACP2E-2641-->

![Korrektur des Problems](../assets/fix.svg) Der Status des Produktbestands ist jetzt immer **auf Lager** auf der Storefront, wenn endlose Rückkaufaufträge aktiviert sind und das Produkt einem benutzerdefinierten Lager zugewiesen wird, unabhängig von der zurückbestellten Menge. Zuvor waren die Produkte nicht mehr vorrätig, selbst wenn rückwirkende Bestellungen aktiviert waren. <!--- ACP2E-664-->

![Korrektur des Fehlers](../assets/fix.svg) Konfigurierbares übergeordnetes und untergeordnetes Produkt-Lager wird jetzt korrekt aktualisiert, nachdem das Quellelement mit `POST /V1/inventory/source-items` aktualisiert wurde. Nachdem das untergeordnete Produkt über die API aktualisiert wurde, wird ein neues Inventar-Plug-in für standardmäßige Bestandskontrollen erstellt und die konfigurierbare Produktmenge und -status aktualisiert. <!--- ACP2E-442-->

![Korrektur des Fehlers](../assets/fix.svg) Nicht vorrätige gruppierte Produkte werden nicht mehr auf der Seite &quot;Storefront-Kategorie&quot;aufgelistet. <!--- ACP2E-2082-->

![Korrektur des Problems](../assets/fix.svg) Korrektur des Paketnamens in `CatalogInventory` `composer.json` <!--- ACP2E-2914-->.

![Korrektur des Fehlers](../assets/fix.svg) Der Status der Bestellung wird jetzt im Admin korrekt angezeigt, nachdem eine Bestellung mit einem Nullmengenprodukt in einer Bereitstellung mit mehreren Quellen/Lagern aufgegeben wurde. [GitHub-33756](https://github.com/magento/magento2/issues/33756) <!--- ACP2E-713-->

![Problem behoben](../assets/fix.svg) Nicht vorrätige Bundle-Produkte werden nicht mehr auf der Seite &quot;Storefront-Kategorie&quot;angezeigt, wenn das Bundle-Produkt über den Abschnitt &quot;Lager&quot;aktualisiert wird. <!--- ACP2E-2012-->

![Korrektur eines Problems](../assets/fix.svg) Kompatibilitätsprobleme mit PHP 7.4 wurden behoben. <!--- AC-3192-->

![Problem behoben](../assets/fix.svg) Die Leistung von Speichervorgängen, die Bundle-Produkte mit vielen Optionen enthalten (mehrere 100), wurde verbessert. Bisher dauerte das Speichern dieser großen Bundle-Produkte einige Minuten und führte manchmal zu Zeitüberschreitungen bei Implementierungen mit aktivierten Lagerbestandsdiensten. [GitHub-34732](https://github.com/magento/magento2/issues/34732) <!--- AC-1901-->

![Korrektur des Problems](../assets/fix.svg) Das Massen-Aktionstool für Produkte (**[!UICONTROL Select Products]** > **[!UICONTROL Actions]** > **[!UICONTROL Assign Inventory Source]**) funktioniert jetzt erwartungsgemäß, wenn Lagerbestandsquellen mehreren Produkten zugewiesen werden, wenn SKUs dupliziert werden, mit Ausnahme des führenden `0` (z. B. `01234` und `1234`). Zuvor wurde nur einem Produkt eine Lagerbestandsquelle zugewiesen. [GitHub-35171](https://github.com/magento/magento2/issues/35171) <!--- AC-2584-->

![Korrektur des Problems](../assets/fix.svg) Das Feld `ProductInterface.only_x_left_in_stock` gibt jetzt 0 zurück, wenn der Bestand 0 ist. Zuvor wurde null zurückgegeben. [GitHub-29932](https://github.com/magento/magento2/issues/29932) <!--- AC-1806-->

![Problem behoben](../assets/fix.svg) Sie können jetzt Standardlager über Admin **[!UICONTROL Stores]** > **[!UICONTROL Inventory]** > **[!UICONTROL Stocks]** bearbeiten. Zuvor wurde in der Konsole ein JavaScript-Fehler angezeigt, als Sie versuchten, Quellen aus dem Standardbestand hinzuzufügen oder daraus zu entfernen. Sie konnten jedoch Websites einem Standardbestand zuweisen. <!--- ACP2E-545-->

![Korrektur des Problems](../assets/fix.svg) <!--- ACP2E-274--> Die Produktanzahl der Kategorienliste ist jetzt korrekt, wenn der Inventar-Einzelquellenmodus mit aktivierter Einstellung **[!UICONTROL Display Out-Of-Stock Products]** verwendet wird. Ein neues Plug-in verwendet nun `AreProductsSalableInterface` und `StockConfigurationInterface`, um die Gesamtanzahl der Produkte zu ermitteln. Zuvor gab die Produktliste der Kategorie die falsche Produktmenge zurück.

![Korrektur des Fehlers](../assets/fix.svg) <!--- ACP2E-322--> Konfigurierbare Produkte werden jetzt an die letzte Position in der Produktliste verschoben, nachdem der Lagerbestand aktualisiert wurde, wenn die Einstellung **[!UICONTROL Move out of stock to the bottom]** aktiviert ist. Eine neue benutzerdefinierte Datenbankabfrage wird implementiert, um die Sortierreihenfolge von Elasticsearch-Indizes zu umkehren, wodurch die Admin-aktivierte Sortierreihenfolge ignoriert wird. Zuvor wurden konfigurierbare Produkte und ihre untergeordneten Produkte nicht an den unteren Rand der Liste verschoben, wenn diese Einstellung aktiviert war.

## v1.2.4

Inventory management 1.2.4 (Modulversion: `magento/inventory-metapackage = 1.2.4`) wird in Version 2.4.4 unterstützt und ist mit Version 2.4.0 von Adobe Commerce, Adobe Commerce in der Cloud-Infrastruktur und der Magento Open Source-Codebasis kompatibel.

![Problem behoben](../assets/fix.svg) Commerce zeigt jetzt einen genauen Wert für die Verkaufsmenge für alle Produkte in der Admin-Produktlistenansicht an. Zuvor wurde ein leerer Wert für die verkaufbare Menge von Produkten auf Lager mit SKUs angezeigt, die Sonderzeichen enthielten. <!--- MC-41936-->

![Korrektur des Fehlers](../assets/fix.svg) Die Leistung wurde für Warenkorb- und Checkout-Aktionen verbessert, z. B. beim Hinzufügen von Produkten zum Warenkorb in Bereitstellungen mit vielen (ca. 10.000) Inventarquellen. <!--- MC-42570-->

![Korrektur des Fehlers](../assets/fix.svg) Der Befehl `bin/magento inventory:reservation:list-inconsistencies` verarbeitet jetzt Bestellungen mit Teillieferungen korrekt, selbst wenn die Reservierungen aus der Datenbank fehlen und der Cache gelöscht wurde. Zuvor wurde bei der Ausführung dieses Befehls mit einem vorab geleerten Cache der folgende Fehler in Commerce angezeigt: `Area code is not set`. <!--- MC-42142-->

![Korrektur des Problems](../assets/fix.svg) Inkrementelle Indizierung von gruppierten Produkt-untergeordneten Produkten führt nicht mehr dazu, dass andere gruppierte Produkte beim Freigeben von untergeordneten Elementen falsch indiziert werden. <!--- MC-41963-->

![Problem behoben](../assets/fix.svg) Auf der Kategorieseite in der Storefront wird jetzt die richtige Produktanzahl angezeigt, nachdem ein Produkt aus einer Kategorie nach API entfernt wurde. Zuvor war die Produktanzahl der Kategorieseiten bis zur Neuindizierung falsch. <!--- MC-42287-->

![Korrektur des Fehlers](../assets/fix.svg) Konfigurierbare Produkte können jetzt beim Erstellen eines Credit Memos wieder vorrätig gestellt werden, wenn die Option **[!UICONTROL Manage Stock]** deaktiviert ist. Zuvor wurde in Commerce auf der Seite zur Erstellung des Kreditspeichers das Kontrollkästchen **Zurück zu Lager** nicht angezeigt, wenn diese Option deaktiviert war. <!--- MC-42002-->

![Korrektur des Problems](../assets/fix.svg) Die Verwaltung des Lagerbestands, der mehr als 10.000 Elemente umfasst, wurde verbessert. Bisher konnten Kaufleute aufgrund von Leistungsproblemen manchmal keine Lagerbestände in der Admin-Konsole bearbeiten, bevor sie ihre Website aufriefen. <!--- MC-42643-->

![Korrektur des Problems](../assets/fix.svg) Die Seite **[!UICONTROL User Roles]** im Admin wird aktualisiert, um Administratoren eingeschränkten Zugriff auf die Konfiguration der Versandmethoden zu gewähren. Der Abschnitt _Versandmethoden_ wurde in _[!UICONTROL Delivery methods]_umbenannt und_[!UICONTROL In-Store Pickup]_ wird unter den Abschnitt _[!UICONTROL Delivery methods]_verschoben. [GitHub-30053](https://github.com/magento/magento2/issues/30053) <!--- MC-41545-->

![Problem behoben](../assets/fix.svg) Adobe Commerce erstellt keine doppelte Produktreservierung mehr, nachdem ein Kreditmemo durch die API aktualisiert wurde. <!--- MC-41757-->

![Korrektur des Fehlers](../assets/fix.svg) Beim Wechseln von der Registerkarte _[!UICONTROL Pick up in Store]_zur Registerkarte_[!UICONTROL Shipping]_ im Checkout-Workflow wird kein JavaScript-Fehler mehr Trigger, wenn nur die In-Store-Abruf-Bereitstellung verfügbar ist. <!--- MC-42808-->

![Problem behoben](../assets/fix.svg) Die veräußerbare Produktmenge und die Lagerproduktmenge werden jetzt korrekt synchronisiert. Zuvor wurde die Bestandserhaltungskompensation für stornierte Bestellungen nicht neu erstellt. <!--- MC-42485-->

![Problem behoben](../assets/fix.svg) Die Leistung des Validators wurde optimiert, um zu verhindern, dass dem untergeordneten Produkt eines gebündelten Produkts mit dem Versandtyp `Ship Together` <!--- MC-43039--> eine neue Quelle hinzugefügt wird.

## 1.2.3

[!DNL Inventory Management] 1.2.3 (Modulversion: `magento/inventory-metapackage = 1.2.3`) wird in Version 2.4.3 unterstützt und ist mit Version 2.4.0 von Adobe Commerce, Adobe Commerce in der Cloud-Infrastruktur und der Magento Open Source-Codebasis kompatibel.

![Korrektur des Fehlers](../assets/fix.svg) Fehlerkorrektur - diverse Probleme im Zusammenhang mit der Sichtbarkeit des zusammengesetzten Produkts auf der Vorderseite wurden behoben.

![Korrektur des Fehlers](../assets/fix.svg) Verbesserte Leistung bei der Verwaltung von Warenkorbseiten mit der erforderlichen Mindestmenge.

![Korrektur des Fehlers](../assets/fix.svg) Verschiedene Fehlerbehebungen zur Behebung von Problemen mit der Quellerstellung, nicht vorrätigen Elementen, der Lagerbestandsbeschaffung, der Sortierung zugewiesener Quellen, der In-Store-Bereitstellung und den Lagerbestandsbefehlen.

![Korrektur des Fehlers](../assets/fix.svg) [!DNL Commerce] unterstützt jetzt dreistellige kanadische Postleitzahlen für den In-Store-Versand. Sechstellige Codes werden aufgrund von Beschränkungen, die durch `geonames.org` festgelegt wurden, nicht unterstützt.

![Problem behoben](../assets/fix.svg) Der Administrator zeigt jetzt die richtige Menge des Standardbestands für deaktivierte Produkte im Raster **Produkte** und auf der Seite **Produkt bearbeiten** für Bereitstellungen mit mehreren Stores an.

![Problem behoben](../assets/fix.svg) [!DNL Commerce] aktualisiert jetzt den Kategorieprodukt-Cache, wenn ein Bundle-Produkt wieder auf Lager ist.

## 1.2.2

[!DNL Inventory Management] 1.2.2 (Modulversion: `magento/inventory-metapackage = 1.2.2`) wird in Version 2.4.2 unterstützt und ist mit Version 2.4.0 von Adobe Commerce, Adobe Commerce in der Cloud-Infrastruktur und der Magento Open Source-Codebasis kompatibel.

![Korrektur des Fehlers](../assets/fix.svg) Fehlerkorrektur - diverse Probleme im Zusammenhang mit der Sichtbarkeit des zusammengesetzten Produkts auf der Vorderseite wurden behoben.

![Korrektur eines Problems](../assets/fix.svg) Verbesserte Leistung der Warenkorbseite während der Mengenaktualisierung auf B2B.

![Korrektur des Problems](../assets/fix.svg) Mehrere Fehlerbehebungen, die zur Behebung von Problemen bei der In-Store-Erfassung, Massenaktualisierungen und der Inventarschwelle verwendet wurden.

![Neu](../assets/new.svg) **Funktionstests.** Es wurden neue Funktionstests eingeführt und Fehlerbehebungen für bestehende Tests bereitgestellt, um sie stabiler zu machen.

## 1.2.1

[!DNL Inventory Management] 1.2.1 (Modulversion: `magento/inventory-metapackage = 1.2.1`) wird in Version 2.4.1 unterstützt und ist mit Version 2.4.0 von Adobe Commerce, Adobe Commerce in der Cloud-Infrastruktur und der Magento Open Source-Codebasis kompatibel.

![Korrektur des Fehlers](../assets/fix.svg), der ein bekanntes Problem im Zusammenhang mit dem `inventory_cleanup_reservations`-Cron-Auftrag behoben und ein Problem im Zusammenhang mit der In-Store-Abruf-Funktion für Bundle-Produkte behoben hat. Dieses Update umfasst auch allgemeine Verbesserungen bei der Berechnung von Lagerbeständen, der Unterstützung von Bundle-Produkten und der Backorder-Funktionalität.

![Neu](../assets/new.svg) **Funktionstests.** Es wurden neue Funktionstests eingeführt, um eine zusätzliche Abdeckung für die In-Store-Abruf-Funktion bereitzustellen.

## 1,2,0

[!DNL Inventory Management] 1.2.0 (Modulversion: `magento/inventory-metapackage = 1.2.0`) wird in Version 2.4.0 von Adobe Commerce, Adobe Commerce in der Cloud-Infrastruktur und der Magento Open Source-Codebasis unterstützt.

![Korrektur des Fehlers](../assets/fix.svg) Zahlreiche Fehlerbehebungen zur Lösung von Problemen mit der Quellzuweisung, der Unterstützung skalierbarer Umgebungsfunktionen und der Kompatibilität mit PHP 7.4, MySQL 8 und PHPUNIT 9.

![Neu](../assets/new.svg) **In-store-Bereitstellungsmethode.** Es wurde eine Option hinzugefügt, mit der Benutzer eine Quelle auswählen können, die beim Checkout als Abholort verwendet werden soll. Siehe [In-store-Bereitstellung](../stores-purchase/shipping-in-store-delivery.md) im _Verkaufs- und Kauferlebnis-Handbuch_.

![Neu](../assets/new.svg) **Bundle-Produktunterstützung für den Multi-Source-Modus.** Der Bestand unterstützt alle Produktarten mit mehreren Quellen.

![Neu](../assets/new.svg) **Asynchrone Neuindizierung des Lagers.** Die Fähigkeit zur asynchronen Neuindizierung von Beständen wurde hinzugefügt und die Leistung verschiedener kritischer Szenarien verbessert.

![Neu](../assets/new.svg) **Massenschnittstellen.** Neue Bulk-Schnittstellen für die Veräußerbarkeitsprüfung eingeführt: `\Magento\InventorySalesApi\Api\AreProductsSalableInterface`, `\Magento\InventorySalesApi\Api\AreProductsSalableForRequestedQtyInterface`.

![Neu](../assets/new.svg) **Verbesserte Testabdeckung.** Die neue Funktionalität wird von automatisierten Tests abgedeckt, einschließlich erweiterter Abdeckung für erkannte und behobene Probleme.

![Bekanntes Problem](../assets/bug.svg) **Bekanntes Problem.** Das Fehlen des Felds `object_id` in den Reservierungsmetadaten verhindert, dass der Cron-Auftrag `inventory_cleanup_reservations` ordnungsgemäß funktioniert. Dieses Problem wurde in [magento/inventory#3046](https://github.com/magento/inventory/pull/3046) eingeführt.

**Problemumgehung:** Führen Sie die folgenden MySQL-Abfragen aus, um Reservierungen manuell zu bereinigen:

```sql
SELECT GROUP_CONCAT(reservation_id) FROM inventory_reservation GROUP BY stock_id, sku HAVING SUM(quantity) = 0;
DELETE FROM inventory_reservation where reservation_id IN (result_of_the_first_query);
```

## 1.1.6

[!DNL Inventory Management] 1.1.6 (Modulversion: `inventory-composer-metapackage = 1.1.6`) wird mit Version 2.3.6 unterstützt und ist mit den Versionen 2.3.5, 2.3.4, 2.3.3, 2.3.2, 2.3.1 und 2.3.0 von Adobe Commerce, Adobe Commerce über Cloud-Infrastruktur und der Magento Open Source-Codebasis kompatibel.

![Korrektur des Fehlers](../assets/fix.svg) Behebung von Problemen im Zusammenhang mit Rückständen, Kreditmemos, geringem Bestands-Berichtsraster, Fehlerbehebungen im Zusammenhang mit dem CLI-Tool &quot;Inkonsistenzen aufheben&quot;und allgemeinen Verbesserungen.

![Neu](../assets/new.svg) **Asynchrone Neuindizierung des Lagers.** Die Fähigkeit zur asynchronen Neuindizierung von Beständen wurde hinzugefügt und die Leistung verschiedener kritischer Szenarien verbessert.

## 1,1,5

[!DNL Inventory Management] 1.1.5 (Modulversion: `inventory-composer-metapackage = 1.1.5`) wird in Version 2.3.5 unterstützt und ist mit den Versionen 2.3.4, 2.3.3, 2.3.2, 2.3.1 und 2.3.0 von Adobe Commerce, Adobe Commerce in der Cloud-Infrastruktur und der Magento Open Source-Codebasis kompatibel.

![Neu](../assets/new.svg) **Aktualisieren Sie den Bestand, sobald die Produkt-SKU geändert wurde.** Es wurde eine neue Konfigurationseinstellung eingeführt, um zum neuen Verhalten zu wechseln: &quot;Mit Katalog synchronisieren&quot;.

![Neu](../assets/new.svg) **Funktionstests.** Neue Funktionstests wurden eingeführt, um die Lücke in der Testabdeckung zu schließen. Fehlerkorrektur - Tests sind jetzt stabiler und zuverlässiger.

![Bekanntes Problem](../assets/bug.svg) Fehlerbehebungen, um zu verhindern, dass Produkt-Überverkäufe, die Sichtbarkeit von &quot;nicht vorrätigen&quot;Produkten auf der Storefront, zahlreiche Fehlerbehebungen für skalierbare Umgebungsunterstützung und Verbesserungen der Benutzeroberfläche verhindert werden.

## 1.1.4

[!DNL Inventory Management] 1.1.4 (Modulversion: `inventory-composer-metapackage = 1.1.4`) wird in Version 2.3.4 unterstützt und ist mit den Versionen 2.3.3, 2.3.2, 2.3.1 und 2.3.0 von Adobe Commerce, Adobe Commerce in der Cloud-Infrastruktur und der Magento Open Source-Codebasis kompatibel.

![Problem behoben ](../assets/fix.svg)**Verbesserte Leistung.** Die Bundching-Logik für den CLI-Befehl &quot;Inventarreservierungen&quot;wurde eingeführt, um die Speicherbelegung zu reduzieren und Fälle zu vermeiden, in denen der Prozess ohne Antwort blockiert wird.

![Neu ](../assets/new.svg)**Verbesserte Testabdeckung.** Es wurden viele neue Funktionstests eingeführt. Fast alle manuellen Inventarszenarien werden mit automatisierten Tests abgedeckt.

![Bekanntes Problem](../assets/bug.svg) Zahlreiche Fehlerbehebungen zur Behebung von Problemen mit Kreditkarten, gruppierten Produkten sowie Massenaktionen bei Quelle und Lager.

## 1.1.3

[!DNL Inventory Management] 1.1.3 (Modulversion: `inventory-composer-metapackage = 1.1.3`) wird in Version 2.3.3 unterstützt und ist mit den Versionen 2.3.2, 2.3.1 und 2.3.0 von Adobe Commerce, Adobe Commerce in der Cloud-Infrastruktur und der Magento Open Source-Codebasis kompatibel.

![Korrektur eines Problems ](../assets/fix.svg)**Bessere Integration in Adobe Commerce- und B2B-Funktionen.** [!DNL Inventory Management] funktioniert jetzt ordnungsgemäß mit den folgenden Funktionen für Websites, die nicht standardmäßige Inventarquellen und -bestände verwenden:

- Bestellung nach SKU (Adobe Commerce)
- Schnellbestellung (B2B)
- Anforderungslisten (B2B)

![Neu ](../assets/new.svg)**Verbesserte Leistung.** Die Browserleistung des Storefront-Katalogs wurde für Websites verbessert, die den standardmäßigen Lagerbestand und die Standardquelle ausführen.

![Neu ](../assets/new.svg)**Verbesserte Testabdeckung.** Die automatisierte Funktions- und Integrationstest-Abdeckung wurde deutlich erhöht.

## 1.1.2

[!DNL Inventory Management] 1.1.2 (Modulversion: `inventory-composer-metapackage = 1.1.2`) wird in Version 2.3.2 unterstützt und ist mit den Versionen 2.3.1 und 2.3.0 von Adobe Commerce, Adobe Commerce in der Cloud-Infrastruktur und der Magento Open Source-Codebasis kompatibel.

![Korrektur des Problems](../assets/fix.svg) `source_code` zur Antwort für den REST-Endpunkt GET `/V1/shipments`. <!-- https://github.com/magento/inventory/pull/2142 -->

![Korrektur des Fehlers](../assets/fix.svg) Korrektur des Fehlers, der dazu führte, dass Reservierungen korrekt gelöscht und Produktmengen aktualisiert wurden, nachdem ein Kreditvermerk für eine nicht versandte Bestellung ausgestellt wurde. Wenn Sie die Option auf <!-- https://github.com/magento/inventory/pull/2179 --> auswählen

![Korrektur des Fehlers](../assets/fix.svg) Korrektur des Fehlers, der beim Eingeben von Mengen während der Produkterstellung die Menge für konfigurierbare Produkt-untergeordnete Elemente korrekt speicherte. <!-- https://github.com/magento/inventory/pull/2158 -->

Zu den neuen Modulen für [!DNL Inventory Management] 1.1.2 Beta gehören:

```php
        'Magento_InventoryGraphQl' => 1,
        'Magento_InventoryReservations' => 1,
        'Magento_InventoryReservationsApi' => 1,
        'Magento_InventoryReservationCli' => 1,
        'Magento_InventoryExportStock' => 0,
        'Magento_InventoryExportStockApi' => 0,
```

![Neu](../assets/new.svg) **Der Endpunkt &quot;Gebündelter Teil-Lagerbestand-Transfer&quot;** wurde hinzugefügt - Aktuelle Endpunkte für die Massenübertragung verschieben alle zugewiesenen Mengen von einer Quelle in eine Zielquelle. Der neue `/rest/V1/inventory/bulk-partial-source-transfer` -Endpunkt ermöglicht Händlern die Übertragung eines partiellen Bestands von der Quelle an die Quelle als Massenvorgang. Um eine bestimmte Menge zu übertragen, geben Sie eine Anforderung mit den Werten `sku`, `qty`, `origin_source_code` und `destination_source_code` an den Endpunkt ein. Übertragungen überprüfen, ob die Quelle den `sku` zugewiesen ist, ob genügend Menge für eine Übertragung vorhanden ist usw. Siehe [Massenaktionen des Bestands](https://developer.adobe.com/commerce/webapi/rest/inventory/bulk-inventory/){target="_blank"} in der REST-API-Dokumentation. <!-- https://github.com/magento/inventory/pull/2117 -->

![Neu](../assets/new.svg) **Reservierungs-CLI hinzugefügt** - Neue Befehle bieten Optionen zum Erkennen und Auflösen von Reservierungsinkonsistenzen. Wenn Bestellungen einreichen und den Status ändern, generiert [!DNL Inventory Management] anfängliche Reservierungen und Aktualisierungen durch Ausgleichsreservierungen. Diese Befehle geben eine Liste der erkannten Inkonsistenzen nach Bestell-ID, SKU und Lager-ID zurück und erstellen Vorbehalte, die aufgelöst werden können. Weitere Informationen finden Sie in der [CLI-Referenz](cli.md) . <!-- https://github.com/magento/inventory/pull/2199 https://github.com/magento/inventory/pull/2184 https://github.com/magento/inventory/pull/2171 https://github.com/magento/inventory/pull/2148  -->

![Neu](../assets/new.svg) **Leistungsverbesserungen für Quellen und SSA-Optionen** - Die Sortierung und Auswahl von Quellen während des Versands führte zu einer Leistungsverschlechterung bei Beständen mit einer hohen Anzahl von Quellen. Diese Version bietet wesentliche Leistungsverbesserungen bei der Auflistung und Sortierung der verfügbaren Quellen bei der Überprüfung und Auswahl von SSA-Optionen in Sendungen. <!-- https://github.com/magento/inventory/pull/2056 https://github.com/magento/inventory/pull/2090 -->

![Neu](../assets/new.svg) **GraphQL-Unterstützung für Inventory management** hinzugefügt - Mit dieser Version wird ein neues `magento/module-inventory-graph-ql` -Modul installiert. Die GraphQL-Attribute [ProductInterface ](https://developer.adobe.com/commerce/webapi/graphql/schema/products/interfaces/attributes/){target="_blank"} enthalten jetzt die Attribute `only_x_left_in_stock` und `stock_status` für die Unterstützung von [!DNL Inventory Management]. <!-- https://github.com/magento/inventory/pull/2124 -->

![Neu](../assets/new.svg) **Vereinfachte Benutzeroberfläche für zugewiesene Quellen** - Die Tabelle Zugewiesene Quellen auf Produktseiten enthält vereinfachte Inhalte für einfachere Aktualisierungen und verbesserte Leistung bei der Anzeige vieler Quellen. Alle Quellen werden nach Quellname aufgelistet (bei `source_code` bewegen Sie den Mauszeiger darüber).

![Neu](../assets/new.svg) **Aggregierten Lagerdienst exportieren** - Diese Version bietet einen neuen, exportaggregierten Lagerdienst (der Reservierungen im System beibehält), der externe Sales Channel wie Amazon, eBay und Google Shopping-Anzeigen unterstützt.  <!-- https://github.com/magento/inventory/pull/2067 -->

## 1.1.0

[!DNL Inventory Management] 1.1.0 (Modulversion: `inventory-composer-metapackage = 1.1.0`) wird unterstützt und ist mit Version 2.3.0 von Adobe Commerce, Adobe Commerce in der Cloud-Infrastruktur und der Magento Open Source-Codebasis kompatibel. [!DNL Inventory Management] 1.1.1 wird nur als Aktualisierung des Paketnamens veröffentlicht, unterstützt für Version 2.3.1 und kompatibel mit Version 2.3.0 von Adobe Commerce, Adobe Commerce für die Cloud-Infrastruktur und der Magento Open Source-Codebasis.

![Problem behoben](../assets/fix.svg) **Unterstützung für Elasticsearch für Einzel- und Mehrfachquellenmodi** - Jetzt können Sie Elasticsearch mit benutzerdefinierten Lagern konfigurieren und verwenden. Informationen zur Installation finden Sie unter [Einrichten des Elasticsearch-Dienstes](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure/service/elasticsearch.html){target="_blank"} . <!-- PR https://github.com/magento/inventory/pull/1943 -->

![Korrektur des Problems](../assets/fix.svg) Behebung von Leistungsproblemen mit Standardspeicher, um die Leistung bei zahlreichen Vorgängen drastisch zu steigern. Durch Verbesserungen wird die Leistung für Einzelquellenmodi, die Übertragung des Bestands an Source, Storefront-Kategorieseiten und die Berechnung der Verkaufsmenge verbessert.

<!-- All Performance Track issues resolved https://github.com/magento/inventory/issues?q=is%3Aopen+is%3Aissue+label%3APerformance -->

![Korrektur des Fehlers](../assets/fix.svg) Behebung von Problemen mit dem Status &quot;Nicht auf Lager&quot;und der Massenbestandsübertragung auf Lager für konfigurierbare und gruppierte Produkte. Die Auswahl der übergeordneten Produkte und die Durchführung von Massenaktionen wirken sich nicht auf den Produktstatus aus. Wenn das übergeordnete Produkt auf Lager war, bleibt es auf Lager.

<!-- PR https://github.com/magento/inventory/pull/1972 -->

![Neu](../assets/new.svg) **Distance Priority Algorithm** - Der Distance Priority Algorithm ist ein neuer, vordefinierter Source Selection Algorithm für entfernungsbasierte Versandempfehlungen. Dieser Algorithmus vergleicht den Speicherort der Lieferzieladresse mit den Quellspeicherorten, um die nächstgelegene Quelle zu bestimmen, aus der Sendungen durchgeführt werden können. Der Abstand kann entweder durch die physische Entfernung oder die auf Reisen von einem Ort zum anderen verbrachte Zeit bestimmt werden, indem importierte Geocode-Standortdaten oder Google-Anweisungen (Fahren, Gehen oder Fahrradfahren) verwendet werden.

![Neu](../assets/new.svg) **Erweiterte Liste der Quellmengen** - Händler mit einer hohen Anzahl von Quellen können einfach über das Produktraster alle Quellen pro Produkt bewegen und anzeigen. Jedes Produkt zeigt mindestens fünf Quellen und entsprechende Mengen an. Wenn Sie den Mauszeiger über die Quellen bewegen, können Sie durch die gesamte Liste der Quellen und aktuellen Mengen blättern.

![Bekanntes Problem](../assets/bug.svg) Bekanntes Problem mit Magento Open Source und Adobe Commerce v2.3.1 - Beim asynchronen Migrieren von Daten zwischen Quellen treten aufgrund von Änderungen in asynchronen APIs Probleme auf, bei denen Themennamen die PHP-Klasse und Methodennamen widerspiegeln. Es wird empfohlen, für synchrone Vorgänge **[!UICONTROL Run asynchronously]** den Wert `No` festzulegen.
