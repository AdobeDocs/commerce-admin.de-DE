---
title: '[!DNL Inventory Management] Versionshinweise'
description: Informationen zu allen Versionen finden  [!DNL Inventory Management]  in den Versionshinweisen .
exl-id: 856b9503-7621-4beb-ac2f-3eb1a240cebc
feature: Inventory, Release Notes
source-git-commit: 01d8a1d50f574330f3ce7e8bf03a018f0079f5db
workflow-type: tm+mt
source-wordcount: '3445'
ht-degree: 0%

---

# [!DNL Inventory Management] Versionshinweise

Diese Versionshinweise beschreiben Versionen von [!DNL Inventory Management] und umfassen Folgendes:

![Neu](../assets/new.svg) Neue Funktionen
![Problem behoben](../assets/fix.svg) Fehlerbehebungen und Verbesserungen
![Bekanntes Problem](../assets/bug.svg) Bekannte Probleme

[!DNL Inventory Management] ist ein Magento Open Source-Community-Engineering-Sonderprojekt, das Mitwirkenden offen steht. Um teilzunehmen und einen Beitrag zu leisten, lesen Sie das [GitHub-Projekt](https://github.com/magento/inventory)-Repository und [Wiki](https://github.com/magento/inventory/wiki), um loszulegen. Um das Projekt zu besprechen, treten Sie dem [Slack](https://magentocommeng.slack.com/?redir=%2Farchives%2FC5FU5E2HY)-Kanal ([Self-Signup](https://opensource.magento.com/slack)) bei.

[Versionsplan](https://experienceleague.adobe.com/docs/commerce-operations/release/planning/schedule.html){target="_blank"} für unterstützte und kompatible Versionen.

## v1.2.7

[!DNL Inventory Management] Versionshinweise zu 1.2.7 sind in den Versionshinweisen zu [Core 2.4.7“ ](https://experienceleague.adobe.com/en/docs/commerce-operations/release/notes/adobe-commerce/2-4-7#inventory-management-1).

## v1.2.6

[!DNL Inventory Management] 1.2.6 (Modulversion: `magento/inventory-metapackage = 1.2.6`) wird mit Version 2.4.6 unterstützt und ist mit Version 2.4.0 von Adobe Commerce, Adobe Commerce on Cloud Infrastructure und der Magento Open Source Code Base kompatibel.

![Problem behoben](../assets/fix.svg) Die Storefront zeigt jetzt zusammengesetzte Produkte (konfigurierbar, gebündelt und gruppiert) als vorrätig an, wenn untergeordnete Produkte, die ausverkauft waren, wieder auf Lager sind. Zuvor gab die Storefront an, dass das zusammengesetzte Produkt unter diesen Bedingungen nicht vorrätig war. <!-- ACP2E-1106-->

![Problem behoben](../assets/fix.svg) Konfigurierbare Produktoptionen werden jetzt wie erwartet in der Storefront als nicht vorrätig angezeigt, wenn die Option mit einer Menge von 0 erstellt wurde und **[!UICONTROL Display out-of-stock products]** aktiviert ist. <!-- ACP2E-1148-->

![Problem behoben](../assets/fix.svg) Kategorieseiten-Caches werden nicht mehr invalidiert, wenn sich die Lagermenge ändert und das Produkt noch auf Lager ist. Adobe Commerce lädt jetzt Seiten aus dem Cache, anstatt sie neu zu generieren, wenn sich die Produktmenge (und sonst nichts) auf der Kategorieseite der Storefront ändert. <!-- ACP2E-118-->

![Problem behoben](../assets/fix.svg) Die Produktanzahl der Kategorieliste ist jetzt korrekt, wenn Inventar im Einzelquellenmodus mit aktivierter **[!UICONTROL Display Out-Of-Stock Products]** verwendet wird. Adobe Commerce prüft jetzt beim Zählen, ob ein Produkt skalierbar ist. <!-- ACP2E-1033-->

![Problem behoben](../assets/fix.svg) Die Regeln für den Warenkorbpreis für den In-Store-Versand funktionieren jetzt wie erwartet, wenn der Bestand aktiviert ist. Zuvor wurden die durch die Warenkorbpreisregel generierten Rabatte unter diesen Bedingungen nicht angewendet. <!-- ACP2E-1015-->

![Es wurde ein Problem behoben](../assets/fix.svg) Durch die Aktualisierung des Produktbestands im geplanten Modus werden nicht mehr alle Caches gelöscht. Zuvor hat der Inventar-Indexer alle Konfigurations-Caches gelöscht. <!-- ACP2E-1003-->

![Problem behoben](../assets/fix.svg) Der Wert für das Attribut **[!UICONTROL Allow Multiple Boxes for Shipping]** für ein Produkt im erweiterten Inventar wird jetzt erwartungsgemäß gespeichert. <!-- ACP2E-992-->

![Problem behoben](../assets/fix.svg) Adobe Commerce gibt jetzt eine genaue Reservierungskompensation aus, nachdem eine teilweise Rückerstattungsgutschrift für eine Bestellung erstellt wurde, die mit der Abholung im Geschäft aufgegeben wurde. Zuvor wurde eine falsche Reservierung in der `inventory_reservation` gespeichert, wenn ein Administrator bzw. eine Administratorin eine Gutschrift erstellt hat, ohne das Kontrollkästchen &quot;**[!UICONTROL Return to Stock]**&quot; zu aktivieren. <!-- ACP2E-979-->

![Problem behoben](../assets/fix.svg) Adobe Commerce zeigt konfigurierbare Produkte nicht mehr als nicht vorrätig in der Storefront an, wenn eine der Varianten in Bereitstellungen, die Inventar aus mehreren Quellen implementieren, manuell auf Lager zurückgegeben wurde. <!-- ACP2E-952-->

![Problem behoben](../assets/fix.svg) Die Spaltenposition im Produktraster (**[!UICONTROL Catalog]** > **[!UICONTROL Products]**) kehrt nicht mehr an die vorherige Position zurück, nachdem die Seite in Bereitstellungen mit mehreren konfigurierten Inventarquellen neu geladen wurde. <!-- ACP2E-925-->

![Problem behoben](../assets/fix.svg) Die Lagermenge ist jetzt korrekt, nachdem eine Gutschrift für ein virtuelles Produkt ausgestellt wurde, wenn das Kontrollkästchen &quot;**[!UICONTROL Back to stock]**&quot; nicht aktiviert ist. <!-- ACP2E-908-->

![Problem behoben](../assets/fix.svg) Sie können jetzt Kategorien mit automatischer Produktsortierung und dem Umfang speichern, der nicht dem Standardbestand zugewiesen ist. Zuvor hat Adobe Commerce die Kategorie nicht gespeichert und den folgenden Fehler angezeigt: `Something went wrong while saving the category`. <!-- ACP2E-859-->

![Problem behoben](../assets/fix.svg) Der Status Konfigurierbarer Produktbestand wird jetzt erwartungsgemäß aktualisiert, wenn das Produkt mit allen nicht vorrätigen konfigurierbaren Varianten erstellt wird. <!-- ACP2E-813-->

![Problem behoben](../assets/fix.svg) Das Tool zur Analyse der Reservierungsinkonsistenz funktioniert jetzt korrekt mit teilweise gelieferten Bestellungen, die konfigurierbare, gebündelte und gruppierte Produkte enthalten. Die zusammengesetzten Warentypen werden nun analysiert. Zuvor wurden Stornierungen und Rückerstattungen nur für übergeordnete Produkte gespeichert, nicht für Unterproduktbestellungen von konfigurierbaren und zusammen versandten Bundle-Produkten. <!-- ACP2E-924-->

![Problem behoben](../assets/fix.svg) Adobe Commerce zeigt keinen Fehler mehr an, wenn ein Admin-Benutzer versucht, einem Lager oder Produkt 200 oder mehr Inventarquellen zuzuweisen. <!-- ACP2E-1180-->

![Problem behoben](../assets/fix.svg) Adobe Commerce unterstützt jetzt die Erstellung einer Gutschrift für eine Bestellung, aus der ein Produkt gelöscht wurde. Zuvor konnten Händler keine Gutschrift erstellen, wenn Produkte aus der Bestellung gelöscht wurden, nachdem eine Rechnung erstellt worden war. Die Anwendung zeigte diesen Fehler an: `Following products with requested skus were not found: s00001`. T. <!-- ACP2E-1138-->

![Problem behoben](../assets/fix.svg) Stores werden jetzt sowohl nach einzelnen als auch nach mehreren Store-IDs gefiltert. Der `event` Produktattribut-Code wurde der Liste der reservierten Attributcodes hinzugefügt. Zuvor gab es im Bericht zu geringen Lagerbeständen eine Ausnahme, wenn das Inventar-Modul installiert wurde. <!-- ACP2E-1017-->

![Problem behoben](../assets/fix.svg) Filter für mehrschichtige Navigation funktionieren jetzt erwartungsgemäß, und nicht vorrätige Produkte werden jetzt der Produktliste der Storefront-Kategorie angehängt. Das neue Sortierattribut `is_out_of_stock` verwendet den dynamischen Feld-Mapper des Elasticsearchs für die Storefront-Produktsammlung. <!-- ACP2E-748-->

![Problem behoben](../assets/fix.svg) Der Lagerstatus von zusammengesetzten Produkten (Bundle, gruppiert und konfigurierbar) wird wie erwartet aktualisiert, wenn der Status des untergeordneten Produktbestands durch einen REST-`POST /rest/V1/inventory/source-items`-Aufruf geändert wird. <!-- ACP2E-1209-->

## v1.2.5

[!DNL Inventory Management] 1.2.5 (Modulversion: `magento/inventory-metapackage = 1.2.5`) wird mit Version 2.4.5 unterstützt und ist mit Version 2.4.0 von Adobe Commerce, Adobe Commerce on Cloud Infrastructure und der Magento Open Source Code Base kompatibel.

![Problem behoben](../assets/fix.svg) Der standardmäßige Lagerstatus von Paketen und gruppierten Produkten wird jetzt wie erwartet aktualisiert, wenn ein Händler eine Lieferung vom Administrator erstellt. Bislang blieb der Status dieser Waren nach der Herstellung einer Lieferung unverändert. <!--- ACP2E-418-->

![Problem behoben](../assets/fix.svg) Konfigurierbare Produkte werden jetzt wieder auf Lager gebracht, wenn eine der folgenden Bedingungen erfüllt ist: 1. Das übergeordnete Produkt hat mindestens ein gespeichertes untergeordnetes Element auf Lager. 2. Das konfigurierbare Produkt selbst wurde aktualisiert und als **auf Lager** festgelegt und hatte mindestens ein Kind auf Lager. <!--- ACP2E-443-->

![Problem behoben](../assets/fix.svg) Bestandsänderungen, die über die REST-API implementiert wurden, werden jetzt wie erwartet auf Produktdetailseiten angezeigt. Der Cache für Katalogprodukte wird jetzt bereinigt, nachdem der letzte und der aktuelle Lagerstatus verglichen wurden. Zuvor führte das Weglassen der Rückruffunktion zu einer fehlerhaften Auswertung von Bestandsstatusänderungen, wodurch die erforderliche Cache-Bereinigung nicht Trigger wurde. Infolgedessen spiegelt die Storefront die Bestandsänderungen nicht wider. <!--- ACP2E-161-->

![Problem behoben](../assets/fix.svg) Produkte, die dem Standardlager zugewiesen sind und zuvor nicht vorrätig waren, sind jetzt in der Storefront sichtbar, nachdem das Quellelement mithilfe von `/V1/inventory/source-items` aktualisiert wurde. Zuvor hatte dieser REST-API-Endpunkt die falsche `stock_status` festgelegt. <!--- ACP2E-562-->

![Es wurde ein Problem behoben](../assets/fix.svg) Die Zuweisung von Inventarquellen durch Massenaktionen (**[!UICONTROL Catalog]** > **[!UICONTROL Products]** > **[!UICONTROL Select Products]** > **[!UICONTROL Actions - Unassign Inventory Source]**) funktioniert jetzt wie erwartet, wenn Quellen doppelte SKUs mit Ausnahme einer führenden Null (z. B. `01234` und `1234`) enthalten. Zuvor hat die Anwendung die Zuweisung von Inventarquellen nicht aufgehoben und einen Fehler ausgegeben. <!--- ACP2E-2641-->

![Problem behoben](../assets/fix.svg) Der Produktbestandsstatus ist jetzt immer **auf Lager** wenn „Unendliche Rückbestellungen“ aktiviert ist und das Produkt unabhängig von der Menge der Rückbestellungen einem benutzerdefinierten Lager zugewiesen wird. Zuvor waren Produkte nicht vorrätig, auch wenn Auftragsrückstände aktiviert waren. <!--- ACP2E-664-->

![Problem behoben](../assets/fix.svg) Konfigurierbarer übergeordneter und untergeordneter Produktbestand wird jetzt korrekt aktualisiert, nachdem das Quellelement mit `POST /V1/inventory/source-items` aktualisiert wurde. Nachdem das untergeordnete Produkt über die API aktualisiert wurde, wird ein neues Inventar-Plug-in für standardmäßige Lagerprüfungen hinzugefügt und die konfigurierbare Produktmenge und der Status aktualisiert. <!--- ACP2E-442-->

![Problem behoben](../assets/fix.svg) Nicht vorrätige gruppierte Produkte werden nicht mehr auf der Seite „Storefront-Kategorie“ aufgeführt. <!--- ACP2E-2082-->

![Problem behoben](../assets/fix.svg) Der Paketname in `CatalogInventory` `composer.json` wurde korrigiert. <!--- ACP2E-2914-->

![Problem behoben](../assets/fix.svg) Der Status der Auftragsrückstände wird jetzt korrekt in der Admin angezeigt, nachdem eine Bestellung mit einer Produktmenge von null in einer Bereitstellung mit mehreren Quellen/Lagern aufgegeben wurde. [GitHub-33756](https://github.com/magento/magento2/issues/33756)-<!--- ACP2E-713-->

![Problem behoben](../assets/fix.svg) Nicht vorrätige Bundle-Produkte werden nicht mehr auf der Kategorieseite der Storefront angezeigt, wenn das Bundle-Produkt im Abschnitt Lager aktualisiert wird. <!--- ACP2E-2012-->

![Behobenes Problem](../assets/fix.svg) Kompatibilitätsprobleme mit PHP 7.4 wurden behoben. <!--- AC-3192-->

![Problem behoben](../assets/fix.svg) Die Leistung von Speichervorgängen, die Bundle-Produkte mit vielen Optionen (mehrere 100) enthalten, wurde verbessert. Zuvor dauerte das Speichern dieser großen Bundle-Produkte mehrere Minuten und führte manchmal zu Zeitüberschreitungen bei Bereitstellungen mit aktivierten Inventar-Services. [GitHub-34732](https://github.com/magento/magento2/issues/34732)-<!--- AC-1901-->

![Problem behoben](../assets/fix.svg) Das Aktionstool für Massenprodukte (**[!UICONTROL Select Products]** > **[!UICONTROL Actions]** > **[!UICONTROL Assign Inventory Source]**) funktioniert jetzt wie erwartet, wenn Sie mehreren Produkten eine Lagerquelle zuweisen, wenn SKUs dupliziert werden, mit Ausnahme eines führenden `0` (z. B. `01234` und `1234`). Zuvor wurde nur einem Produkt eine Lagerquelle zugewiesen. [GitHub-35171](https://github.com/magento/magento2/issues/35171)-<!--- AC-2584-->

![Problem behoben](../assets/fix.svg) Das Feld &quot;`ProductInterface.only_x_left_in_stock`&quot; gibt jetzt 0 zurück, wenn der Bestand 0 ist. Zuvor wurde null zurückgegeben. [GitHub-29932](https://github.com/magento/magento2/issues/29932)-<!--- AC-1806-->

![Problem behoben](../assets/fix.svg) Sie können jetzt das Standardlager über die Admin **[!UICONTROL Stores]** > **[!UICONTROL Inventory]** > **[!UICONTROL Stocks]** bearbeiten. Zuvor wurde in der Konsole ein JavaScript-Fehler angezeigt, als Sie versuchten, Quellen zum Standard-Stock hinzuzufügen oder daraus zu entfernen. Sie konnten jedoch Websites zum Standard-Stock zuweisen. <!--- ACP2E-545-->

![Problem behoben](../assets/fix.svg) <!--- ACP2E-274--> Die Produktanzahl der Kategorieliste ist jetzt korrekt, wenn der Inventar-Einzelquellenmodus mit aktivierter **[!UICONTROL Display Out-Of-Stock Products]** verwendet wird. Ein neues Plug-in verwendet jetzt `AreProductsSalableInterface` und `StockConfigurationInterface`, um die Gesamtzahl der Produkte zu ermitteln. Zuvor hat die Produktliste der Kategorie die falsche Produktmenge zurückgegeben.

![Problem behoben](../assets/fix.svg) <!--- ACP2E-322--> Konfigurierbare Produkte werden jetzt an die letzte Position in der Produktliste verschoben, nachdem der Lagerbestand aktualisiert wurde, wenn die **[!UICONTROL Move out of stock to the bottom]** aktiviert ist. Eine neue benutzerdefinierte Datenbankabfrage wird implementiert, um die Sortierreihenfolge der Elasticsearch-Indizes zu negieren, was die Sortierreihenfolge für Admin-aktivierte ignoriert. Zuvor wurden konfigurierbare Produkte und ihre untergeordneten Produkte nicht an das Ende der Liste verschoben, wenn diese Einstellung aktiviert war.

## v1.2.4

Inventory management 1.2.4 (Modulversion: `magento/inventory-metapackage = 1.2.4`) wird mit Version 2.4.4 unterstützt und ist mit Version 2.4.0 von Adobe Commerce, Adobe Commerce on Cloud Infrastructure und der Magento Open Source Code Base kompatibel.

![Problem behoben](../assets/fix.svg) Commerce zeigt jetzt für alle Produkte in der Admin-Produktlistenansicht einen genauen Verkaufsmengenwert an. Zuvor wurde ein leerer Wert für die verkäufliche Menge an Lagerprodukten mit SKUs angezeigt, die Sonderzeichen enthielten. <!--- MC-41936-->

![Problem behoben](../assets/fix.svg) Die Leistung bei Warenkorb- und Kassenaktionen wurde verbessert, z. B. beim Hinzufügen von Produkten zum Warenkorb in Bereitstellungen mit vielen (ca. 10.000) Inventarquellen. <!--- MC-42570-->

![Problem behoben](../assets/fix.svg) Der `bin/magento inventory:reservation:list-inconsistencies`-Befehl verarbeitet jetzt Bestellungen mit Teillieferungen korrekt, auch wenn die Reservierungen aus der Datenbank ausgelassen werden und der Cache geleert wurde. Zuvor hat Commerce beim Ausführen dieses Befehls mit einem vorab geleerten Cache den folgenden Fehler angezeigt: `Area code is not set`. <!--- MC-42142-->

![Problem behoben](../assets/fix.svg) Durch die inkrementelle Indizierung gruppierter untergeordneter Produktprodukte werden andere gruppierte Produkte nicht mehr falsch indiziert, wenn untergeordnete Produkte freigegeben werden. <!--- MC-41963-->

![Es wurde ](../assets/fix.svg) Problem behoben: Auf der Kategorieseite der Storefront wird jetzt die richtige Produktanzahl angezeigt, nachdem ein Produkt per API aus einer Kategorie entfernt wurde. Zuvor war die Produktzahl der Kategorieseite falsch, bis eine Neuindizierung stattfand. <!--- MC-42287-->

![Problem behoben](../assets/fix.svg) Konfigurierbare Produkte können jetzt beim Erstellen einer Gutschrift auf Lager zurückgegeben werden, wenn die Option **[!UICONTROL Manage Stock]** deaktiviert ist. Zuvor hat Commerce das Kontrollkästchen **Zurück an Lager** auf der Seite zur Erstellung von Gutschriften nicht angezeigt, wenn diese Option deaktiviert war. <!--- MC-42002-->

![Problem behoben](../assets/fix.svg) Die Verwaltung des Lagerbestands, der 10.000 Artikel überschreitet, wurde verbessert. Zuvor hinderten Leistungsprobleme Händler manchmal daran, den Bestand im Admin zu bearbeiten, bevor sie ihre Website aufriefen. <!--- MC-42643-->

![Problem behoben](../assets/fix.svg) Die Seite **[!UICONTROL User Roles]** in der Admin wird aktualisiert und bietet Admins eingeschränkte Berechtigungen für den Zugriff auf die Konfiguration der Versandmethoden. Der Abschnitt _Versandmethoden_ wurde in _[!UICONTROL Delivery methods]_umbenannt und_[!UICONTROL In-Store Pickup]_ wird unter den Abschnitt _[!UICONTROL Delivery methods]_verschoben. [GitHub-30053](https://github.com/magento/magento2/issues/30053)-<!--- MC-41545-->

![Problem behoben](../assets/fix.svg) Adobe Commerce erstellt keine doppelte Produktreservierung mehr, nachdem eine Gutschrift von der API aktualisiert wurde. <!--- MC-41757-->

![Es wurde ](../assets/fix.svg), dass beim Wechsel von der Registerkarte &quot;_[!UICONTROL Pick up in Store]_&quot; zur Registerkarte &quot;_[!UICONTROL Shipping]_&quot; im Checkout-Workflow kein JavaScript-Fehler mehr Trigger wird, wenn nur der In-Store-Pick-up-Versand verfügbar ist. <!--- MC-42808-->

![Problem behoben](../assets/fix.svg) Verkaufsfähige Produktmenge und Lagerproduktmenge werden jetzt korrekt synchronisiert. Zuvor wurde die Ausgleichszahlung für Lagerreservierungen für stornierte Bestellungen nicht neu erstellt. <!--- MC-42485-->

![Problem behoben](../assets/fix.svg) Die Leistung des Validators wurde optimiert, um das Hinzufügen einer neuen Quelle zum untergeordneten Produkt eines gebündelten Produkts mit dem Versandtyp `Ship Together` zu verhindern. <!--- MC-43039-->

## 1,2,3

[!DNL Inventory Management] 1.2.3 (Modulversion: `magento/inventory-metapackage = 1.2.3`) wird mit Version 2.4.3 unterstützt und ist mit Version 2.4.0 von Adobe Commerce, Adobe Commerce on Cloud Infrastructure und der Magento Open Source Code Base kompatibel.

![Problem behoben](../assets/fix.svg) Es wurden mehrere Probleme im Zusammenhang mit der Composite Product Visibility im Frontend behoben.

![Problem behoben](../assets/fix.svg) Verbesserte Warenkorbseiten-Management-Leistung mit der erforderlichen Mindestmenge.

![Problem behoben](../assets/fix.svg) Verschiedene Fehlerbehebungen zur Behebung von Problemen bei der Quellenerstellung, bei nicht vorrätigen Artikeln, bei der Beschaffung von Lagerbeständen, beim Sortieren zugewiesener Quellen, beim Versand im Geschäft und bei Lagerbefehlen.

![Problem behoben](../assets/fix.svg) [!DNL Commerce] unterstützt jetzt dreistellige kanadische Postleitzahlen für den Versand im Geschäft. Sechsstellige Codes werden aufgrund von Einschränkungen, die von `geonames.org` festgelegt wurden, nicht unterstützt.

![Problem behoben](../assets/fix.svg) Der Administrator zeigt jetzt für Bereitstellungen mit mehreren Stores die richtige Menge Standardvorräte für deaktivierte Produkte im **Produkte** und auf der **Produkt bearbeiten** an.

![Problem behoben](../assets/fix.svg) aktualisiert [!DNL Commerce] jetzt den Kategorie-Produkt-Cache, wenn ein Bundle-Produkt wieder auf Lager ist.

## 1.2.2

[!DNL Inventory Management] 1.2.2 (Modulversion: `magento/inventory-metapackage = 1.2.2`) wird mit Version 2.4.2 unterstützt und ist mit Version 2.4.0 von Adobe Commerce, Adobe Commerce on Cloud Infrastructure und der Magento Open Source Code Base kompatibel.

![Problem behoben](../assets/fix.svg) Es wurden mehrere Probleme im Zusammenhang mit der Composite Product Visibility im Frontend behoben.

![Problem behoben](../assets/fix.svg) Verbesserte Leistung der Warenkorbseite während der Mengenaktualisierung auf B2B.

![Problem behoben](../assets/fix.svg) Verschiedene Fehlerbehebungen zur Behebung von Problemen mit der Abholung im Geschäft, Massenaktualisierungen und dem Schwellenwert für die Bestandserfassung.

![Neu](../assets/new.svg) **Funktionstests.** führte neue Funktionstests ein und stellte Fehlerbehebungen für bestehende Tests bereit, um diese stabiler zu machen.

## 1.2.1

[!DNL Inventory Management] 1.2.1 (Modulversion: `magento/inventory-metapackage = 1.2.1`) wird mit Version 2.4.1 unterstützt und ist mit Version 2.4.0 von Adobe Commerce, Adobe Commerce on Cloud Infrastructure und der Magento Open Source Code Base kompatibel.

![Problem behoben](../assets/fix.svg) Bekanntes Problem im Zusammenhang mit dem `inventory_cleanup_reservations` Cron-Auftrag behoben und ein Problem im Zusammenhang mit der Funktion „In-Store-Abholung“ für Bundle-Produkte behoben. Dieses Update enthält auch allgemeine Verbesserungen bei der Lagerberechnung, der Produktunterstützung für Bundles und der Auftragsbearbeitungsfunktion.

![Neu](../assets/new.svg) **Funktionstests.** führte neue Funktionstests ein, um zusätzliche Abdeckung für die Funktion „In-Store-Abholung“ bereitzustellen.

## 1,2,0

[!DNL Inventory Management] 1.2.0 (Modulversion: `magento/inventory-metapackage = 1.2.0`) wird von Version 2.4.0 von Adobe Commerce, Adobe Commerce auf Cloud-Infrastruktur und der Magento Open Source Code-Basis unterstützt.

![Behobenes Problem](../assets/fix.svg) Zahlreiche Fehlerbehebungen zur Behebung von Problemen mit der Quellzuweisung, Unterstützung für skalierbare Umgebungen und Kompatibilität mit PHP 7.4, MySQL 8 und PHPUNIT 9.

![Neu](../assets/new.svg) **In-Store-Versandmethode.** wurde eine Option hinzugefügt, mit der Benutzer eine Quelle auswählen können, die während des Checkouts als Abholort verwendet werden soll. Siehe [In-Store-](../stores-purchase/shipping-in-store-delivery.md) im _Handbuch für Kauf und Verkauf_.

![Neu](../assets/new.svg) **Bundle-Produktunterstützung für den Multi-Source-Modus.** Inventar unterstützt alle Produkttypen mit mehreren Quellen.

![Neu](../assets/new.svg) **Asynchrone Stock-Neuindizierung.** wurde die Möglichkeit hinzugefügt, Stock asynchron neu zu indizieren und die Leistung mehrerer kritischer Szenarien zu verbessern.

![Neu](../assets/new.svg) **Massenschnittstellen.** Einführung neuer Bulk-Schnittstellen für die Skalierbarkeitsprüfung: `\Magento\InventorySalesApi\Api\AreProductsSalableInterface`, `\Magento\InventorySalesApi\Api\AreProductsSalableForRequestedQtyInterface`.

![Neu](../assets/new.svg) **Erhöhte Testabdeckung.** Neue Funktionen werden durch automatisierte Tests abgedeckt, einschließlich einer erweiterten Abdeckung erkannter und behobener Probleme.

![Bekanntes Problem](../assets/bug.svg) **Bekanntes Problem.** Das Fehlen des Felds `object_id` in den Reservierungs-Metadaten verhindert, dass der `inventory_cleanup_reservations` Cron-Auftrag ordnungsgemäß funktioniert. Dieses Problem wurde in [magento/inventory#3046) ](https://github.com/magento/inventory/pull/3046).

**Problemumgehung:** Führen Sie die folgenden MySQL-Abfragen aus, um Reservierungen manuell zu bereinigen:

```sql
SELECT GROUP_CONCAT(reservation_id) FROM inventory_reservation GROUP BY stock_id, sku HAVING SUM(quantity) = 0;
DELETE FROM inventory_reservation where reservation_id IN (result_of_the_first_query);
```

## 1,1,6

[!DNL Inventory Management] 1.1.6 (Modulversion: `inventory-composer-metapackage = 1.1.6`) wird mit Version 2.3.6 unterstützt und ist mit den Versionen 2.3.5, 2.3.4, 2.3.3, 2.3.2, 2.3.1 und 2.3.0 von Adobe Commerce, Adobe Commerce on Cloud Infrastructure und der Magento Open Source Code Base kompatibel.

![Behobenes Problem](../assets/fix.svg) Fehlerbehebungen zur Behebung von Problemen im Zusammenhang mit Auftragsrückständen, Gutschriften, niedrigem Lagerberichtsraster, Fehlerbehebungen im Zusammenhang mit dem CLI-Tool zur „Behebung von Inkonsistenzen“ und allgemeinen Verbesserungen.

![Neu](../assets/new.svg) **Asynchrone Stock-Neuindizierung.** wurde die Möglichkeit hinzugefügt, Stock asynchron neu zu indizieren und die Leistung mehrerer kritischer Szenarien zu verbessern.

## 1,1,5

[!DNL Inventory Management] 1.1.5 (Modulversion: `inventory-composer-metapackage = 1.1.5`) wird mit Version 2.3.5 unterstützt und ist mit den Versionen 2.3.4, 2.3.3, 2.3.2, 2.3.1 und 2.3.0 von Adobe Commerce, Adobe Commerce on Cloud Infrastructure und der Magento Open Source Code Base kompatibel.

![Neu](../assets/new.svg) **Inventar aktualisieren, sobald die Produkt-SKU geändert wird.** hat eine neue Konfigurationseinstellung zum Umschalten auf das neue Verhalten eingeführt: „Mit Katalog synchronisieren“.

![Neu](../assets/new.svg) **Funktionstests.** Es wurden neue Funktionstests eingeführt, um die Lücke bei der Testabdeckung zu schließen. Es wurden mehrere Probleme behoben, um Tests stabiler und zuverlässiger zu machen.)

![Bekanntes Problem](../assets/bug.svg) Fehlerbehebungen zur Verhinderung von Produktüberverkäufen, Sichtbarkeit nicht vorrätiger Produkte in der Storefront, zahlreiche Fehlerbehebungen für die Unterstützung skalierbarer Umgebungen und Verbesserungen der Benutzeroberfläche.

## 1,1,4

[!DNL Inventory Management] 1.1.4 (Modulversion: `inventory-composer-metapackage = 1.1.4`) wird mit Version 2.3.4 unterstützt und ist mit den Versionen 2.3.3, 2.3.2, 2.3.1 und 2.3.0 von Adobe Commerce, Adobe Commerce on Cloud Infrastructure und der Magento Open Source Code Base kompatibel.

![Behobenes Problem ](../assets/fix.svg)**Erhöhte Leistung.** wurde eine Bündelungslogik für den CLI-Befehl für Inventarreservierungen eingeführt, um die Speichernutzung zu reduzieren und Fälle zu vermeiden, in denen der Prozess ohne Antwort hängen bleibt.

![Neu ](../assets/new.svg)**Erhöhte Testabdeckung.** führte viele neue Funktionstests ein. Fast alle manuellen Inventarszenarien werden mit automatisierten Tests abgedeckt.

![Bekanntes Problem](../assets/bug.svg) Zahlreiche Fehlerbehebungen zur Behebung von Problemen mit Gutschriften, gruppierten Produkten sowie Quell- und Lagerdatenaktionen.

## 1.1.3

[!DNL Inventory Management] 1.1.3 (Modulversion: `inventory-composer-metapackage = 1.1.3`) wird mit Version 2.3.3 unterstützt und ist mit den Versionen 2.3.2, 2.3.1 und 2.3.0 von Adobe Commerce, Adobe Commerce on Cloud Infrastructure und der Magento Open Source Code Base kompatibel.

![Problem behoben ](../assets/fix.svg)**Bessere Integration mit Adobe Commerce- und B2B-Funktionen.** [!DNL Inventory Management] funktioniert jetzt mit den folgenden Funktionen für Websites, die nicht standardmäßige Inventarquellen und -bestände verwenden, ordnungsgemäß:

- Bestellung nach SKU (Adobe Commerce)
- Schnellbestellung (B2B)
- Anforderungslisten (B2B)

![Neu ](../assets/new.svg)**Erhöhte Leistung.** Leistung beim Durchsuchen des Storefront-Katalogs wurde für Websites verbessert, auf denen der standardmäßige Inventarbestand und die Standardquelle ausgeführt werden.

![Neu ](../assets/new.svg)**Erhöhte Testabdeckung.** Die Abdeckung der automatisierten Funktions- und Integrationstests hat deutlich zugenommen.

## 1.1.2

[!DNL Inventory Management] 1.1.2 (Modulversion: `inventory-composer-metapackage = 1.1.2`) wird mit Version 2.3.2 unterstützt und ist mit Version 2.3.1 und 2.3.0 von Adobe Commerce, Adobe Commerce on Cloud Infrastructure und der Magento Open Source Code Base kompatibel.

![Problem behoben](../assets/fix.svg) Der Antwort für den REST-Endpunkt GET `/V1/shipments` wurde ein `source_code` hinzugefügt. <!-- https://github.com/magento/inventory/pull/2142 -->

![Problem behoben](../assets/fix.svg) Problem behoben, um Reservierungen korrekt zu löschen und die Produktmengen nach der Ausstellung einer Gutschrift für eine nicht versendete Bestellung zu aktualisieren. Wenn Sie die zu <!-- https://github.com/magento/inventory/pull/2179 --> Option auswählen

![Problem behoben](../assets/fix.svg) Problem behoben, um Menge für konfigurierbare untergeordnete Produktelemente beim Eingeben von Mengen während der Produkterstellung korrekt zu speichern. <!-- https://github.com/magento/inventory/pull/2158 -->

Zu den neuen Modulen für [!DNL Inventory Management] 1.1.2 Beta gehören:

```php
        'Magento_InventoryGraphQl' => 1,
        'Magento_InventoryReservations' => 1,
        'Magento_InventoryReservationsApi' => 1,
        'Magento_InventoryReservationCli' => 1,
        'Magento_InventoryExportStock' => 0,
        'Magento_InventoryExportStockApi' => 0,
```

![Neu](../assets/new.svg) **Ein Massenendpunkt für die partielle Bestandsübertragung wurde hinzugefügt** - Aktuelle Massenübertragungs-Endpunkte verschieben alle zugewiesenen Mengen von einem Ursprung in eine Zielquelle. Mit dem neuen `/rest/V1/inventory/bulk-partial-source-transfer`-Endpunkt können Händler Teile des Lagers als Massenvorgang von der Quelle an die Quelle übertragen. Um einen bestimmten Mengenbetrag zu übertragen, geben Sie eine Anforderung an den Endpunkt mit den `sku`, `qty`, `origin_source_code` und `destination_source_code` ein. Übertragungen überprüfen, ob die Quelle dem `sku` zugewiesen ist, ob genügend Menge für die Übertragung vorhanden ist usw. Siehe [Massenaktionen für Inventar](https://developer.adobe.com/commerce/webapi/rest/inventory/bulk-inventory/){target="_blank"} in der REST-API-Dokumentation. <!-- https://github.com/magento/inventory/pull/2117 -->

![Neu](../assets/new.svg) **Reservierungs-CLI hinzugefügt** - Neue Befehle bieten Ihnen Optionen, um Reservierungsinkonsistenzen zu erkennen und zu beheben. Wenn Bestellungen eingehen und den Status ändern, generiert [!DNL Inventory Management] anfängliche Reservierungen und Aktualisierungen durch Vergütungsreservierungen. Diese Befehle geben eine Liste der erkannten Inkonsistenzen nach Auftrags-ID, SKU und Lager-ID zurück und erstellen Reservierungen, die behoben werden müssen. Weitere Informationen finden Sie in [CLI](cli.md)Referenz. <!-- https://github.com/magento/inventory/pull/2199 https://github.com/magento/inventory/pull/2184 https://github.com/magento/inventory/pull/2171 https://github.com/magento/inventory/pull/2148  -->

![Neu](../assets/new.svg) **Leistungsverbesserungen für Quellen und SSA-Optionen** - Das Sortieren und Auswählen von Quellen während des Versands führte zu Leistungseinbußen bei Beständen mit einer hohen Anzahl von Quellen. Diese Version bietet erhebliche Leistungsverbesserungen bei der Auflistung und Sortierung verfügbarer Quellen bei der Überprüfung und Auswahl von SSA-Optionen in Sendungen. <!-- https://github.com/magento/inventory/pull/2056 https://github.com/magento/inventory/pull/2090 -->

![Neu](../assets/new.svg) **GraphQL-Unterstützung für Inventory management hinzugefügt** - In dieser Version wird ein neues `magento/module-inventory-graph-ql` installiert. Die GraphQL [ProductInterface-Attribute](https://developer.adobe.com/commerce/webapi/graphql/schema/products/interfaces/attributes/){target="_blank"} enthalten jetzt die `only_x_left_in_stock`- und `stock_status` für [!DNL Inventory Management] Unterstützung. <!-- https://github.com/magento/inventory/pull/2124 -->

![Neu](../assets/new.svg) **Vereinfachte Benutzeroberfläche für Zugewiesene Quellen** - Die Tabelle Zugewiesene Quellen auf Produktseiten enthält vereinfachte Inhalte für einfachere Aktualisierungen und erhöhte Leistung bei der Anzeige vieler Quellen. Alle Quellen werden nach Quellnamen aufgelistet (bewegen Sie den Mauszeiger über `source_code`).

![Neu](../assets/new.svg) **Aggregierter Lagerdienst exportieren** - Diese Version bietet einen neuen aggregierten Lagerdienst für den Export (Reservierungen im System beibehalten), um externe Sales Channel wie Amazon, eBay und Google Shopping-Anzeigen zu unterstützen.  <!-- https://github.com/magento/inventory/pull/2067 -->

## 1,1,0

[!DNL Inventory Management] 1.1.0 (Modulversion: `inventory-composer-metapackage = 1.1.0`) wird unterstützt und ist mit Version 2.3.0 von Adobe Commerce, Adobe Commerce on Cloud Infrastructure und der Magento Open Source Code Base kompatibel. [!DNL Inventory Management] 1.1.1 wird nur als Paketnamen-Update veröffentlicht, wird für Version 2.3.1 unterstützt und ist mit Version 2.3.0 von Adobe Commerce, Adobe Commerce on Cloud Infrastructure und der Magento Open Source Code Base kompatibel.

![Problem behoben](../assets/fix.svg) **Es wurde Unterstützung für Elasticsearch für Einzel- und** hinzugefügt. - Sie können jetzt Elasticsearch mit benutzerdefinierten Lagern konfigurieren und verwenden. Siehe [Einrichten des Elasticsearch-](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure/service/elasticsearch.html){target="_blank"}) für Installationsinformationen. <!-- PR https://github.com/magento/inventory/pull/1943 -->

![Problem behoben](../assets/fix.svg) Es wurden Leistungsprobleme mit Default Stock behoben, um die Leistung bei zahlreichen Vorgängen drastisch zu steigern. Durch Verbesserungen wird die Leistung für den Single-Source-Modus, die Übertragung von Inventar an Source, die Kategorieseiten der Storefront und die Berechnung der Verkaufsmenge gesteigert.

<!-- All Performance Track issues resolved https://github.com/magento/inventory/issues?q=is%3Aopen+is%3Aissue+label%3APerformance -->

![Problem behoben](../assets/fix.svg) Behobene Probleme mit dem Status „Nicht vorrätig“ und der Masseninventarübertragung an Lager für konfigurierbare und gruppierte Produkte. Die Auswahl der übergeordneten Produkte und die Durchführung von Massenaktionen hat keine Auswirkungen auf den Produktstatus. Wenn das übergeordnete Produkt auf Lager war, bleibt es auf Lager.

<!-- PR https://github.com/magento/inventory/pull/1972 -->

![Neu](../assets/new.svg) **Distance Priority Algorithm** - Der Distance Priority Algorithm ist ein neuer, vorkonfigurierter Source-Auswahlalgorithmus für Versandempfehlungen auf Distanzbasis. Dieser Algorithmus vergleicht den Ort der Versandzieladresse mit den Quellorten, um die nächstgelegene Quelle für die Lieferungen zu ermitteln. Die Entfernung kann entweder durch die physische Entfernung oder die Zeit bestimmt werden, die mit der Reise von einem Ort zum anderen verbracht wurde, wobei importierte Geocode-Standortdaten oder Google-Richtungen (Fahren, Gehen oder Fahrradfahren) verwendet werden.

![Neu](../assets/new.svg) **Erweiterte Quellmengenliste** - Händler mit einer hohen Anzahl von Quellen können einfach den Mauszeiger über alle Quellen pro Produkt bewegen und diese über das Produktraster anzeigen. Jedes Produkt zeigt mindestens fünf Quellen und passende Mengen an. Wenn Sie den Mauszeiger über die Quellen bewegen, können Sie durch die gesamte Liste der Quellen und aktuellen Mengen scrollen.

![Bekanntes Problem](../assets/bug.svg) Bekanntes Problem mit Magento Open Source und Adobe Commerce v2.3.1 - Asynchrone Datenmigration zwischen Quellen tritt auf Probleme aufgrund von Änderungen in asynchronen APIs mit Themennamen, die PHP-Klassen- und Methodennamen widerspiegeln. Es wird empfohlen, synchrone Vorgänge zu verwenden und **[!UICONTROL Run asynchronously]** auf `No` festzulegen.
