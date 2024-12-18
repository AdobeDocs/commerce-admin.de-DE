---
title: Adobe Commerce B2B-abwärtsinkompatible Änderungen
description: Erfahren Sie mehr über Änderungen in Adobe Commerce B2B-Versionen, die möglicherweise eine Aktualisierung Ihres benutzerdefinierten Codes erfordern.
exl-id: 79b66843-3f34-4fe9-9670-53d19b749eb4
source-git-commit: 29663b8a88abc581b9543621ddb475f7d7903027
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 0%

---

# Adobe Commerce B2B-abwärtsinkompatible Änderungen

Überprüfen Sie die allgemeinen Referenzinformationen für alle abwärtsinkompatiblen Änderungen in B2B für Adobe Commerce-Versionen. Im Abschnitt mit den Highlights finden Sie inkompatible Änderungen, die erhebliche Auswirkungen haben und detaillierte Erläuterungen und spezielle Anweisungen erfordern.

## Highlights

### 1.4.2 bis 1.5.0

Durch das Hinzufügen der Zuweisung für mehrere Unternehmen können Firmenbenutzerkonten jetzt mehrere `company_id` aufweisen. Die `Magento\Company\Api\Data\CompanyCustomerInterface` wurde aktualisiert, um die `company_id` für einen Benutzer festzulegen. Als Standard wird das erste Unternehmen festgelegt, das dem Firmenbenutzerkonto zugewiesen ist.

Beim Upgrade von einer früheren Version empfiehlt Adobe, die folgenden Methoden in Klassen zu implementieren, die die -`Magento\Company\Api\Data\CompanyCustomerInterface` verwenden.

- Magento\Company\Api\Data\CompanyCustomerInterface::getIsDefault
- Magento\Company\Api\Data\CompanyCustomerInterface::setIsDefault

## Verweis

{{$include /help/_includes/backward-incompatible-changes/1.4.2-1.5.0.md}}

{{$include /help/_includes/backward-incompatible-changes/1.4.1-1.4.2.md}}

{{$include /help/_includes/backward-incompatible-changes/1.4.0-1.4.1.md}}

{{$include /help/_includes/backward-incompatible-changes/1.3.5-1.4.0.md}}

{{$include /help/_includes/backward-incompatible-changes/1.3.4-1.3.5.md}}

{{$include /help/_includes/backward-incompatible-changes/1.3.3-1.3.4.md}}
