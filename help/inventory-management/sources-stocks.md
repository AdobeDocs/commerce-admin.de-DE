---
title: Bestände und Quellen
description: Lernen Sie die Beziehungen zwischen Produkten, Quellen und Lagern kennen.
exl-id: 01bbbd82-898b-4757-ab40-0d8b89ec59bc
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '792'
ht-degree: 0%

---

# Bestände und Quellen

Verwalten Sie Ihr Inventar unabhängig vom Lagerort, vom Produkt- oder Servicetyp oder vom Vertriebskanal. Bestellungen und Versandprodukte aus mehreren Lagern, Ziegeleien- und Mörtelläden, Vertriebszentren und Lieferabfällen zu kompletten Bestellungen mit Schwerpunkt auf ausgeglichenen Lagerbeständen, Versandkosten und mehr.

Diese Beschreibungen umfassen Produkte, Quellen und Lager für ein Fahrradunternehmen mit mehreren Versandstandorten und Websites in den USA und Europa.

## Quellen

[Quellen](sources-manage.md) sind die physischen Orte, an denen das Produktinventar verwaltet und zur Erfüllung der Bestellung versandt wird oder an denen Dienste verfügbar sind. Zu diesen Standorten zählen Lagerhäuser, Bausteine- und Mörtelgeschäfte, Vertriebszentren und Tropfenlieferanten. [!DNL Commerce] verwendet die Mengen und Verkaufsmengen pro Lager und verwaltet die Lagerbestände automatisch für verwaltete Produkte und Bestellungen. Wenn Sie eine Quelle haben, werden Sie im Modus _Einfache Quelle_ berücksichtigt. Wenn Sie mehrere Quellen haben, werden Sie im Modus _mehrere Quellen_ berücksichtigt.

Eine Quelle kann im Lagerbereich eines Lagers Vorrang haben, aber nicht unbedingt in allen Lagern, da die Quelle in verschiedenen Lagern wiederverwendet werden kann. Die Anzahl der Lager und Quellen erhöht die Komplexität bei der Bestimmung des besten Lagers oder Stores, der bzw. der bestellt werden kann. So können Sie z.B. eine begrenzte Anzahl von Produkten von Ihren Ziegeleien und Mörtel-Standorten mit einem umfangreichen Inventar in Ihren Lagern und Dienstleistungen an wichtigen Standorten mit begrenzter Verfügbarkeit haben.

In diesem Beispiel verfügt der Händler über ein Mountainbike, das aus Geschäften, Lagerhäusern und einem Drop Shipper geliefert werden kann.

![Beispielquellendiagramm](assets/diagram-sources.png){width="600" zoomable="yes"}

## Lagerbestände

[Stocks](stocks-manage.md) stellen einen virtuellen, aggregierten Bestand von Produkten dar, die für Ihre Vertriebskanäle (Websites) zum Verkauf angeboten werden. Jedes Lager ordnet Ihre Verkaufskanäle mit Quellen für verfügbare Lagerbestände und Verkaufsmengen zu. Abhängig von Ihrer Site-Konfiguration kann das Lager einem oder mehreren Vertriebskanälen und -quellen zugewiesen werden.

Sales Channel stellen Entitäten dar, die Ihren Bestand verkaufen, einschließlich Websites, Storeansichten, B2B-Kundengruppen usw. Verkaufskanäle können nur einem Lager zugeordnet werden. Jedem Vertriebskanal kann nur ein einziges Lager zugewiesen werden, und ein einzelnes Lager kann mehreren Websites zugewiesen werden. Über das Lager können Sie die Priorisierung der beim Versand von Bestellungen verwendeten Quellen sowie durch den [Source-Auswahlalgorithmus](selection-reservations.md) ändern.

Beginnen Sie mit einem Standardbestand, der mit der standardmäßigen Source und Ihrer Website zugewiesen ist, die am besten von Einzelquellenhändlern verwendet werden. Diesem Lager kann nur die Standard-Source zugewiesen werden. Händler mit mehreren Quellen erstellen bei Bedarf benutzerdefinierte Lager für benutzerdefinierte Quellen und Websites.

![Diagramm für z. B. Lager für einen Store](assets/diagram-stock.png){width="600" zoomable="yes"}

## Erzeugnismengen

&quot;Menge&quot;ist die Anzahl der Produkte in Ihrem aktiven Bestand, die zum Kauf verfügbar sind. Die Produktmenge steigt und nimmt ab, wenn Sie Sendungen abschließen oder den Lagerbestand anpassen. Das Hinzufügen von Produkten zu einem Warenkorb wirkt sich nicht auf diesen Betrag aus. Die Verkaufsmenge verfolgt die Verfügbarkeit des Produkts für einen Vertriebskanal und verwendet diesen Wert auch zur Bestimmung des zu kaufenden Bestands. Abhängig von der Anzahl Ihrer Quellen sehen und verwalten Sie die Produktmenge für eine der folgenden Optionen:

- **Menge** - Bei Einzelquell-Händlern verfolgen die Spalte _[!UICONTROL Quantity]_und der Wert die Menge des verfügbaren In-Hand-Bestands.
- **Menge pro Source** - Bei Händlern mit mehreren Quellen wird in der Spalte &quot;_[!UICONTROL Quantity per Source]_&quot; und in den Werten der lokale Bestand nach Standort verfolgt. Wenn Sie mehrere Quellen hinzufügen, ersetzt dieser Wert die Menge und listet jede Quelle und zugewiesene Menge auf.

Reservierungen verfolgen Lageranforderungen für den gesamten Einkaufsprozess - Hinzufügen von Produkten zum Warenkorb, Abschließen des Checkout und Verwalten von Erstattungen. Für verfügbare Bestände und Lager reservieren Lagerbestände pro Bestellung durch den Checkout-Prozess, abgezogen von der verkaufbaren Menge. Reservierungen werden in Mengenabzüge umgewandelt, wenn Produkte in Rechnung gestellt und versandt werden.

Die Verkaufsmenge berechnet das virtuelle Inventar der Produkte (oder der Verfügbarkeit) anhand konfigurierter Schwellenwerte, reservierter oder verkaufter Mengen und Mengen pro Quelle. Für jeden Bestand greift [!DNL Commerce] auf alle zugewiesenen Quellen zu und aggregiert die zugehörigen Produktmengen. Bei diesem Basiswert werden dann alle Reservierungsbeträge und der Schwellenwert _[!UICONTROL Notify for Quantity Below]_abgezogen.

![Berechnung der Verkaufsmenge für einen Bestand](assets/diagram-salable-quantity.png){width="600" zoomable="yes"}

## Lagerkonfigurationen

Jedes Produkt, jede Quelle und jeder Lager enthält mehrere Optionen, die für Ihren Store auf globaler, Quell-, Lager- und Produktebene konfiguriert werden können. Eine vollständige Liste dieser Optionen finden Sie unter [Konfigurieren von Inventory management](configuration.md).

Die folgenden Optionen sind wichtig, um [!DNL Inventory Management] zu verstehen:

- **[!UICONTROL Out-of-Stock Threshold]** - Legt einen Betrag fest, der von Ihrer Verkaufsmenge abgezogen werden soll. Wenn Sie Rückstellungen aktivieren, wird dieser Wert nicht von der Salable Quantity abgezogen.
- **[!UICONTROL Backorders]** - Bestimmt, ob Produkte über einen Nullbestand hinaus verkauft werden können, um Bestellungen zu sparen, bis sie wieder aufgestockt werden. Wenn Rückstände aktiviert sind, wird empfohlen, den [!UICONTROL Out-of-Stock Threshold] zu konfigurieren.

>[!NOTE]
>
>Der Schwellenwert für nicht vorrätige Bestände unterstützt negative und positive Beträge. Wenn Sie Rückaufträge aktivieren, setzen Sie diesen Wert auf einen negativen Betrag für die maximale Anzahl von Produkten, die zurückbestellt werden können, bevor das Produkt wirklich als nicht vorrätig betrachtet wird.

## Inventory management-Demo

Sehen Sie sich dieses Video an, um mehr über Inventory management-Quellen und -Lager zu erfahren:

>[!VIDEO](https://video.tv.adobe.com/v/343748?quality=12)
