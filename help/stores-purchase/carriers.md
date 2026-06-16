---
title: Einrichtung des Spediteurs
description: Erfahren Sie mehr über den Support für kommerzielle Versandkonten, der für Ihren Shop verfügbar ist.
exl-id: b6098068-12f3-4223-b216-98055a802b19
feature: Shipping/Delivery
TQID: https://experienceleague.adobe.com/zKN3BQWHywAOLJ-zaJX1-8b7aAYxtzl8v9J7uJG1rFg
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 496
ht-degree: 0%

---

# Einrichtung des Spediteurs

Wenn Sie über ein kommerzielles Konto bei einem unterstützten Carrier verfügen, können Sie Ihren Kunden die Bequemlichkeit bieten, diesen Carrier während des Checkouts auszuwählen. Die Tarife werden automatisch heruntergeladen, sodass Sie die Informationen nicht nachschlagen müssen.

>[!NOTE]
>
>Siehe [Commerce Marketplace](../getting-started/commerce-marketplace.md) für zusätzliche Versandservices für Ihre Commerce-Installation.

Bevor Sie Ihren Kunden eine Auswahl an Versandunternehmen anbieten können, müssen Sie die folgenden Schritte ausführen:

- Konfigurieren Sie die [Versandeinstellungen](shipping-settings.md), um den Ausgangspunkt für Ihr Geschäft festzulegen.

- Konfigurieren Sie die Einstellungen für jeden Provider-Dienst, den Sie anbieten möchten.

   - [**UPS**](ups.md) - United Parcel Service (UPS) bietet inländische und internationale Verschiffen auf dem Land- und Luftweg in mehr als 220 Länder an.
   - [**USPS**](usps.md) - Der United States Postal Service (USPS) ist der unabhängige Postdienst der US-Regierung. USPS bietet inländische und internationale Schifffahrtsdienstleistungen auf dem Land- und Luftweg an.
   - [**FedEx**](fedex.md) - FedEx bietet inländische und internationale Schifffahrtsdienstleistungen auf dem Land- und Luftweg in mehr als 220 Länder an.
   - [**DHL**](dhl.md) - DHL bietet integrierte internationale Dienstleistungen und maßgeschneiderte, kundenorientierte Lösungen für die Verwaltung und den Transport von Briefen, Waren und Informationen.

## Dimensionsgewicht

Das dimensionale Gewicht, manchmal auch als Volumengewicht bezeichnet, ist eine gängige Praxis in der Branche, die den Transportpreis auf einer Kombination von Gewicht und Verpackungsvolumen basiert. Einfach ausgedrückt, bestimmt das Maßgewicht die Versandrate anhand des Raumes, den ein Paket im Frachtbereich des Frachtführers einnimmt. Das dimensionale Gewicht wird in der Regel verwendet, wenn eine Verpackung im Vergleich zu ihrem Volumen relativ leicht ist.

Alle großen Spediteure wenden auf einige Sendungen ein dimensionales Gewicht an. Die Art und Weise, wie die Preisgestaltung nach der Dimensionierung der Gewichtung angewandt wird, ist jedoch von einem Anbieter zum anderen unterschiedlich. Wenn Ihr Unternehmen ein hohes Versandvolumen hat, kann selbst ein leichter Unterschied im Versandpreis im Laufe eines Jahres zu Tausenden von Dollar führen.

## Konfiguration

Die Konfigurationsoptionen variieren für jeden Provider. Alle erfordern jedoch die folgenden Schritte:

1. Öffnen Sie ein Versandkonto beim Spediteur.

1. Geben Sie Ihre Kontonummer oder Benutzer-ID und die Gateway-URL zu ihrem System in die Konfiguration Ihres Stores ein.

### Einstellung der USPS Web Tools-API

Die Adobe Commerce-Versionen 2.4.6, 2.4.7 und 2.4.8 verwenden die Legacy-Web-Tools-APIs für die vordefinierte Versandintegration mit USPS. USPS hat USPS APIs eingeführt, eine REST-basierte Plattform, die die veralteten Web-Tools-APIs ersetzt.

Seit dem 25. Januar 2026 hat USPS die Legacy-Webtools-APIs eingestellt. Nach diesem Datum schlagen alle Anfragen an die Web-Tools-APIs fehl.

Um Unterbrechungen des USPS-Versands zu vermeiden, aktualisieren Sie auf die neueste Version von Adobe Commerce oder führen Sie die folgenden Schritte aus:

- Wenden Sie den [USPS REST API Migration Quality Patch](https://experienceleague.adobe.com/de/docs/commerce-operations/tools/quality-patches-tool/patches-available-in-qpt/v1-1-70/ac-15210) an, um Unterstützung für die Integration mit den USPS REST-APIs hinzuzufügen.

- Aktualisieren Sie die Commerce USPS-Konfiguration zur Verwendung der REST-APIs:

   - [USPS Spediteurkonfiguration](usps.md)

   - [Konfiguration der Versandkennzeichnung](shipping-label-create.md)

