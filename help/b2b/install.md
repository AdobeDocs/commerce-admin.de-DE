---
title: Installieren Sie die [!DNL Adobe Commerce B2B] Erweiterung
description: Erfahren Sie, wie Sie die [!DNL Adobe Commerce B2B] Metapaket.
feature: B2B, Install
role: Admin, Developer
exl-id: a6947212-1708-40ae-9e81-874467eba5e1
source-git-commit: be36742aa1214e7e8e7f343051336cd3635099f4
workflow-type: tm+mt
source-wordcount: '1086'
ht-degree: 0%

---


# Installieren Sie die [!DNL Adobe Commerce B2B] Erweiterung

Die Adobe Commerce B2B-Erweiterung, `magento/extension-b2b` ist für alle unterstützten Versionen von Adobe Commerce verfügbar. Es wird nach der Installation von Adobe Commerce installiert.


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

- Zugriff auf [repo.magento.com](https://repo.magento.com/) , um die Erweiterung herunterzuladen. Informationen zur Schlüsselgenerierung und zum Erhalt der erforderlichen Berechtigungen finden Sie unter [Abrufen der Authentifizierungsschlüssel](https://experienceleague.adobe.com/en/docs/commerce-operations/installation-guide/prerequisites/authentication-keys).

  Speichern Sie Authentifizierungsschlüssel für die Installation, indem Sie sie global in Ihrer [COMPOSER_HOME](https://getcomposer.org/doc/03-cli.md#composer-home) Verzeichnis. Oder speichern Sie sie in einem [auth.json](https://developer.adobe.com/commerce/contributor/guides/install/clone-repository/#authentication-file) im Stammverzeichnis der Adobe Commerce-Anwendung.

- [Unterstützte Version der B2B-Erweiterung](https://experienceleague.adobe.com/en/docs/commerce-operations/release/product-availability)-Bestimmen Sie die neueste Version der B2B-Erweiterung, die von der bereitgestellten Adobe Commerce-Version unterstützt wird.

- In den Versionshinweisen finden Sie die aktuellen Informationen zur Versionskompatibilität, zu Aktualisierungen oder Änderungen, die sich auf die Installations- oder Aktualisierungsanforderungen auswirken können.

   - [B2B-Versionshinweise](release-notes.md)
   - [Versionshinweise zu Adobe Commerce](https://experienceleague.adobe.com/en/docs/commerce-operations/release/versions)

>[!ENDSHADEBOX]

Installieren Sie die B2B-Erweiterung (`magento/b2b-extension`) mithilfe von Composer. Die Erweiterung ist ein Composer-Metapaket, das die Sammlung von Modulen enthält, die die B2B-Funktionen für eine Adobe Commerce-Instanz aktivieren. Eine Liste der enthaltenen Module finden Sie unter [B2B-Pakete](packages.md).

>[!BEGINTABS]

>[!TAB Cloud-Infrastruktur]

>[!TIP]
>
>Bei der Installation von Adobe Commerce B2B in der Cloud-Infrastruktur empfiehlt Adobe, dass Sie Ihre Adobe Commerce-Anwendung vor dem Beginn in einer Integrations- oder Staging-Umgebung bereitstellen.

Adobe empfiehlt, in einer Entwicklungsverzweigung zu arbeiten, wenn Sie die B2B-Erweiterung zu Ihrem Projekt hinzufügen. Wenn Sie keine Verzweigung haben, lesen Sie [Erstellen einer Verzweigung für die Entwicklung](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/cli-branches). Bei der Installation der B2B-Erweiterung muss die Variable `Magento_B2b` Der Erweiterungsname wird automatisch in die `app/etc/config.php` -Datei. Die Datei muss nicht direkt bearbeitet werden.

**Installieren der B2B-Erweiterung**:

1. Wechseln Sie auf Ihrer lokalen Workstation zum Projektverzeichnis.

1. Erstellen oder checken Sie einen Entwicklungszweig aus.

1. Fügen Sie die B2B-Erweiterung zum `require` Abschnitt `composer.json` -Datei.

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
   >Durch das Übermitteln von Aktualisierungen an die Cloud-Umgebung wird der Commerce-Cloud-Bereitstellungsprozess initiiert, um die Änderungen anzuwenden. Überprüfen Sie den Bereitstellungsstatus im [Bereitstellungsprotokoll](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/deploy/process). Wenn Bereitstellungsfehler auftreten, lesen Sie [Wiederherstellen nach Komponentenfehler](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/deploy/recover-failed-deployment).

1. Nachdem der Build und die Bereitstellung abgeschlossen sind, melden Sie sich mit SSH bei der Remote-Umgebung an und überprüfen Sie, ob die B2B-Erweiterung installiert und aktiviert ist.

   ```bash
   bin/magento module:status Magento_B2b
   ```

   Ein Erweiterungsname verwendet das folgende Format: `<VendorName>_<ComponentName>`.

   Beispielantwort:

   ```terminal
   Magento_B2b : Module is enabled
   ```

>[!TAB Vor Ort]

1. Aktualisieren Sie im Stammordner der Adobe Commerce-Anwendung das `composer.json` Hinzufügen der Abhängigkeiten für die B2B-Erweiterung:

   ```bash
   composer require magento/extension-b2b:<version>
   ```

   Wenn beispielsweise ein Fehler auftritt:

   ```terminal
   [InvalidArgumentException] Could not find a matching version of package magento/extension-b2b.
   ```

   Überprüfen Sie die Rechtschreibung des Pakets, Ihre Versionsbeschränkung und ob das Paket verfügbar ist und mit Ihrer Mindestanforderung an die Stabilität (stabil) übereinstimmt.

1. Geben Sie bei entsprechender Aufforderung Ihren [Authentifizierungsschlüssel](https://experienceleague.adobe.com/en/docs/commerce-operations/installation-guide/prerequisites/authentication-keys).

   Ihre _öffentlicher Schlüssel_ ist Ihr Benutzername; Ihr _privater Schlüssel_ ist Ihr Passwort. Wenn Sie Ihre öffentlichen und privaten Schlüssel in `auth.json`festgelegt ist, werden Sie nicht zur Authentifizierung aufgefordert.

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
| `sharedCatalogUpdatePrice` | Aktualisiert den Preis für jedes Produkt in einem freigegebenen Katalog. Erforderlich, wenn die [**[!UICONTROL Shared Catalogs]**](catalog-shared.md) in den Konfigurationseinstellungen des Admin-Systems aktiviert ist. |
| `sharedCatalogUpdateCategoryPermissions` | Aktualisiert Kategorien, die einer freigegebenen Katalogkategorie zugewiesen sind. Erforderlich, wenn die [**[!UICONTROL Shared Catalogs]**](catalog-shared.md) in den Konfigurationseinstellungen des Admin-Systems aktiviert ist. |
| `negotiableQuotePriceUpdate` | Aktualisiert die Preise für verhandelbare Kurse. Erforderlich, wenn die [**[!UICONTROL Quotes]**](quotes.md) in den Konfigurationseinstellungen des Admin-Systems aktiviert ist. |
| `purchaseorder.toorder` | Konvertiert eine Bestellung in eine Bestellung. Erforderlich, wenn die [**[!UICONTROL Purchase Orders]**](purchase-order-flow.md) in den Konfigurationseinstellungen des Admin-Systems aktiviert ist. |
| `purchaseorder.transactional.email` | Senden Sie E-Mails zur Bestellung. Erforderlich, wenn die [**[!UICONTROL Purchase Orders]**](purchase-order-flow.md) in den Konfigurationseinstellungen des Admin-Systems aktiviert ist. |
| `purchaseorder.validation` | Validiert die Bestellung für relevante [Validierungsregeln](account-dashboard-approval-rules.md). Erforderlich, wenn die [**[!UICONTROL Purchase Orders]**](purchase-order-flow.md) in den Konfigurationseinstellungen des Admin-Systems aktiviert ist. |
| `quoteItemCleaner` | Löscht ungültige oder inaktive Preisangebote, wenn ein Produkt aus dem Katalog gelöscht oder aus dem Warenkorb entfernt wird. Erforderlich, wenn die [**[!UICONTROL Quotes]**](quotes.md) in den Konfigurationseinstellungen des Admin-Systems aktiviert ist. |
| `inventoryQtyCounter` | Korrigiert den Aktienindex asynchron, nachdem eine Bestellung platziert oder ein Produkt entfernt wurde. Erforderlich, wenn die [**[!UICONTROL Use deferred stock update]**](../configuration-reference/catalog/inventory.md#product-stock-options) in den Admin-Konfigurationseinstellungen für Inventory management aktiviert ist. Siehe [Best Practices für die Leistung](https://experienceleague.adobe.com/en/docs/commerce-operations/performance-best-practices/configuration#deferred-stock-update). |
| `async.operations.all` | Erstellt Nachrichten für jede einzelne Aufgabe eines [Massenvorgang](https://developer.adobe.com/commerce/php/development/components/message-queues/bulk-operations/) wie die Einfuhr oder Ausfuhr von Waren, die Änderung der Preise in großem Maßstab und die Zuteilung von Erzeugnissen an ein Lager. Erforderlich, wenn die [**Massenvorgänge für Administratoren**](../configuration-reference/catalog/inventory.md#admin-bulk-operations) -Option für [!DNL Inventory Management] auf **Asynchron ausführen** in den Konfigurationseinstellungen des Admin-Systems. |

{style="table-layout:auto"}

>[!NOTE]
>
>Eine Liste aller Adobe Commerce-Nachrichtenverbraucher finden Sie unter [Verbraucher in der Nachrichtenwarteschlange](https://experienceleague.adobe.com/en/docs/commerce-operations/configuration-guide/message-queues/consumers) im _Konfigurationshandbuch_.

### Konfigurieren von Nachrichtenbenutzern

Vermeiden Sie mögliche Verarbeitungsprobleme oder -verzögerungen durch Hinzufügen der folgenden Parameter, wenn Sie [Starten der Nachricht für den Verbraucher](#start-message-consumers) für B2B-Funktionen.

- `--max-messages <value>`— Gibt die maximale Anzahl von Nachrichten an, die jeder Verbraucher vor dem Beenden verarbeiten muss (Standard = 10000). Obwohl Adobe es nicht empfiehlt, können Sie mit 0 verhindern, dass der Verbraucher beendet wird. Die Best Practice für eine PHP-Anwendung besteht darin, langwierige Prozesse neu zu starten, um mögliche Speicherlecks zu vermeiden.

- `--batch-size <value>`— Ermöglicht Ihnen, die von den Verbrauchern verbrauchten Systemressourcen zu beschränken (CPU, Speicher). Die Verwendung kleinerer Batches verringert die Ressourcenbelegung und führt so zu einer langsameren Verarbeitung.  Wenn dies angegeben ist, werden Nachrichten in einer Warteschlange in Stapeln von `<value>` jedes. Diese Option gilt nur für den Batch-Benutzer. Wenn `--batch-size` nicht definiert ist, empfängt der Batch-Benutzer alle verfügbaren Nachrichten in einer Warteschlange.

Weitere Informationen zu zusätzlichen Konfigurationsoptionen finden Sie unter [Specific-configuration](https://experienceleague.adobe.com//en/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues#specific-configuration).

### Starten von Nachrichtenempfängern

Um asynchrone Vorgänge für B2B-Funktionen zu aktivieren, müssen Sie mehrere Nachrichtenverbraucher starten.

1. Geben Sie die verfügbaren E-Mail-Verbraucher an:

   ```bash
   bin/magento queue:consumers:list
   ```

   Der Befehl gibt verfügbare Nachrichtenkunden zurück, einschließlich aller [B2B-Nachrichten-Verbraucher](#message-consumers).

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
>Um sie im Hintergrund auszuführen, hängen Sie `&` zum Befehl wechseln, zu einer Eingabeaufforderung zurückkehren und die Ausführung der Befehle fortsetzen. Beispiel: `bin/magento queue:consumers:start sharedCatalogUpdatePrice &`.

Weitere Informationen finden Sie unter [Verwalten von Nachrichtenwarteschlangen](https://experienceleague.adobe.com/en/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues) im _Konfigurationshandbuch_.

### Hinzufügen von Nachrichtenkonsumenten zu Cron

Sie können den Ausführungszeitplan für die `SharedCatalogUpdateCategoryPermissions` und `SharedCatalogUpdatePrice` Nachrichten für Verbraucher durch Hinzufügen des Zeitplans zur Cron-Konfigurationsdatei [/app/code/Magento/MessageQueue/etc/crontab.xml](https://experienceleague.adobe.com/en/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues#process-management).

```terminal
* * * * * ps ax | grep [s]haredCatalogUpdateCategoryPermissions >>/dev/null 2>&1 || nohup php /var/www/html/magento2/bin/magento queue:consumers:start sharedCatalogUpdateCategoryPermissions &
* * * * * ps ax | grep [s]haredCatalogUpdatePrice >>/dev/null 2>&1 || nohup php /var/www/html/magento2/bin/magento queue:consumers:start sharedCatalogUpdatePrice &
```

Sie können Zeitpläne für Nachrichtenverbraucher auch über die [Konfigurationseinstellungen speichern](../systems/cron.md) im Admin.

## B2B-Funktionen in Admin aktivieren

Nach der Installation der Adobe Commerce-B2B-Erweiterung und dem Starten von Nachrichtenempfängern müssen Sie außerdem [B2B-Funktionen in Admin aktivieren](enable-basic-features.md).

