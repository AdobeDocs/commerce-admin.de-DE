---
title: Abwärtskompatible Änderungen von Adobe Commerce B2B
description: Erfahren Sie mehr über Änderungen in B2B-Versionen von Adobe Commerce, bei denen Sie möglicherweise Ihren benutzerdefinierten Code aktualisieren müssen.
exl-id: 79b66843-3f34-4fe9-9670-53d19b749eb4
source-git-commit: 29663b8a88abc581b9543621ddb475f7d7903027
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 0%

---

# Abwärtskompatible Änderungen von Adobe Commerce B2B

Überprüfen Sie die allgemeinen Referenzinformationen für alle abwärtsinkompatiblen Änderungen in B2B für Adobe Commerce-Versionen. Im Abschnitt Highlights finden Sie inkompatible Änderungen, die erhebliche Auswirkungen haben und eine detaillierte Erläuterung und spezielle Anweisungen erfordern.

## Highlights

### 1.4.2 bis 1.5.0

Mit der Hinzufügung der Zuweisung mehrerer Unternehmen können Unternehmensbenutzerkonten jetzt mehrere `company_id` -Werte aufweisen. Die `Magento\Company\Api\Data\CompanyCustomerInterface` wurde aktualisiert, um den Standardwert `company_id` für einen Benutzer festzulegen. Die Standardeinstellung ist das erste Unternehmen, das dem Unternehmensbenutzerkonto zugewiesen ist.

Wenn Sie von einer früheren Version aktualisieren, empfiehlt Adobe die Implementierung der folgenden Methoden in Klassen, die die `Magento\Company\Api\Data\CompanyCustomerInterface` verwenden.

- Magento\Company\Api\Data\CompanyCustomerInterface::getIsDefault
- Magento\Company\Api\Data\CompanyCustomerInterface::setIsDefault

## Referenz

{{$include /help/_includes/backward-incompatible-changes/1.4.2-1.5.0.md}}

{{$include /help/_includes/backward-incompatible-changes/1.4.1-1.4.2.md}}

{{$include /help/_includes/backward-incompatible-changes/1.4.0-1.4.1.md}}

{{$include /help/_includes/backward-incompatible-changes/1.3.5-1.4.0.md}}

{{$include /help/_includes/backward-incompatible-changes/1.3.4-1.3.5.md}}

{{$include /help/_includes/backward-incompatible-changes/1.3.3-1.3.4.md}}
