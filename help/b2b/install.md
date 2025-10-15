---
title: Installieren der  [!DNL Adobe Commerce B2B] -Erweiterung
description: Erfahren Sie, wie Sie das  [!DNL Adobe Commerce B2B] -Paket installieren.
feature: B2B, Install
role: Admin, Developer
exl-id: a6947212-1708-40ae-9e81-874467eba5e1
badgePaas: label="Nur PaaS" type="Informative" url="https://experienceleague.adobe.com/de/docs/commerce/user-guides/product-solutions" tooltip="Gilt nur für Adobe Commerce in Cloud-Projekten (von Adobe verwaltete PaaS-Infrastruktur) und lokale Projekte."
source-git-commit: 25964363ca5c4ec849e231d4eccb5f60b682a499
workflow-type: tm+mt
source-wordcount: '1149'
ht-degree: 0%

---


# Installieren der [!DNL Adobe Commerce B2B]

Die Adobe Commerce B2B-Erweiterung `magento/extension-b2b` ist für alle unterstützten Versionen von Adobe Commerce verfügbar. Sie wird nach der Installation von Adobe Commerce installiert.


## Anforderungen

- [Adobe Commerce](https://business.adobe.com/de/products/magento/magento-commerce.html), alle unterstützten Versionen
- PHP 8.1, 8.2 und 8.3 (erfordert B2B 1.5.0)
- [!DNL Composer]

>[!IMPORTANT]
>
>Adobe Commerce B2B ab Version 1.4.2 ist nicht mit PHP 8.3 kompatibel. Wenn Sie die Commerce-Instanz auf Commerce Version 2.4.7+ aktualisieren, stellen Sie sicher, dass die auf der Instanz installierte PHP-Version PHP 8.2 ist, um die Kompatibilität mit B2B 1.4.2+ beizubehalten.

## Unterstützte Plattformen

- Adobe Commerce auf Cloud-Infrastruktur (ECE)
- Adobe Commerce On-Premises (EE)

## Installationsschritte

>[!BEGINSHADEBOX]

**Voraussetzungen**

- Zugriff auf [repo.magento.com](https://repo.magento.com/) zum Herunterladen der Erweiterung. Informationen zum Generieren von Schlüsseln und zum Abrufen der erforderlichen Berechtigungen finden Sie unter [Abrufen Ihrer Authentifizierungsschlüssel](https://experienceleague.adobe.com/de/docs/commerce-operations/installation-guide/prerequisites/authentication-keys).

  Speichern Sie Authentifizierungsschlüssel für die Installation, indem Sie sie global im Verzeichnis [COMPOSER_HOME](https://getcomposer.org/doc/03-cli.md#composer-home) definieren. Oder speichern Sie sie in einer [auth.json](https://developer.adobe.com/commerce/contributor/guides/install/clone-repository/#authentication-file)-Datei im Stammverzeichnis der Adobe Commerce-Anwendung.

- [Unterstützte Version der B2B-Erweiterung](https://experienceleague.adobe.com/de/docs/commerce-operations/release/product-availability) - Ermitteln Sie die neueste Version der B2B-Erweiterung, die von der bereitgestellten Adobe Commerce-Version unterstützt wird.

- In den Versionshinweisen finden Sie die neuesten Informationen zur Versionskompatibilität, zu Updates oder Änderungen, die sich auf Installations- oder Upgrade-Anforderungen auswirken können.

   - [B2B-Versionshinweise](release-notes.md)
   - [Versionshinweise zu Adobe Commerce](https://experienceleague.adobe.com/de/docs/commerce-operations/release/versions)

>[!ENDSHADEBOX]

Installieren Sie die B2B-Erweiterung (`magento/b2b-extension`) mit dem Composer. Die -Erweiterung ist ein Composer-Metapaket, das die Auflistung von -Modulen enthält, die die B2B-Funktionen für eine Adobe Commerce-Instanz aktivieren. Eine Liste der enthaltenen Module finden Sie unter [B2B-](packages.md).

>[!BEGINTABS]

>[!TAB Cloud-Infrastruktur]

>[!TIP]
>
>Bei der Installation von Adobe Commerce B2B auf einer Cloud-Infrastruktur empfiehlt Adobe, Ihre Adobe Commerce-Anwendung in einer Integrations- oder Staging-Umgebung bereitzustellen, bevor Sie beginnen.

Adobe empfiehlt, in einer Entwicklungsverzweigung zu arbeiten, wenn Sie Ihrem Projekt die B2B-Erweiterung hinzufügen. Wenn Sie keine Verzweigung haben, lesen Sie [Erstellen einer Verzweigung für die Entwicklung](https://experienceleague.adobe.com/de/docs/commerce-cloud-service/user-guide/develop/cli-branches). Bei der Installation der B2B-Erweiterung wird der Name der `Magento_B2b`-Erweiterung automatisch in die `app/etc/config.php`-Datei eingefügt. Es ist nicht erforderlich, die Datei direkt zu bearbeiten.

**So installieren Sie die B2B-**:

1. Wechseln Sie auf Ihrer lokalen Workstation in Ihr Projektverzeichnis.

1. Erstellen oder Auschecken einer Entwicklungsverzweigung.

1. Fügen Sie die B2B-Erweiterung zum Abschnitt `require` der `composer.json` hinzu.

   ```bash
   composer require magento/extension-b2b --no-update
   ```

1. Aktualisieren Sie die Projektabhängigkeiten.

   ```bash
   composer update
   ```

1. Code-Änderungen hinzufügen, übertragen und per Push übertragen.

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
   >Durch das Pushen von Aktualisierungen an die Cloud-Umgebung wird der Commerce-Cloud-Bereitstellungsprozess gestartet, um die Änderungen anzuwenden. Überprüfen Sie den Bereitstellungsstatus im [Bereitstellungsprotokoll](https://experienceleague.adobe.com/de/docs/commerce-cloud-service/user-guide/develop/deploy/process). Wenn Sie auf Bereitstellungsfehler stoßen, lesen Sie [Nach Komponentenfehler wiederherstellen](https://experienceleague.adobe.com/de/docs/commerce-cloud-service/user-guide/develop/deploy/recover-failed-deployment).

1. Nachdem der Build und die Bereitstellung abgeschlossen sind, verwenden Sie SSH, um sich bei der Remote-Umgebung anzumelden und sicherzustellen, dass die B2B-Erweiterung installiert und aktiviert ist.

   ```bash
   bin/magento module:status Magento_B2b
   ```

   Ein Erweiterungsname verwendet das Format `<VendorName>_<ComponentName>`.

   Beispielantwort:

   ```
   Magento_B2b : Module is enabled
   ```

>[!TAB On-Premises]

1. Aktualisieren Sie im Stammverzeichnis der Adobe Commerce-Anwendung die `composer.json` , um die Abhängigkeiten für die B2B-Erweiterung hinzuzufügen:

   ```bash
   composer require magento/extension-b2b:<version>
   ```

   Wenn ein Fehler auftritt, zum Beispiel:

   ```
   [InvalidArgumentException] Could not find a matching version of package magento/extension-b2b.
   ```

   Überprüfen Sie die Schreibweise des Pakets, Ihre Versionsbeschränkung und, ob das Paket verfügbar ist und Ihren Mindestanforderungen an die Stabilität (stabil) entspricht.

1. Geben Sie bei Aufforderung Ihre [Authentifizierungsschlüssel](https://experienceleague.adobe.com/de/docs/commerce-operations/installation-guide/prerequisites/authentication-keys) ein.

   Ihr _öffentlicher Schlüssel_ ist Ihr Benutzername; Ihr _privater Schlüssel_ ist Ihr Kennwort. Wenn Sie Ihre öffentlichen und privaten Schlüssel in `auth.json` gespeichert haben, werden Sie nicht aufgefordert, sich zu authentifizieren.

1. Führen Sie die folgenden Befehle aus, nachdem Composer die Aktualisierung der Module abgeschlossen hat:

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
   >Im Produktionsmodus erhalten Sie möglicherweise eine Nachricht an `Please rerun Magento compile command`. Geben Sie die Befehle ein, um die Installation abzuschließen. Adobe Commerce fordert Sie nicht auf, den Kompilierungsbefehl im Entwicklermodus auszuführen.

>[!ENDTABS]

Konfigurieren und starten Sie nach Abschluss der Installation Message Consumer.

## Nachrichtenkonsumenten

Die Adobe Commerce B2B-Erweiterung verwendet MySQL für die Verwaltung von Nachrichtenwarteschlangen. In der folgenden Tabelle sind die Nachrichtenkonsumenten aufgeführt, die B2B-Funktionen unterstützen. Starten Sie nach der Installation der Erweiterung die Nachricht Consumer für die B2B-Funktionen, die für Ihre Commerce-Storefront erforderlich sind.

| Verbraucher | Beschreibung |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `sharedCatalogUpdatePrice` | Aktualisiert den Preis für jedes Produkt in einem freigegebenen Katalog. Erforderlich, wenn die Option [**[!UICONTROL Shared Catalogs]**](catalog-shared.md) in den Konfigurationseinstellungen des Admin-Systems aktiviert ist. |
| `sharedCatalogUpdateCategoryPermissions` | Aktualisiert Kategorien, die einer freigegebenen Katalogkategorie zugewiesen sind. Erforderlich, wenn die Option [**[!UICONTROL Shared Catalogs]**](catalog-shared.md) in den Konfigurationseinstellungen des Admin-Systems aktiviert ist. |
| `negotiableQuotePriceUpdate` | Aktualisiert Preise für verhandelbare Angebote. Erforderlich, wenn die Option [**[!UICONTROL Quotes]**](quotes.md) in den Konfigurationseinstellungen des Admin-Systems aktiviert ist. |
| `purchaseorder.toorder` | Wandelt eine Bestellung in eine Bestellung um. Erforderlich, wenn die Option [**[!UICONTROL Purchase Orders]**](purchase-order-flow.md) in den Konfigurationseinstellungen des Admin-Systems aktiviert ist. |
| `purchaseorder.transactional.email` | Senden Sie E-Mails zu Bestellungen. Erforderlich, wenn die Option [**[!UICONTROL Purchase Orders]**](purchase-order-flow.md) in den Konfigurationseinstellungen des Admin-Systems aktiviert ist. |
| `purchaseorder.validation` | Validiert eine Bestellung anhand der relevanten [Genehmigungsregeln](account-dashboard-approval-rules.md). Erforderlich, wenn die Option [**[!UICONTROL Purchase Orders]**](purchase-order-flow.md) in den Konfigurationseinstellungen des Admin-Systems aktiviert ist. |
| `quoteItemCleaner` | Löscht ungültige oder inaktive Preisangebote, wenn ein Produkt aus dem Katalog gelöscht oder aus dem Warenkorb entfernt wird. Erforderlich, wenn die Option [**[!UICONTROL Quotes]**](quotes.md) in den Konfigurationseinstellungen des Admin-Systems aktiviert ist. |
| `inventoryQtyCounter` | Korrigiert asynchron den Aktienindex, nachdem eine Bestellung aufgegeben oder ein Produkt entfernt wurde. Erforderlich, wenn die Option [**[!UICONTROL Use deferred stock update]**](../configuration-reference/catalog/inventory.md#product-stock-options) für Inventory management in den Admin-Konfigurationseinstellungen aktiviert ist. Siehe [Best Practices für die Leistung](https://experienceleague.adobe.com/de/docs/commerce-operations/performance-best-practices/configuration#deferred-stock-update). |
| `async.operations.all` | Erstellt Nachrichten für jede einzelne Aufgabe eines [Massenvorgangs“, &#x200B;](https://developer.adobe.com/commerce/php/development/components/message-queues/bulk-operations/). B. den Import oder Export von Artikeln, die Änderung von Preisen in großem Maßstab und die Zuweisung von Produkten zu einem Lager. Erforderlich, wenn die Option [**Massenvorgänge von Administratoren**](../configuration-reference/catalog/inventory.md#admin-bulk-operations) für [!DNL Inventory Management] in den Konfigurationseinstellungen des Administratorsystems auf **Asynchron** ist. |

{style="table-layout:auto"}

>[!NOTE]
>
>Eine Liste aller Adobe Commerce-Nachrichtenkonsumenten finden Sie unter [Nachrichtenwarteschlangenkonsumenten](https://experienceleague.adobe.com/de/docs/commerce-operations/configuration-guide/message-queues/consumers) im _Konfigurationshandbuch_.

### Konfigurieren von Nachrichtenkonsumenten

Vermeiden Sie mögliche Verarbeitungsprobleme oder -verzögerungen, indem Sie die folgenden Parameter hinzufügen, wenn Sie [die Nachrichten-Consumer starten](#start-message-consumers) für B2B-Funktionen.

- `--max-messages <value>`- Gibt die maximale Anzahl an Nachrichten an, die jeder Consumer vor dem Beenden verarbeiten muss (Standard = 10000). Obwohl Adobe dies nicht empfiehlt, können Sie 0 verwenden, um zu verhindern, dass der Verbraucher beendet. Die Best Practice für eine PHP-Anwendung besteht darin, langwierige Prozesse neu zu starten, um mögliche Speicherlecks zu vermeiden.

- `--batch-size <value>` - Ermöglicht es Ihnen, die von den Verbrauchern verbrauchten Systemressourcen (CPU, Speicher) zu begrenzen. Die Verwendung kleinerer Batches reduziert die Ressourcennutzung und führt daher zu einer langsameren Verarbeitung.  Wenn angegeben, werden Nachrichten in einer Warteschlange in Batches von jeweils `<value>`. Diese Option gilt nur für den Batch-Verbraucher. Wenn `--batch-size` nicht definiert ist, erhält der Batch-Benutzer alle verfügbaren Nachrichten in einer Warteschlange.

Weitere Informationen zu zusätzlichen Konfigurationsoptionen finden Sie unter [Specific-configuration](https://experienceleague.adobe.com//en/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues?lang=de#specific-configuration).

### Nachrichtenkonsumenten starten

Um asynchrone Vorgänge für B2B-Funktionen zu aktivieren, müssen Sie mehrere Nachrichten-Consumer starten.

1. Auflisten der verfügbaren Nachrichtenbenutzer:

   ```bash
   bin/magento queue:consumers:list
   ```

   Der Befehl gibt verfügbare Nachrichtenverbraucher zurück, einschließlich aller [B2B-Nachrichtenverbraucher](#message-consumers).

1. Jeden Verbraucher separat starten:

   ```bash
   bin/magento queue:consumers:start [--max-messages=<value>] [--batch-size=<value>] <consumer_name>
   ```

   Beispiel:

   ```bash
   bin/magento queue:consumers:start quoteItemCleaner
   ```

>[!TIP]
>
>Um sie im Hintergrund auszuführen, hängen Sie `&` an den Befehl an, kehren zu einer Eingabeaufforderung zurück und führen Sie die Befehle weiter aus. Beispiel: `bin/magento queue:consumers:start sharedCatalogUpdatePrice &`.

Weitere Informationen finden Sie unter [Verwalten von Nachrichtenwarteschlangen](https://experienceleague.adobe.com/de/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues) im _Konfigurationshandbuch_.

### Hinzufügen von Nachrichtenkonsumenten zu Cron

Sie können den Ausführungsplan für die `SharedCatalogUpdateCategoryPermissions`- und `SharedCatalogUpdatePrice` automatisieren, indem Sie den Zeitplan zur Cron-Konfigurationsdatei [/app/code/Magento/MessageQueue/etc/crontab.xml](https://experienceleague.adobe.com/de/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues#process-management) hinzufügen.

```
* * * * * ps ax | grep [s]haredCatalogUpdateCategoryPermissions >>/dev/null 2>&1 || nohup php /var/www/html/magento2/bin/magento queue:consumers:start sharedCatalogUpdateCategoryPermissions &
* * * * * ps ax | grep [s]haredCatalogUpdatePrice >>/dev/null 2>&1 || nohup php /var/www/html/magento2/bin/magento queue:consumers:start sharedCatalogUpdatePrice &
```

Sie können Zeitpläne für Nachrichtenbenutzer auch über die [Store-Konfigurationseinstellungen](../systems/cron.md) im Admin-Bereich konfigurieren.

## Aktivieren von B2B-Funktionen in Admin

Nach der Installation der Adobe Commerce B2B-Erweiterung und dem Start der Nachrichtenbenutzer müssen Sie auch [B2B-Funktionen in Admin aktivieren](enable-basic-features.md).

