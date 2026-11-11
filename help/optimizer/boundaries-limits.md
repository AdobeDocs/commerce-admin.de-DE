---
title: Beschränkungen und Grenzen der Merchandising-Services
description: Erfahren Sie mehr über Adobe Commerce Optimizer-Lizenzbeschränkungen und Systemgrenzen. Planen Sie die Kapazität, verfolgen Sie die Nutzung und vermeiden Sie Latenz und Drosselung bei der Überschreitung von Grenzwerten.
role: Admin, Developer
hide: true
badgeSaas: label="Nur SaaS" type="Positive" url="https://experienceleague.adobe.com/de/docs/commerce/user-guides/product-solutions" tooltip="Gilt nur für Adobe Commerce as a Cloud Service-Instanzen, die mit CCDM bereitgestellt werden (von Adobe verwaltete SaaS-Infrastruktur)."
autotag-review: '2026-11-02T18:48:38.168Z'
TQID: 'https://experienceleague.adobe.com/KoRp--G2sMvv-Hr7KiHriZrFmtEm0BhGoGWVQQK-ofE'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
  - id: de2e2e68-c5d7-4efe-be7b-27528698f06b
    internal-label: Commerce as a Cloud Service
feature_v2:
  - id: 5a951749-fac9-5bc7-9a98-ebe4ff066437
    internal-label: Cloud
  - id: 8d0b446f-5b16-5a10-b272-01143504a11c
    internal-label: System
  - id: d3b92bef-63fa-5031-a925-d04d9362d616
    internal-label: Saas
source-git-commit: 71df9ad673f2e7dff802e4b26d8e169c42d9c063
workflow-type: tm+mt
source-wordcount: '1006'
ht-degree: 1%
---

# Beschränkungen und Grenzen der Merchandising-Services mit dem zusammensetzbaren Katalogdatenmodell (CCDM)

Adobe Commerce Merchandising Services mit CCDM wendet Lizenzbeschränkungen und Systemgrenzen an, die definieren, wie viel Kapazität Ihr Projekt verwenden kann:

- **Lizenzbeschränkungen** - Abhängig von Ihrer erworbenen Kapazität; kann durch den Kauf zusätzlicher Pakete erweitert werden.
- **Systemgrenzen** - Feste Grenzwerte, die Systemressourcen schützen und eine zuverlässige Leistung für alle Benutzer sicherstellen.

Ihre Nutzung muss innerhalb dieser Grenzen bleiben. Sie zu überschreiten kann zu erhöhter Latenz und Anfragebeschränkung führen.

## Zusätzliche Kapazität anfordern

Lizenzbeschränkungen können erhöht werden, indem Sie die Lizenzpakete erwerben, die im Abschnitt [Lizenzbeschränkungen und Systemgrenzen](#license-limits-and-system-boundaries) beschrieben sind, oder indem Sie benutzerdefinierte Lizenzen für eindeutige Anwendungsfälle aushandeln. Wenden Sie sich an Ihren Adobe-Kundenbetreuer, um Ihre Anforderungen zu besprechen.

Wenden Sie sich bei Fragen zu Systemgrenzen an den [Adobe-Support](https://experienceleague.adobe.com/home?lang=de#support).

## Leistungsprobleme verhindern

Befolgen Sie diese Best Practices, um innerhalb der Beschränkungen zu bleiben und betriebliche Probleme zu vermeiden:

- **Überprüfen Sie Ihre**: Machen Sie sich mit Ihren [Kapazitätsbeschränkungen](#license-limits-and-system-boundaries) vertraut, bevor Sie neue Storefronts oder Kampagnen starten.
- **Nutzung nachverfolgen** - Verwenden Sie integrierte Metriken-Dashboards oder CDN-Protokolle.

## Lizenzbeschränkungen und Systemgrenzen

In den folgenden Tabellen sind die Lizenzbeschränkungen und Systemgrenzen nach Funktionsbereich zusammengefasst und gegebenenfalls Informationen zum Hinzufügen zusätzlicher Lizenzen zur Erweiterung der Kapazität enthalten.


### Katalog

| **Funktion** | **Beschreibung** | **Basiszuweisung** | **Erweiterbar?** |
| --- | --- | --- | --- |
| Aufnahmegeschwindigkeit eines Produkts | Die Anzahl der erstellten oder aktualisierten Produkte | 1K Aktualisierungen pro Minute<p>Maximal 100.000 Aktualisierungen pro Tag</p> | Ja<p>Ein Lizenzpaket hinzufügen:</p><ul><li>5.000 Aktualisierungen pro Minute<br>maximal 5.000 Aktualisierungen pro Tag</li> <li>10.000 Updates pro Minute<br>maximal 1.000 Updates pro Tag</li></ul><p>Die maximale Kapazität für die Datenaufnahme beträgt 1 Million Aktualisierungen pro Tag.</p> |
| Payload-Größe des Produkts | Die maximale Datenmenge, die beim Erstellen, Aktualisieren oder Aufnehmen von Produktinformationen mithilfe der API zulässig ist | 200 KB | Nein |
| Katalogvarianten | Die Anzahl der Ansichten eines Katalogs, die Storefront-Benutzern zur Verfügung stehen,<p>die gezählt werden als (*Anzahl der Katalogansichten × Anzahl der Preisbücher*)</p> | 100 Varianten | Ja<p>100 Katalogvarianten-Lizenzpaket hinzufügen</p> |
| Produkte in einer einzigen Katalogquelle | Im Katalog unterstützte SKUs | 250K SKUs | Ja<p>100K SKU-Lizenzpaket hinzufügen</p> |
| Varianten pro Produkt | Die Anzahl der pro Produkt zulässigen Produktvarianten (Größe, Farbkombinationen) | 10 K | Nein |
| Katalogquellen | Die Anzahl der Katalogdatenkontexte (z. B. Gebietsschemata oder Datenquellen wie PIMs und ERPs) | 50 | Nein |

{style="table-layout:auto"}

### Preisbücher

| **Funktion** | **Beschreibung** | **Basiszuweisung** | **Erweiterbar?** |
| --- | --- | --- | --- |
| Preisbücher | Die Anzahl der pro Instanz zulässigen Preisverzeichnisse | Basierend auf der Anzahl der [Katalogvarianten](#catalog) | Ja<br>Katalogvarianten erhöhen |
| Rabatte pro Preisnachweis | Die Anzahl der Rabatte, die auf einen Produktpreis innerhalb eines einzigen Preisbuchs angewendet werden können | 10 | Nein |

{style="table-layout:auto"}

### Katalogansichten und Richtlinien

| **Funktion** | **Beschreibung** | **Basiszuweisung** | **Erweiterbar?** |
| --- | --- | --- | --- |
| Katalogansichten | Anzahl der konfigurierbaren Teilmengen des Hauptkatalogs | Basierend auf der Anzahl der [Katalogvarianten](#catalog) | Ja<br>Katalogvarianten erhöhen |
| Richtlinien pro Katalogansicht | Anzahl der zulässigen Datenfilter | 10 | Nein |
| Attributwerte in einer Richtlinie | Anzahl der Produktmerkmale, die für die Filterung konfiguriert werden können | 100 | Nein |
| [Tastenzuweisung für eingeschränkten Zugriff](setup/private-catalog-view.md) | Anzahl der eingeschränkten Zugriffsschlüssel, die einer einzelnen Katalogansicht zugewiesen werden können | 3 | Nein |
| RSA-Schlüsselgröße (eingeschränkte Zugriffsschlüssel) | Minimale und maximale Schlüsselstärke, die für einen eingeschränkten Zugriffsschlüssel akzeptiert wird | Minimum 2048 Bit, Maximum 8192 Bit | Nein |
| Schlüssel für eingeschränkten Zugriff | Verzögerung der Schlüsselsperrweitergabe | Bis zu 5 Minuten aufgrund des Caching. Von einem entfernten Schlüssel signierte Token werden verweigert, sobald die Verzögerung abgelaufen ist. | Nicht zutreffend |

{style="table-layout:auto"}

### Katalog-Storefront

Die Basiszuweisung für die Funktionen der Katalog-Storefront wird auf der Grundlage der GMV-Stufe (Bruttowarenwert) bestimmt. Die Tabelle zeigt die Mindestzuweisung für jede Funktion an.

| **Funktion** | **Beschreibung** | **Basiszuweisung** | **Erweiterbar?** |
| --- | --- | --- | --- |
| Abrufrate des Katalogs | Anzahl der Aufrufe einer Katalog-API pro Monat durch ein System (Storefront, Transaktionssystem, ERP oder sonstiges), um Daten aus dem Katalog abzurufen | Basierend auf GMV-Stufe<p>Mindestzuweisung: 10 Mio./Monat</p> | Ja<p>1 Million Anfragen pro Monat für Lizenzpakete hinzufügen</p> |
| Inhaltsanfragen | Anfragen an die Storefront für HTML-Seitenansichten oder JSON-API-Aufrufe. Wird als 1 Seitenansicht oder 5 API-Aufrufe gezählt. | Basierend auf GMV-Stufe<p>Mindestzuweisung: 2 Mio./Monat</p> | Ja<p>1 Million pro Monat Lizenzpaket hinzufügen</p> |
| Storefront GenAI-Varianten | Toleranz für die textbasierte Inhaltserstellung | Basierend auf GMV-Stufe<p>Mindestzuweisung: 1.000 Varianten/Monat</p> | Ja<p>Generative KI-Credits separat erwerben</p> |

{style="table-layout:auto"}

>[!NOTE]
>
>Für die Bildgenerierung ist eine [!DNL Adobe Firefly]-Lizenz erforderlich, die für dieselbe IMS-Organisation wie [!DNL Adobe Commerce Optimizer] bereitgestellt wird.


### Produkterkennung

Die folgenden Einschränkungen gelten für die Storefront-Produktsuche, -Auflistung und -Merchandising-Konfiguration.

| **Funktion** | **Beschreibung** | **Basiszuweisung** | **Erweiterbar?** |
| --- | --- | --- | --- |
| Produktabruf | Maximale SKUs pro [!DNL Catalog Service] GraphQL-Anfrage beim Abrufen von Produktdaten mit `products`, `productSearch`, `refineProduct` und `variants`. Teilen Sie größere Anfragen auf mehrere Aufrufe auf. | 100 | Nein |
| Filterbare Attribute | Die Anzahl der Produktmerkmale (z. B. Farbe, Größe, Marke oder Material), die für die mehrschichtige Navigation und Facetten aktiviert werden können | 200 | Nein |
| Durchsuchbare Attribute | Die Anzahl der Produktmerkmale, die für die Katalogsuche indiziert werden können | 200 | Nein |
| Sortierbare Attribute | Die Anzahl der Produktmerkmale, die als Sortieroptionen auf Such- und Kategorieseiten verfügbar sind. | 50 | Nein |
| Paginierungstiefe suchen | Maximal erreichbare Produkte durch Suchpaginierung (z. B. Seite 100 × 100 Produkte/Seite) | 10 K | Nein |
| Facetten | Die Anzahl der filterbaren Produktattribute (wie Marke, Farbe, Größe, Preis), die konfiguriert werden können, um Käufern zu helfen, Suchergebnisse zu verfeinern und Kategorien zu durchsuchen | 100<p>Muss filterbare Attribute sein</p> | Nein |
| Optionen pro Facette | Die Anzahl der filterbaren Produktattributwerte, die Käufer innerhalb einer Facette auswählen können (z. B. „Rot“, „Blau“ für Farbe; „Klein“, &quot;Medium&quot; für Größe) | 100 | Ja<p>Kann über eine Support-Anfrage erhöht werden</p> |

{style="table-layout:auto"}

### Recommendations

Die folgenden Funktionen sind für Produktempfehlungen verfügbar. Einige in anderen Adobe Commerce-Produkten verfügbare Funktionen werden in [!DNL Adobe Commerce Optimizer] nicht unterstützt.

| **Funktion** | **Beschreibung** | **Basiszuweisung** | **Erweiterbar?** |
| --- | --- | --- | --- |
| Aktive Empfehlungseinheiten | Anzahl der Live-Empfehlungskomponenten in Ihrer Storefront (z. B. „Kunden haben sich auch angesehen“ oder „Ihnen könnte das auch gefallen„) | 50 | Nein |
| Ein-/Ausschlüsse von Kategorien oder Attributen | Produkte nach einem bestimmten Satz filtern, der für Recommendations geeignet ist | Nicht unterstützt | — |

{style="table-layout:auto"}
