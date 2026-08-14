---
title: Handbuch zu [!DNL Inventory Management]
description: Admin- und CLI-Handbuch für  [!DNL Inventory Management] , Quellen, Mengen, Konfiguration, Bestellungen und Lieferungen in Adobe Commerce und Magento Open Source.
seo-title: Adobe Commerce Inventory Management Guide
seo-description: Describes how to use the [!DNL Inventory Management] module in Adobe Commerce or Magento Open Source.
exl-id: 8013bc13-b057-4ad7-bbed-ee00c2f6e4eb
TQID: https://experienceleague.adobe.com/AFaKjUXrfZOMSYWjcW-dyD9OBMlQj6PkILIQiuT8YJU
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
  - id: e8818fe6-9c8b-4bc0-9ef8-377a10b7bc75
  - id: f42e0a1a-0d79-488d-a83f-f2c30672b137
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 94e419120b8e16848cc1d449650f023f361a2af7
workflow-type: tm+mt
source-wordcount: 329
ht-degree: 1%

---

# Übersicht über [!DNL Inventory Management]

Dieses Handbuch richtet sich an Admins, die Lagerbestände an mehreren Standorten in Adobe Commerce und Magento Open Source verwalten. Es stellt Konfigurations- und Verwaltungsverfahren für das [!DNL Inventory Management] bereit und setzt ein grundlegendes Verständnis der [!DNL Commerce] voraus.

Verwenden Sie **Admin** für Konfigurations-, Reporting- und tägliche Inventaraufgaben. Verwenden Sie die **Befehlszeilenschnittstelle** für Installation, Upgrades und Backend-Konfiguration.

Dieses Handbuch behandelt Folgendes:

| Subjekt | Beschreibung |
| ------- | ----------- |
| [Einführung](introduction.md) | Funktionen, Terminologie und die passende [!DNL Inventory Management] für Ihren Store. |
| [Versionshinweise](release-notes.md) | Versionsverlauf des Moduls und bekannte Probleme. |
| [Grundlagen zum Inventar](sources-stocks.md) | Konzepte für [Lager und Quellen](sources-stocks.md), [Quellauswahl und &#x200B;](selection-reservations.md), [Bestell- und &#x200B;](order-status.md) und [Produkttypen](product-types.md). |
| Erste Schritte | [Commerce](migrate.md)-Upgrades[&#x200B; (Installation und &#x200B;](install-update.md)), [Merchant-Sourcing-](merchant-sourcing.md) und [Inventarumstrukturierung](expand-restructure.md). |
| [Konfiguration](configuration.md) | Globale, Produkt- und Algorithmuseinstellungen für Anzeige und Versand in der Storefront. |
| [Quellen verwalten](sources-manage.md) | Erstellen und Verwalten von Orten für die Erfüllung |
| [Verwalten von Lagerbeständen](stocks-manage.md) | Zuordnen von Quellen zu Vertriebskanälen. |
| [Mengen verwalten](quantities-manage.md) | Zuweisen und Aktualisieren von Produktmengen pro Quelle. |
| [Bestellungen und Sendungen verwalten](shipments.md) | Bestellungen ausführen und Lieferungen aus dem Bestand verwalten. |
| [CLI-Referenz](cli.md) | Befehlszeileninventar- und Konfigurationsaufgaben. |

{style="table-layout:auto"}

## Entwicklerinformationen

Zugriff auf erweiterte Ressourcen für APIs, Anpassung und Modularchitektur. Technische Details zu APIs und zur Anpassung von Algorithmen finden Sie unter [[!DNL Inventory Management]](https://developer.adobe.com/commerce/webapi/rest/inventory/) in der Entwicklerdokumentation zur REST-API .

## Dokumentation zu Commerce

Hier finden Sie Händler-, Cloud- und Entwicklerhandbücher, die Ihnen bei allen Aspekten von Adobe Commerce helfen. Verwenden Sie diese Ressourcen für alle Einrichtungs- oder Verwaltungsanforderungen.

{{docs-links}}

## Fehlerbehebung und Support

Verwenden Sie Support-Artikel und Ticketsysteme, um Inventarprobleme schnell zu lösen. Erhalten Sie zusätzliche Hilfe für den Lagerstatus oder die Produktverwaltung.

Wenn Sie Informationen benötigen oder Fragen haben, die in diesem Handbuch nicht behandelt werden, verwenden Sie die folgenden Ressourcen:

- [Lagerstatus nach der Bestandsinstallation falsch](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/miscellaneous/stock-status-incorrect-after-magento-inventory-install.html?lang=de)
- [Support-](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide.html?lang=de#submit-ticket): Senden Sie ein Ticket, um zusätzliche Hilfe zu erhalten.
