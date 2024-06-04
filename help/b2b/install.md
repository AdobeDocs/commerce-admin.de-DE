---
title: Installieren Sie die [!DNL Adobe Commerce B2B] Erweiterung
description: Erfahren Sie, wie Sie die [!DNL Adobe Commerce B2B] Metapaket.
feature: B2B, Install
role: Admin, Developer
exl-id: a6947212-1708-40ae-9e81-874467eba5e1
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '873'
ht-degree: 0%

---


# Installieren Sie die [!DNL Adobe Commerce B2B] Erweiterung

Die Adobe Commerce B2B-Erweiterung ist nur für Adobe Commerce v2.2.0 oder höher verfügbar. Es wird nach der Installation von Adobe Commerce installiert.

Installieren Sie die neueste Version der B2B-Erweiterung, die von der bereitgestellten Adobe Commerce-Version unterstützt wird.

>[!NOTE]
>
>Diese Installationsanweisungen gelten für Adobe Commerce, das vor Ort eingesetzt wird. Informationen zum Installieren der B2B-Erweiterung für Commerce-Projekte, die in der Cloud-Infrastruktur bereitgestellt werden, finden Sie in der [Commerce Cloud Infrastructure Guide](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure-store/b2b-module.html).

## Voraussetzungen

- Adobe Commerce-Version 2.3.x oder höher
- [Unterstützte Version der B2B-Erweiterung](https://experienceleague.adobe.com/docs/commerce-operations/release/product-availability.html#compatibility)
- Gültig [Authentifizierungsschlüssel](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/authentication-keys.html) , um Adobe Commerce-Erweiterungen herunterzuladen.

  Speichern Sie Authentifizierungsschlüssel für die Installation, indem Sie sie global in Ihrer [COMPOSER_HOME](https://getcomposer.org/doc/03-cli.md#composer-home) Verzeichnis. Oder speichern Sie sie in einem [auth.json](https://developer.adobe.com/commerce/contributor/guides/install/clone-repository/#authentication-file) im Stammverzeichnis der Adobe Commerce-Anwendung.

Prüfen Sie vor der Installation oder Aktualisierung der B2B-Erweiterung die Versionshinweise auf die aktuellsten Informationen zur Versionskompatibilität, zu Aktualisierungen oder Änderungen, die sich auf die Installations- oder Aktualisierungsanforderungen auswirken können.

- [B2B-Versionshinweise](release-notes.md)
- [Versionshinweise zu Adobe Commerce](https://experienceleague.adobe.com/docs/commerce-operations/release/versions.html?lang=en)

## Installationsschritte

1. Aktualisieren Sie im Stammordner der Adobe Commerce-Anwendung das `composer.json` Hinzufügen der Abhängigkeiten für die B2B-Erweiterung:

   ```bash
   composer require magento/extension-b2b:<version>
   ```

   Wenn beispielsweise ein Fehler auftritt:

   ```terminal
   [InvalidArgumentException] Could not find a matching version of package magento/extension-b2b.
   ```

   Überprüfen Sie die Rechtschreibung des Pakets, Ihre Versionsbeschränkung und ob das Paket verfügbar ist und mit Ihrer Mindestanforderung an die Stabilität (stabil) übereinstimmt.

1. Geben Sie bei entsprechender Aufforderung Ihren [Authentifizierungsschlüssel](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/authentication-keys.html).

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

Konfigurieren und starten Sie nach Abschluss der Installation die Nachricht, einschließlich [Festlegen von Parametern für Nachrichtenverbraucher](#configure-message-consumers).

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
| `inventoryQtyCounter` | Korrigiert den Aktienindex asynchron, nachdem eine Bestellung platziert oder ein Produkt entfernt wurde. Erforderlich, wenn die [**[!UICONTROL Use deferred stock update]**](../configuration-reference/catalog/inventory.md#product-stock-options) in den Admin-Konfigurationseinstellungen für Inventory management aktiviert ist. Siehe [Best Practices für die Leistung](https://experienceleague.adobe.com/docs/commerce-operations/performance-best-practices/configuration.html#deferred-stock-update). |
| `async.operations.all` | Erstellt Nachrichten für jede einzelne Aufgabe eines [Massenvorgang](https://developer.adobe.com/commerce/php/development/components/message-queues/bulk-operations/), wie z. B. die Ein- oder Ausfuhr von Waren, die Änderung der Preise in großem Maßstab und die Zuteilung von Erzeugnissen an ein Lager. Erforderlich, wenn die [**Massenvorgänge für Administratoren**](../configuration-reference/catalog/inventory.md#admin-bulk-operations) -Option für [!DNL Inventory Management] auf **Asynchron ausführen** in den Konfigurationseinstellungen des Admin-Systems. |

{style="table-layout:auto"}

>[!NOTE]
>
>Eine Liste aller Adobe Commerce-Nachrichtenverbraucher finden Sie unter [Verbraucher in der Nachrichtenwarteschlange](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/message-queues/consumers.html) im _Konfigurationshandbuch_.

### Konfigurieren von Nachrichtenbenutzern

Vermeiden Sie mögliche Verarbeitungsprobleme oder -verzögerungen durch Hinzufügen der folgenden Parameter, wenn Sie [Starten der Nachricht für den Verbraucher](#start-message-consumers) für B2B-Funktionen.

- `--max-messages <value>`— Gibt die maximale Anzahl von Nachrichten an, die jeder Verbraucher vor dem Beenden verarbeiten muss (Standard = 10000). Obwohl wir es nicht empfehlen, können Sie 0 verwenden, um zu verhindern, dass der Verbraucher beendet wird. Die Best Practice für eine PHP-Anwendung besteht darin, langwierige Prozesse neu zu starten, um mögliche Speicherlecks zu vermeiden.

- `--batch-size <value>`— Ermöglicht Ihnen, die von den Verbrauchern verbrauchten Systemressourcen zu beschränken (CPU, Speicher). Die Verwendung kleinerer Batches verringert die Ressourcenbelegung und führt so zu einer langsameren Verarbeitung.  Wenn dies angegeben ist, werden Nachrichten in einer Warteschlange in Stapeln von `<value>` jedes. Diese Option gilt nur für den Batch-Benutzer. Wenn `--batch-size` nicht definiert ist, empfängt der Batch-Benutzer alle verfügbaren Nachrichten in einer Warteschlange.

Weitere Informationen zu zusätzlichen Konfigurationsoptionen finden Sie unter [Specific-configuration](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues.html#specific-configuration).

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

Weitere Informationen finden Sie unter [Verwalten von Nachrichtenwarteschlangen](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues.html) im _Konfigurationshandbuch_.

### Hinzufügen von Nachrichtenkonsumenten zu Cron

Sie haben die Möglichkeit, den Ausführungszeitplan für die `SharedCatalogUpdateCategoryPermissions` und `SharedCatalogUpdatePrice` Nachrichten für Verbraucher durch Hinzufügen des Zeitplans zur Cron-Konfigurationsdatei [/app/code/Magento/MessageQueue/etc/crontab.xml](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues.html#process-management).

```terminal
* * * * * ps ax | grep [s]haredCatalogUpdateCategoryPermissions >>/dev/null 2>&1 || nohup php /var/www/html/magento2/bin/magento queue:consumers:start sharedCatalogUpdateCategoryPermissions &
* * * * * ps ax | grep [s]haredCatalogUpdatePrice >>/dev/null 2>&1 || nohup php /var/www/html/magento2/bin/magento queue:consumers:start sharedCatalogUpdatePrice &
```

Sie können Zeitpläne für Nachrichtenverbraucher auch über die [Konfigurationseinstellungen speichern](../systems/cron.md) im Admin.

## B2B-Funktionen in Admin aktivieren

Nach der Installation der Adobe Commerce-B2B-Erweiterung und dem Starten von Nachrichtenempfängern müssen Sie außerdem [B2B-Funktionen in Admin aktivieren](enable-basic-features.md).
