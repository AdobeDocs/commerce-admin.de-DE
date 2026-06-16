---
title: Handbuch  [!DNL Inventory Management]  Inventory management
description: Umfassende Informationen zu  [!DNL Inventory Management]  für Adobe Commerce- und Magento Open Source-Administratoren, einschließlich Migration und Konfiguration.
seo-title: Adobe Commerce Inventory Management Guide
seo-description: Describes how to use the [!DNL Inventory Management] module in Adobe Commerce or Magento Open Source.
exl-id: 8013bc13-b057-4ad7-bbed-ee00c2f6e4eb
TQID: https://experienceleague.adobe.com/AFaKjUXrfZOMSYWjcW-dyD9OBMlQj6PkILIQiuT8YJU
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: c1256247-af4b-46d8-9dca-0c654ecfa157id: d1e21356-0064-4f48-9089-16e3f0dbd2a6id: dac87252-6066-4d6e-a9d2-f6d84c323de7id: e8818fe6-9c8b-4bc0-9ef8-377a10b7bc75id: f42e0a1a-0d79-488d-a83f-f2c30672b137
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: c1579802-ddd4-4214-8a91-97b2066abe11id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 394
ht-degree: 0%

---

# [!DNL Inventory Management]

Dieses Handbuch richtet sich an Administratoren, die in Adobe Commerce und Magento Open Source Admin arbeiten. Es enthält detaillierte Informationen zur Aktivierung dieses Moduls, einschließlich Konfiguration und Verwaltung seiner Funktionen. Es setzt ein grundlegendes Verständnis der Konfiguration und Funktionalität der [!DNL Commerce] voraus.

[!DNL Inventory Management] gibt es zwei Bereiche für Administratoren:

- Der Administrator: Verwenden Sie diesen Bereich, um auf die Konfigurations-Benutzeroberfläche und Berichte zuzugreifen.
- Die Befehlszeilenschnittstelle: Verwenden Sie dieses Tool, um Installations- und Backend-Konfigurationsaufgaben auszuführen.

Dieses Handbuch behandelt Folgendes:

| Subjekt | Beschreibung |
| ------- | ----------- |
| [Einführung](introduction.md) | Überblick über die [!DNL Inventory Management] Funktionen, mit denen Sie Lagerbestände an mehreren Orten verwalten können, sodass Ihr Commerce-Store den physischen Bestand genau widerspiegelt. |
| [Versionshinweise](release-notes.md) | Informationen zu allen Versionen finden Sie in [!DNL Inventory Management] Versionshinweisen . |
| Grundlagen zum Inventar | Lernen Sie die Grundlagen zur Verwaltung des Inventars kennen: [Lager und Quellen](sources-stocks.md), [Quellenauswahl und ](selection-reservations.md)[, Bestell- und Reservierungsstatus](order-status.md) und [Produkttypen](product-types.md) |
| Erste Schritte | Erfahren Sie mehr über das [!DNL Inventory Management] und wie es in Ihre Commerce-Instanz und Ihre Speichervorgänge passt: [Commerce-Upgrades](migrate.md), [Modulinstallation und -aktualisierung](install-update.md), [Merchant-Sourcing-Typen](merchant-sourcing.md) und [Sourcing-Strukturänderungen](expand-restructure.md) |
| [Konfiguration](configuration.md) | Erfahren Sie mehr über die Konfiguration [!DNL Inventory Management] Optionen, die die Quellverfügbarkeit, Storefront-Produkte und den Bestellversand bestimmen. |
| [Quellen verwalten](sources-manage.md) | Erfahren Sie mehr über Quellen und darüber, wie sie die physischen Orte definieren, an denen der Produktbestand zur Auftragserfüllung verwaltet und versandt wird oder wo Services verfügbar sind. |
| [Verwalten von Lagerbeständen](stocks-manage.md) | Erfahren Sie, wie Stock verwendet wird, um einen virtuellen, aggregierten Bestand von Produkten für Quellen Ihrer Vertriebskanäle darzustellen. |
| [Mengen verwalten](quantities-manage.md) | Erfahren Sie, wie Sie Quellen und Mengen für neue Produkte zuweisen oder vorhandene Produkte ändern. |
| [Bestellungen und Sendungen verwalten](shipments.md) | Erfahren Sie mehr über die zusätzlichen [!DNL Inventory Management] Funktionen und Optionen zur Verwaltung von Lagermengen während des Versandprozesses. |
| [CLI-Referenz](cli.md) | Erfahren Sie mehr über die Befehle, die das Modul [!DNL Inventory Management] zum Verwalten von Inventardaten und Konfigurationseinstellungen bereitstellt. |

{style="table-layout:auto"}

## Entwicklerinformationen

Siehe [[!DNL Inventory Management]](https://developer.adobe.com/commerce/webapi/rest/inventory/) in der Entwicklerdokumentation für Details zur Modularchitektur, zu APIs und zur Algorithmusanpassung.

## Dokumentation zu Commerce

{{docs-links}}

## Fehlerbehebung und Support

Wenn Sie Informationen benötigen oder Fragen haben, die in diesem Handbuch nicht behandelt werden, verwenden Sie die folgenden Ressourcen:

- [Lagerstatus nach der Bestandsinstallation falsch](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/miscellaneous/stock-status-incorrect-after-magento-inventory-install.html)
- [Support-](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide.html#submit-ticket): Senden Sie ein Ticket, um zusätzliche Hilfe zu erhalten.
