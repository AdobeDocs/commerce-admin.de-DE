---
title: Einrichtung des Spediteurs
description: Erfahren Sie mehr über den Support für kommerzielle Versandkonten, der für Ihren Shop verfügbar ist.
exl-id: b6098068-12f3-4223-b216-98055a802b19
feature: Shipping/Delivery
source-git-commit: 15118877bb8cc533b2323819db34da0513899e25
workflow-type: tm+mt
source-wordcount: '466'
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

Am 25. Januar 2026 stellt USPS die veralteten Web Tools-APIs ein. Nach diesem Datum schlagen alle Anfragen an die Web-Tools-APIs fehl.

Um eine Unterbrechung der USPS-Versandservices zu vermeiden, führen Sie die folgenden Maßnahmen vor dem 25. Januar 2026 durch:

- Wenden Sie den [USPS REST API Migration Quality Patch](https://experienceleague.adobe.com/de/docs/commerce-operations/tools/quality-patches-tool/patches-available-in-qpt/v1-1-70/ac-15210) an, um Unterstützung für die Integration mit den USPS REST-APIs hinzuzufügen.

- Aktualisieren Sie die Commerce USPS-Konfiguration zur Verwendung der REST-APIs:

   - [USPS Spediteurkonfiguration](usps.md)

   - [Konfiguration der Versandkennzeichnung](shipping-label-create.md)

