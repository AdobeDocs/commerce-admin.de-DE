---
title: Preisbücher
description: Erfahren Sie, wie Preislisten aus Katalog- und Preisdaten in [!DNL Adobe Commerce] zugeordnet werden.
role: Admin, Developer
recommendations: noCatalog
badgeSaas: label="Nur SaaS" type="Positive" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Gilt nur für Adobe Commerce as a Cloud Service-Instanzen, die mit CCDM bereitgestellt werden (von Adobe verwaltete SaaS-Infrastruktur)."
TQID: 'https://experienceleague.adobe.com/8gpl-l6oQebTnrt-00-n1FEdKnzqhTQi3hRz4lrGQoE'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
  - id: de2e2e68-c5d7-4efe-be7b-27528698f06b
    internal-label: Commerce as a Cloud Service
feature_v2:
  - id: 3033d2ab-c1d2-5b52-b865-72d9e5ad2c37
    internal-label: Currency
  - id: 58c984c2-e237-5c50-9718-500e40d1e82c
    internal-label: Merchandising
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
source-git-commit: 1041abe0e7d7c1212a717d5fd03180ce7fd32958
workflow-type: tm+mt
source-wordcount: '603'
ht-degree: 0%
---
# Preisbücher

Preisbücher definieren Produktpreise für eine Katalogquelle über Kundenebenen und Märkte hinweg. Sie unterstützen eine Hierarchie der Preisbücher für Eltern und Kinder.

![Preisbuchhierarchie](../assets/price-book-hier.png)

## Schlüsselkonzepte

| Begriff | Beschreibung |
| ------ | ------------- |
| **Preisbuch** | Logische Gruppierung, die Preise für eine Katalogquelle definiert, z. B. eine bestimmte Region oder Kundenebene, und zur Verwaltung von Produktpreisen verwendet wird. |
| **Fallback-Preisbuch** | Das beste Preisbuch in einer Hierarchie. Es hat kein übergeordnetes Element und ist das *einzige* Preisbuch, das die Währung für sich selbst und alle seine untergeordneten Preisbücher definiert.<br/><br/>Wenn bei der Erstellung des Preisbuchs (über die API) kein übergeordnetes Element definiert wird, wird ein neues Fallback-Preisbuch erstellt. |
| **Übergeordnetes Preisbuch** | Ein übergeordnetes Preisbuch, aus dem ein untergeordnetes Preisbuch Preise übernehmen kann, wenn diese nicht explizit im Kind festgelegt sind. |
| **Hierarchietiefe** | Maximal drei Ebenen (Fallback -> Untergeordnet -> Enkelkind), <br/><br/> bei der Aufnahme nicht erzwungen werden. |
| **Währung** | Wird nur für das Fallback-Preisbuch definiert. Von allen untergeordneten Preisbüchern übernommen.<br/><br/>Wenn die Währung bei der Erstellung des Fallback-Preisbuchs (über die API) nicht angegeben wird, wird die Währung standardmäßig auf USD festgelegt. |
| **Produktpreis** | Der spezifische Preis, der einem Produkt (SKU) innerhalb eines bestimmten Preisbuchs zugewiesen ist. |
| **Rabatte** | Rabatte sind im Produktpreis definiert. Nicht vererbt. |

## Preisbuchumsetzung

Bei Verwendung von Adobe Commerce as a Cloud Service mit dem Composable Catalog Data Model (CCDM) werden die Preisverzeichnisse aus den Katalog- und Preisdaten zugeordnet. Sie werden nicht manuell erstellt.

Allgemein betrachtet lautet die Zuordnung:

- **Store-Ansicht → Katalogquelle** - Store-Ansicht-Produktdaten, einschließlich lokalisierter Attribute, werden einer Katalogquelle zugeordnet.
- **Website → Preisbuch oder Preisbücher** - Website-Preiskarten werden dem jeweiligen Preisbuch bzw. den jeweiligen Preisbüchern zugeordnet.
- **Kundengruppenpreise → Preisbucheinträge** - Kundengruppenpreise werden den entsprechenden Preiseinträgen zugeordnet.

Verwalten Sie den Quellkatalog, die Website und die Preiskonfiguration in der Adobe Commerce-Konfiguration und weisen Sie dann die zugeordneten Preisbücher in der entsprechenden Katalogansicht zu, indem Sie die verfügbaren Preisbücher konfigurieren. Wenn keine Preisbücher zugeordnet sind, verwendet die Katalogansicht das Standardpreisbuch.

Eine Katalogansicht verwendet die Konfiguration Verfügbare Preislisten mit ihren Katalogdaten und -richtlinien, um das Merchandising-Erlebnis zu bestimmen, einschließlich der für Produkte zurückgegebenen Preise.

>[!NOTE]
>
>Für Commerce B2B erstellt das System und weist jeder Katalogansicht basierend auf der Konfiguration des freigegebenen Katalogs ein einheitliches Preisbuch zu. Für diese Ansichten müssen Sie die Preisbuchverfügbarkeit nicht konfigurieren.

## Abrechnungspreise

Preisbücher unterstützen das Merchandising- und Storefront-Katalogerlebnis. Commerce Core verarbeitet weiterhin Warenkorb- und Checkout-Vorgänge. Ein Preis, der nur in CCDM verfügbar ist, wird nicht automatisch zu dem Preis, der von der Kasse verwendet wird.

Halten Sie die Preise mit der Commerce-Kernkonfiguration konsistent und testen Sie die angezeigten Preise, das Hinzufügen zum Warenkorb, die Werbeaktionen und den Checkout im Rahmen der Implementierungsvalidierung.

## Preislisten anzeigen

Nachdem die Synchronisierung der Katalogdaten abgeschlossen ist, können Sie die verfügbaren Preislisten und deren IDs im Arbeitsbereich **[!UICONTROL Catalog views]** anzeigen.

1. Navigieren Sie zu _Store-Setup_ und klicken Sie auf **[!UICONTROL Catalog views]**.

1. Klicken Sie auf **[!UICONTROL Create catalog view]**.

1. Die verfügbaren Preisverzeichnisse finden Sie im Abschnitt **[!UICONTROL Price Books]** der Konfiguration der Katalogansicht.

   ![Preisbuch-Namen und -IDs](../assets/price-book-name-ids.png)

## Preisbuchverfügbarkeit konfigurieren

Ordnen Sie zugeordnete Preislisten Katalogansichten zu, indem Sie verfügbare Preislisten im Arbeitsbereich Katalogansichten in der Commerce-Admin konfigurieren.

>[!NOTE]
>
>Eine private Katalogansicht (mit aktiviertem [!UICONTROL Catalog Protection]) kann nur auf ein Preisbuch verweisen.

1. Wählen Sie im Arbeitsbereich **[!UICONTROL Catalog views]** die Katalogansicht aus, die Sie konfigurieren möchten.

1. Wählen Sie im Abschnitt **[!UICONTROL Price Books]** die Preisverzeichnisse aus, die für Geschäfte verfügbar sind, die durch die Katalogansicht gestützt werden.
