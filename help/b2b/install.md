---
title: Installieren der [!DNL Adobe Commerce B2B] Erweiterung
description: Erfahren Sie, wie Sie das [!DNL Adobe Commerce B2B] Metapaket installieren.
feature: B2B, Install
role: Admin, Developer
exl-id: a6947212-1708-40ae-9e81-874467eba5e1
source-git-commit: be36742aa1214e7e8e7f343051336cd3635099f4
workflow-type: tm+mt
source-wordcount: '1086'
ht-degree: 0%

---


# Installieren der Erweiterung [!DNL Adobe Commerce B2B]

Die Adobe Commerce B2B-Erweiterung `magento/extension-b2b` ist für alle unterstützten Versionen von Adobe Commerce verfügbar. Es wird nach der Installation von Adobe Commerce installiert.


## Voraussetzungen

- [Adobe Commerce](https://business.adobe.com/products/magento/magento-commerce.html), alle unterstützten Versionen
- PHP 8.1 / 8.2 / 8.3
- [!DNL Composer]

## Unterstützte Plattformen

- Adobe Commerce über Cloud-Infrastruktur (ECE)
- Adobe Commerce vor Ort (EE)

## Installationsschritte

>[!BEGINSHADEBOX]

**Voraussetzungen**

- Zugriff auf [repo.magento.com](https://repo.magento.com/) , um die Erweiterung herunterzuladen. Informationen zur Schlüsselgenerierung und zum Abrufen der erforderlichen Berechtigungen finden Sie unter [Abrufen Ihrer Authentifizierungsschlüssel](https://experienceleague.adobe.com/en/docs/commerce-operations/installation-guide/prerequisites/authentication-keys).

  Speichern Sie Authentifizierungsschlüssel für die Installation, indem Sie sie global im Verzeichnis [COMPOSER_HOME](https://getcomposer.org/doc/03-cli.md#composer-home) definieren. Oder speichern Sie sie in einer [auth.json](https://developer.adobe.com/commerce/contributor/guides/install/clone-repository/#authentication-file) -Datei im Stammverzeichnis der Adobe Commerce-Anwendung.

- [Unterstützte Version der B2B-Erweiterung](https://experienceleague.adobe.com/en/docs/commerce-operations/release/product-availability) - Bestimmen Sie die neueste Version der B2B-Erweiterung, die von der bereitgestellten Adobe Commerce-Version unterstützt wird.

- In den Versionshinweisen finden Sie die aktuellen Informationen zur Versionskompatibilität, zu Aktualisierungen oder Änderungen, die sich auf die Installations- oder Aktualisierungsanforderungen auswirken können.

   - [B2B-Versionshinweise](release-notes.md)
   - [Adobe Commerce - Versionshinweise](https://experienceleague.adobe.com/en/docs/commerce-operations/release/versions)

>[!ENDSHADEBOX]

Installieren Sie die B2B-Erweiterung (`magento/b2b-extension`) mit Composer. Die Erweiterung ist ein Composer-Metapaket, das die Sammlung von Modulen enthält, die die B2B-Funktionen für eine Adobe Commerce-Instanz aktivieren. Eine Liste der enthaltenen Module finden Sie unter [B2B-Pakete](packages.md).

>[!BEGINTABS]

>[!TAB Cloud-Infrastruktur]

>[!TIP]
>
>Bei der Installation von Adobe Commerce B2B in der Cloud-Infrastruktur empfiehlt Adobe, dass Sie Ihre Adobe Commerce-Anwendung vor dem Beginn in einer Integrations- oder Staging-Umgebung bereitstellen.

Adobe empfiehlt, in einer Entwicklungsverzweigung zu arbeiten, wenn Sie die B2B-Erweiterung zu Ihrem Projekt hinzufügen. Wenn Sie keine Verzweigung haben, finden Sie weitere Informationen unter [Erstellen einer Verzweigung für die Entwicklung](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/cli-branches). Bei der Installation der B2B-Erweiterung wird der Name der `Magento_B2b`-Erweiterung automatisch in die Datei `app/etc/config.php` eingefügt. Die Datei muss nicht direkt bearbeitet werden.

**Installieren der B2B-Erweiterung**:

1. Wechseln Sie auf Ihrer lokalen Workstation zum Projektverzeichnis.

1. Erstellen oder checken Sie einen Entwicklungszweig aus.

1. Fügen Sie die B2B-Erweiterung zum Abschnitt `require` der Datei `composer.json` hinzu.

   ```bash
   composer require magento/extension-b2b --no-update
   ```

1. Aktualisieren Sie die Projektabhängigkeiten.

   ```bash
   composer update
   ```

1. Hinzufügen, Übertragen und Push-Code-Änderungen.

   ```bash
   git add -A
   ```

   ```bash
   git commit -m "Install the B2B extension."
   ```

   ```bash
   git push origin <branch-name>
   ```

   >[!NOTE]
   >
   >Durch das Übermitteln von Aktualisierungen an die Cloud-Umgebung wird der Commerce-Cloud-Bereitstellungsprozess initiiert, um die Änderungen anzuwenden. Überprüfen Sie den Bereitstellungsstatus im [Bereitstellungsprotokoll](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/deploy/process). Wenn Bereitstellungsfehler auftreten, finden Sie weitere Informationen unter [Wiederherstellen nach Komponentenfehler](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/deploy/recover-failed-deployment).

1. Nachdem der Build und die Bereitstellung abgeschlossen sind, melden Sie sich mit SSH bei der Remote-Umgebung an und überprüfen Sie, ob die B2B-Erweiterung installiert und aktiviert ist.

   ```bash
   bin/magento module:status Magento_B2b
   ```

   Ein Erweiterungsname verwendet das folgende Format: `<VendorName>_<ComponentName>`.

   Beispielantwort:

   ```terminal
   Magento_B2b : Module is enabled
   ```

>[!TAB On-premise]

1. Aktualisieren Sie im Stammverzeichnis der Adobe Commerce-Anwendung die `composer.json` -Variable, um die Abhängigkeiten für die B2B-Erweiterung hinzuzufügen:

   ```bash
   composer require magento/extension-b2b:<version>
   ```

   Wenn beispielsweise ein Fehler auftritt:

   ```terminal
   [InvalidArgumentException] Could not find a matching version of package magento/extension-b2b.
   ```

   Überprüfen Sie die Rechtschreibung des Pakets, Ihre Versionsbeschränkung und ob das Paket verfügbar ist und mit Ihrer Mindestanforderung an die Stabilität (stabil) übereinstimmt.

1. Geben Sie bei Aufforderung die [Authentifizierungsschlüssel](https://experienceleague.adobe.com/en/docs/commerce-operations/installation-guide/prerequisites/authentication-keys) ein.

   Ihr _öffentlicher Schlüssel_ ist Ihr Benutzername; Ihr _privater Schlüssel_ ist Ihr Kennwort. Wenn Sie Ihre öffentlichen und privaten Schlüssel in `auth.json` gespeichert haben, werden Sie nicht zur Authentifizierung aufgefordert.

1. Führen Sie die folgenden Befehle aus, nachdem der Composer die Module aktualisiert hat:

   ```bash
   bin/magento setup:upgrade
   ```

   ```bash
   bin/magento setup:di:compile
   ```

   ```bash
   bin/magento setup:static-content:deploy -f
   ```

   ```bash
   bin/magento cache:clean
   ```

   >[!NOTE]
   >
   >Im Produktionsmodus erhalten Sie möglicherweise eine Nachricht an `Please rerun Magento compile command`. Geben Sie die Befehle ein, um die Installation abzuschließen. Adobe Commerce fordert Sie nicht auf, den Befehl &quot;Kompilieren&quot;im Entwicklermodus auszuführen.

>[!ENDTABS]

Konfigurieren und starten Sie nach Abschluss der Installation den Nachrichtenabnehmer.

## Verbraucher informieren

Die Adobe Commerce B2B-Erweiterung verwendet MySQL für die Verwaltung von Nachrichtenwarteschlangen. In der folgenden Tabelle sind die Nachrichtenkunden aufgeführt, die B2B-Funktionen unterstützen. Nachdem Sie die Erweiterung installiert haben, starten Sie die Nachricht für die B2B-Funktionen, die für Ihre Commerce-Storefront erforderlich sind.

| Verbraucher | Beschreibung |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `sharedCatalogUpdatePrice` | Aktualisiert den Preis für jedes Produkt in einem freigegebenen Katalog. Erforderlich, wenn die Option [**[!UICONTROL Shared Catalogs]**](catalog-shared.md) in den Konfigurationseinstellungen des Admin-Systems aktiviert ist. |
| `sharedCatalogUpdateCategoryPermissions` | Aktualisiert Kategorien, die einer freigegebenen Katalogkategorie zugewiesen sind. Erforderlich, wenn die Option [**[!UICONTROL Shared Catalogs]**](catalog-shared.md) in den Konfigurationseinstellungen des Admin-Systems aktiviert ist. |
| `negotiableQuotePriceUpdate` | Aktualisiert die Preise für verhandelbare Kurse. Erforderlich, wenn die Option [**[!UICONTROL Quotes]**](quotes.md) in den Konfigurationseinstellungen des Admin-Systems aktiviert ist. |
| `purchaseorder.toorder` | Konvertiert eine Bestellung in eine Bestellung. Erforderlich, wenn die Option [**[!UICONTROL Purchase Orders]**](purchase-order-flow.md) in den Konfigurationseinstellungen des Admin-Systems aktiviert ist. |
| `purchaseorder.transactional.email` | Senden Sie E-Mails zur Bestellung. Erforderlich, wenn die Option [**[!UICONTROL Purchase Orders]**](purchase-order-flow.md) in den Konfigurationseinstellungen des Admin-Systems aktiviert ist. |
| `purchaseorder.validation` | Validiert die Bestellung anhand der relevanten [Validierungsregeln](account-dashboard-approval-rules.md). Erforderlich, wenn die Option [**[!UICONTROL Purchase Orders]**](purchase-order-flow.md) in den Konfigurationseinstellungen des Admin-Systems aktiviert ist. |
| `quoteItemCleaner` | Löscht ungültige oder inaktive Preisangebote, wenn ein Produkt aus dem Katalog gelöscht oder aus dem Warenkorb entfernt wird. Erforderlich, wenn die Option [**[!UICONTROL Quotes]**](quotes.md) in den Konfigurationseinstellungen des Admin-Systems aktiviert ist. |
| `inventoryQtyCounter` | Korrigiert den Aktienindex asynchron, nachdem eine Bestellung platziert oder ein Produkt entfernt wurde. Erforderlich, wenn die Option [**[!UICONTROL Use deferred stock update]**](../configuration-reference/catalog/inventory.md#product-stock-options) in den Admin-Konfigurationseinstellungen für Inventory management aktiviert ist. Siehe [Best Practices für die Leistung](https://experienceleague.adobe.com/en/docs/commerce-operations/performance-best-practices/configuration#deferred-stock-update). |
| `async.operations.all` | Erstellt Nachrichten für jede einzelne Aufgabe eines [Massenvorgangs](https://developer.adobe.com/commerce/php/development/components/message-queues/bulk-operations/), z. B. den Import oder Export von Artikeln, die Preisänderung in großem Maßstab und die Zuweisung von Produkten zu einem Lager. Erforderlich, wenn die Option [**Massenvorgänge verwalten**](../configuration-reference/catalog/inventory.md#admin-bulk-operations) für [!DNL Inventory Management] in den Konfigurationseinstellungen des Admin-Systems auf **Asynchron ausführen** gesetzt ist. |

{style="table-layout:auto"}

>[!NOTE]
>
>Eine Liste aller Adobe Commerce-Nachrichtenkonsumenten finden Sie unter [Konsumenten in der Nachrichtenwarteschlange](https://experienceleague.adobe.com/en/docs/commerce-operations/configuration-guide/message-queues/consumers) im _Konfigurationshandbuch_.

### Konfigurieren von Nachrichtenbenutzern

Vermeiden Sie mögliche Verarbeitungsprobleme oder -verzögerungen, indem Sie die folgenden Parameter hinzufügen, wenn Sie [die Nachricht &quot;Consumer starten&quot;](#start-message-consumers) für B2B-Funktionen starten.

- `--max-messages <value>` - Gibt die maximale Anzahl von Nachrichten an, die jeder Verbraucher vor dem Beenden verarbeiten muss (Standard = 10000). Obwohl Adobe es nicht empfiehlt, können Sie mit 0 verhindern, dass der Verbraucher beendet wird. Die Best Practice für eine PHP-Anwendung besteht darin, langwierige Prozesse neu zu starten, um mögliche Speicherlecks zu vermeiden.

- `--batch-size <value>` - Ermöglicht Ihnen, die vom Verbraucher verbrauchten Systemressourcen (CPU, Speicher) zu begrenzen. Die Verwendung kleinerer Batches verringert die Ressourcenbelegung und führt so zu einer langsameren Verarbeitung.  Wenn dies angegeben ist, werden Nachrichten in einer Warteschlange in Batches mit jeweils `<value>` verbraucht. Diese Option gilt nur für den Batch-Benutzer. Wenn `--batch-size` nicht definiert ist, empfängt der Batch-Verbraucher alle verfügbaren Nachrichten in einer Warteschlange.

Weitere Informationen zu zusätzlichen Konfigurationsoptionen finden Sie unter [Spezifische Konfiguration](https://experienceleague.adobe.com//en/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues#specific-configuration).

### Starten von Nachrichtenempfängern

Um asynchrone Vorgänge für B2B-Funktionen zu aktivieren, müssen Sie mehrere Nachrichtenverbraucher starten.

1. Geben Sie die verfügbaren E-Mail-Verbraucher an:

   ```bash
   bin/magento queue:consumers:list
   ```

   Der Befehl gibt verfügbare Nachrichtenkunden zurück, einschließlich aller [B2B-Nachrichtennutzer](#message-consumers).

1. Jeden Verbraucher einzeln starten:

   ```bash
   bin/magento queue:consumers:start [--max-messages=<value>] [--batch-size=<value>] <consumer_name>
   ```

   Beispiel:

   ```bash
   bin/magento queue:consumers:start quoteItemCleaner
   ```

>[!TIP]
>
>Um es im Hintergrund auszuführen, hängen Sie `&` an den Befehl an, kehren Sie zu einer Eingabeaufforderung zurück und fahren Sie mit der Ausführung der Befehle fort. Beispiel: `bin/magento queue:consumers:start sharedCatalogUpdatePrice &`.

Weitere Informationen finden Sie unter [Verwalten von Nachrichtenwarteschlangen](https://experienceleague.adobe.com/en/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues) im _Konfigurationshandbuch_.

### Hinzufügen von Nachrichtenkonsumenten zu Cron

Sie können den Ausführungsplan für die Benutzer der Nachrichten `SharedCatalogUpdateCategoryPermissions` und `SharedCatalogUpdatePrice` automatisieren, indem Sie den Zeitplan zur cron-Konfigurationsdatei [/app/code/Magento/MessageQueue/etc/crontab.xml](https://experienceleague.adobe.com/en/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues#process-management) hinzufügen.

```terminal
* * * * * ps ax | grep [s]haredCatalogUpdateCategoryPermissions >>/dev/null 2>&1 || nohup php /var/www/html/magento2/bin/magento queue:consumers:start sharedCatalogUpdateCategoryPermissions &
* * * * * ps ax | grep [s]haredCatalogUpdatePrice >>/dev/null 2>&1 || nohup php /var/www/html/magento2/bin/magento queue:consumers:start sharedCatalogUpdatePrice &
```

Sie können Zeitpläne für Nachrichtennutzer auch über die Einstellungen für die Store-Konfiguration ](../systems/cron.md) in der Admin-Konsole konfigurieren.[

## B2B-Funktionen in Admin aktivieren

Nach der Installation der Adobe Commerce-B2B-Erweiterung und dem Starten der Nachrichtenverbraucher müssen Sie auch [B-Funktionen in Admin](enable-basic-features.md) aktivieren.

