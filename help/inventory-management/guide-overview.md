---
title: Handbuch  [!DNL Inventory Management]  Inventory management
description: Umfassende Informationen zu  [!DNL Inventory Management]  für Adobe Commerce- und Magento Open Source-Administratoren, einschließlich Migration und Konfiguration.
seo-title: Adobe Commerce Inventory Management Guide
seo-description: Describes how to use the [!DNL Inventory Management] module in Adobe Commerce or Magento Open Source.
exl-id: 8013bc13-b057-4ad7-bbed-ee00c2f6e4eb
source-git-commit: f8254db7d69e58c8e9a78948ee6e40f5ea88cea0
workflow-type: tm+mt
source-wordcount: '356'
ht-degree: 0%

---

# [!DNL Inventory Management]

Dieses Handbuch richtet sich an Administratoren von Adobe Commerce und Magento Open Source. Es enthält detaillierte Informationen zur Aktivierung dieses Moduls, einschließlich Konfiguration und Verwaltung seiner Funktionen. Es setzt ein grundlegendes Verständnis der Konfiguration und Funktionalität der [!DNL Commerce] voraus.

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
