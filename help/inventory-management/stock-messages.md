---
title: Szenarien mit Lagermeldungen
description: Erfahren Sie mehr über die Kombination von Konfigurationseinstellungen, die Meldungen zur Lagerverfügbarkeit auf Produktseiten und in Listen von Produkten auf Katalogseiten steuern.
exl-id: 63114305-e695-445b-91cd-9e0fb2729ec4
feature: Inventory, Configuration
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '342'
ht-degree: 2%

---

# Szenarien mit Lagermeldungen

Sie können eine Kombination aus Konfigurationseinstellungen verwenden, um Meldungen zur Lagerverfügbarkeit auf Produktseiten und in Listen von Produkten auf Katalogseiten zu steuern.

![Gruppiertes Produkt mit &quot;Nicht auf Lager&quot;-Meldung](assets/storefront-out-of-stock-message.png){width="600" zoomable="yes"}

## Lagerpositionen der Produktseiten

Je nach Kombination der Einstellungen für die Verwaltung von Lagern und die Lagerverfügbarkeit stehen für die Produktseite verschiedene Varianten der Nachrichten zur Verfügung.

### Beispiel 1: Verfügbarkeitsmeldung anzeigen

#### Szenario 1

Diese Kombination von Einstellungen bewirkt, dass die Verfügbarkeitsmeldung je nach Lagerverfügbarkeit der einzelnen Produkte auf der Produktseite angezeigt wird.

| Lageroptionen | Einstellung | Nachricht |
|--|--|--|
| [!UICONTROL Display product availability in stock in the frontend] | `Yes` | |
| [!UICONTROL Manage Stock] | `Yes` | |
| [!UICONTROL Stock Availability] | `In Stock` | _[!UICONTROL Availability: In Stock]_ |
| | `Out of Stock` | _[!UICONTROL Availability: Out of Stock]_ |

#### Szenario 2

Wenn für ein Produkt kein Lager verwaltet wird, kann diese Kombination von Einstellungen verwendet werden, um die Verfügbarkeitsmeldung auf der Produktseite anzuzeigen.

| Lageroptionen | Einstellung | Nachricht |
|--|--|--|
| [!UICONTROL Display product availability in stock in the frontend] | `Yes` |  |
| [!UICONTROL Manage Stock] | `No` | _[!UICONTROL Availability: In Stock]_ |

### Beispiel 2: Meldung zur Verfügbarkeit ausblenden

#### Szenario 1

Diese Kombination aus Konfiguration und Produkteinstellungen verhindert, dass die Verfügbarkeitsmeldung auf der Produktseite angezeigt wird.

| Lageroptionen | Einstellung | Nachricht |
|--|--|--|
| [!UICONTROL Display product availability in stock in the frontend] | `No` |  |
| [!UICONTROL Manage Stock] | `Yes` |  |
| [!UICONTROL Stock Availability] | `In Stock` | Keines |
|  | `Out of Stock` | Keines |

#### Szenario 2

Wenn für ein Produkt kein Lager verwaltet wird, verhindert diese Kombination aus Konfiguration und Produkteinstellungen, dass die Verfügbarkeitsmeldung auf der Produktseite angezeigt wird.

| Lageroptionen | Einstellung | Nachricht |
|--|--|--|
| [!UICONTROL Display product availability in stock in the frontend] | `No` |  |
| [!UICONTROL Manage Stock] | `No` | Keines |

## Lagerergänzungen für Katalogseiten

Die folgenden Anzeigeoptionen sind je nach Produktverfügbarkeit und Konfigurationseinstellungen für die Kategorie und die Liste der Suchergebnisse möglich.

![Nicht auf Lager befindliche Meldung auf Kategorieseite](assets/storefront-out-of-stock-catalog-page.png){width="600" zoomable="yes"}

### Beispiel 1: Produkt mit Meldung &quot;Nicht vorrätig&quot;anzeigen

Diese Kombination von Konfigurationseinstellungen umfasst nicht vorrätige Produkte in der Kategorie und Suchergebnislisten und zeigt eine Meldung &quot;Nicht vorrätig&quot;an.

| Lageroptionen | Einstellung | Nachricht |
|--|--|--|
| [!UICONTROL Display Out of Stock Products] | `Yes` |  |
| [!UICONTROL Display product availability in stock in the frontend] | `Yes` | _[!UICONTROL Out of stock]_ |
| [!UICONTROL Display Out of Stock Products] | `Yes` |  |
| [!UICONTROL Display product availability in stock in the frontend] | `No` | Keines |

### Beispiel 2: Produkt ohne Meldung &quot;Nicht vorrätig&quot; anzeigen

Diese Kombination von Konfigurationseinstellungen umfasst nicht vorrätige Produkte in der Kategorie und Suchergebnislisten, zeigt jedoch keine Nachricht an.

| Lageroptionen | Einstellung | Nachricht |
|--|--|--|
| [!UICONTROL Display Out of Stock Products] | `Yes` | Keines |
| [!UICONTROL Display product availability in stock in the frontend] | `No` |  |

### Beispiel 3: Produkt so lange ausblenden, bis es wieder auf Lager ist

Bei dieser Konfigurationseinstellung werden Lagerprodukte vollständig aus der Kategorie und Suchergebnisliste ausgeschlossen, bis sie wieder auf Lager sind.

| Lageroptionen | Einstellung | Nachricht |
|--|--|--|
| [!UICONTROL Display Out of Stock Products] | `No` | Keines |
