---
title: Einrichtung des Versandnetzbetreibers
description: Erfahren Sie mehr über die Unterstützung für kommerzielle Versandkonten, die für Ihr Geschäft verfügbar sind.
exl-id: b6098068-12f3-4223-b216-98055a802b19
feature: Shipping/Delivery
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '351'
ht-degree: 0%

---

# Einrichtung des Versandnetzbetreibers

Wenn Sie über ein kommerzielles Konto mit einem unterstützten Netzbetreiber verfügen, können Sie Ihren Kunden den Komfort bieten, diesen Netzbetreiber beim Checkout auszuwählen. Die Preise werden automatisch heruntergeladen, sodass Sie nicht nachschlagen müssen.

>[!NOTE]
>
>Siehe [Commerce Marketplace](../getting-started/commerce-marketplace.md) für zusätzliche Versanddienstleistungen für Ihre Commerce-Installation.

Bevor Sie Ihren Kunden eine Auswahl an Versandunternehmen anbieten können, müssen Sie die folgenden Schritte ausführen:

- Konfigurieren Sie die [Versandeinstellungen](shipping-settings.md) um den Herkunftsort für Ihr Geschäft zu bestimmen.

- Konfigurieren Sie die Einstellungen für jeden Provider-Dienst, den Sie anbieten möchten.

   - [**UPS**](ups.md)  - United Parcel Service (UPS) bietet inländische und internationale Seeverkehrsdienstleistungen auf dem Land- und Luftweg in über 220 Ländern an.
   - [**USPS**](usps.md) - Der US-Postdienst (USPS) ist der unabhängige Postdienst der US-Regierung. USPS bietet inländische und internationale Schifffahrtsdienste auf dem Land- und Luftweg an.
   - [**FedEx**](fedex.md) - FedEx bietet inländische und internationale Schifffahrtsdienste auf dem Land- und Luftweg in mehr als 220 Ländern an.
   - [**DHL**](dhl.md) - DHL bietet integrierte internationale Dienstleistungen und maßgeschneiderte, kundenorientierte Lösungen für die Verwaltung und den Transport von Briefen, Gütern und Informationen.

## Dimensionsgewicht

Das Dimensionsgewicht, manchmal auch als volumetrisches Gewicht bezeichnet, ist eine gängige Branchenpraxis, bei der der Transportpreis auf einer Kombination aus Gewicht und Paketvolumen basiert. Einfach ausgedrückt bestimmt das Dimensionsgewicht die Versandrate anhand des Raumes, den ein Paket im Ladebereich des Frachtführers belegt. Die Dimensionsgewichtung wird in der Regel verwendet, wenn ein Paket im Vergleich zu seinem Volumen relativ leicht ist.

Alle wichtigen Transportunternehmen wenden bei einigen Sendungen Maßgewicht an. Die Art und Weise, in der die dimensionalen Gewichtspreise angewandt werden, variiert jedoch von einem Träger zum anderen. Wenn Ihr Unternehmen ein hohes Versandvolumen hat, kann selbst ein kleiner Unterschied beim Versandpreis im Laufe eines Jahres Tausende von Dollar übersetzen.

## Konfiguration

Die Konfigurationsoptionen variieren für jeden Anbieter. Für alle sind jedoch die folgenden Schritte erforderlich:

1. Öffnen Sie ein Versandkonto mit dem Beförderer.

1. Geben Sie Ihre Kontonummer oder Benutzer-ID und die Gateway-URL zu ihrem System in die Konfiguration Ihres Stores ein.
