---
title: Erstellen einer zugehörigen Produktregel
description: Erfahren Sie, wie Sie eine Regel für verwandte Produkte erstellen, die ausgelöst werden kann, um verwandte Produkte, Upsell und Crosssell anzuzeigen.
exl-id: fbc059ec-d3e6-46ca-810a-a979a0631dd8
feature: Merchandising, Products, Storefront
source-git-commit: cea943cd7f4d148c885fbd113c3bc08bfdf63ea0
workflow-type: tm+mt
source-wordcount: '655'
ht-degree: 0%

---

# Erstellen einer zugehörigen Produktregel

{{ee-feature}}

Der Prozess der Erstellung einer Regel für verwandte Produkte ähnelt dem Einrichten einer Preisregel. Zuerst definieren Sie die Bedingungen, die erfüllt werden sollen, und wählen dann die Produkte aus, die angezeigt werden sollen. Es kann immer mehrere aktive Regeln geben, die ausgelöst werden können, um verwandte Produkte, Upsell und Crosssell anzuzeigen. Die Priorität jeder Regel bestimmt die Reihenfolge, in der der Produktblock auf der Seite angezeigt wird.

>[!NOTE]
>
>Damit ein Attribut in einer Zielregel verwendet werden kann, muss die [_[!UICONTROL Use for Promo Rule Conditions]_](../catalog/product-attributes.md)-Eigenschaft auf `Yes` festgelegt sein.

>[!NOTE]
>
>Der Wert für den `All Store Views` wird immer sowohl für [!UICONTROL Products to Match] als auch für [!UICONTROL Products to Display] Bedingungen für alle Produktattribute verwendet. Dies gilt auch, wenn die Produktattribute unterschiedliche Werte für verschiedene Ansichten und Websites von Stores haben.

## Erstellen einer zugehörigen Produktregel

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_>**[!UICONTROL Related Product Rules]**.

1. Klicken Sie oben rechts auf **[!UICONTROL Add Rule]**.

   ![Regel für verwandte Produkte - Informationen](./assets/catalog-related-products-rule-information.png){width="600" zoomable="yes"}

1. Vervollständigen Sie die **[!UICONTROL Rule Information]** wie folgt:

   - Geben Sie einen **[!UICONTROL Rule Name]** ein, um die Regel beim Arbeiten in der Admin-Gruppe zu identifizieren.

   - Geben Sie **[!UICONTROL Priority]** eine Zahl ein, die die Reihenfolge bestimmt, in der die Ergebnisse auf der Seite angezeigt werden, wenn Ergebnisse aus anderen Regeln auf dieselbe Position abzielen. Nummer `1` hat höchste Priorität.

   - Um die Regel zu aktivieren, setzen Sie **[!UICONTROL Status]** auf `Active`.

   - Legen Sie **[!UICONTROL Apply To]** auf eine der folgenden Einstellungen fest:

      - `Related Products`
      - `Up-sells`
      - `Cross-sells`

   - Wenn die Regel für einen bestimmten Zeitraum aktiv sein soll, geben Sie das **[!UICONTROL From]**- und **[!UICONTROL To]** ein.

   - Geben Sie **[!UICONTROL Result Limit]** die Anzahl der Datensätze ein, die in der Ergebnisliste angezeigt werden sollen. Die maximale Zahl ist 20.

   - Wenn die Regel für ein bestimmtes [Kundensegment](../customers/customer-segments.md) gilt, setzen Sie **[!UICONTROL Customer Segments]** auf `Specified` und wählen Sie das Kundensegment aus der Liste aus.

   - Wenn die Regel für eine bestimmte [Real-Time CDP-Zielgruppe](../customers/audience-activation.md) gilt, setzen Sie **[!UICONTROL Real-Time CDP Audience]** auf `Specified` und wählen Sie die Real-Time CDP-Zielgruppe aus der Liste aus. Diese Funktion befindet sich in der Betaphase. Wenn Sie am Beta-Programm teilnehmen möchten, senden Sie eine Anfrage an [dataconnection@adobe.com](mailto:dataconnection@adobe.com).

     ![Regel für verwandte Produkte - Real-Time CDP-Zielgruppe](./assets/rtcdp-related-products.png){width="500"}

1. Wählen Sie im linken Bedienfeld **[!UICONTROL Products to Match]** und erstellen Sie die Bedingungen wie für eine [Katalogpreisregel](price-rules-catalog.md).

   ![Regel für verwandte Produkte - Abzugleichende Produkte](./assets/catalog-related-products-match.png){width="500"}

1. Wählen Sie im linken Bedienfeld **[!UICONTROL Products to Display]** und erstellen Sie die Ergebnisbedingungen so, wie Sie es für eine [Katalogpreisregel) &#x200B;](price-rules-catalog.md).

   ![Regel für verwandte Produkte - anzuzeigende Produkte](./assets/catalog-related-products-to-display.png){width="500"}

   Schließen Sie die Bedingung ab, um die Produkte zu beschreiben, die Sie in die angezeigten Ergebnisse aufnehmen möchten.

1. Klicken Sie abschließend auf **[!UICONTROL Save]**.

## Löschen einer zugehörigen Produktregel

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_>**[!UICONTROL Related Product Rules]**.

1. Suchen Sie die zugehörige Produktregel, die Sie löschen möchten.

1. Klicken Sie auf die Regel, um die Detailseite zu öffnen.

1. Klicken Sie oben rechts auf **[!UICONTROL Delete]**.

1. Um die Aktion zu bestätigen, klicken Sie auf **[!UICONTROL OK]**.

## Demo zu verwandten Produktregeln

In diesem Video erfahren Sie mehr über das Erstellen von Regeln für verwandte Produkte:

>[!VIDEO](https://video.tv.adobe.com/v/3417565?quality=12&learn=on&captions=ger)

## Feldbeschreibungen

| Feld | Beschreibung |
|--- |--- |
| [!UICONTROL Rule Name] | Ein Name, der die Regel für die interne Verwendung identifiziert. |
| [!UICONTROL Priority] | Bestimmt die Reihenfolge, in der die Ergebnisse der Regel angezeigt werden, wenn sie mit anderen Ergebnissätzen angezeigt werden, die dieselbe Stelle auf der Seite zum Ziel haben. Der Wert kann auf eine beliebige Ganzzahl festgelegt werden, wobei die höchste Priorität 1 ist. Wenn beispielsweise mehrere Upsell-Regeln gelten, wird die Regel mit der höchsten Priorität vor den anderen angezeigt. Die Sortierreihenfolge der Produkte innerhalb jeder Ergebnismenge ist zufällig. Alle Upsell-, Crosssell- und zugehörigen Produkte, die manuell konfiguriert wurden, werden immer vor den regelbasierten Produktaktionen auf der Seite angezeigt. |
| [!UICONTROL Status] | Steuert den aktiven Status der Regel. Optionen: `Active` / `Inactive` |
| [!UICONTROL Apply To] | Gibt den Typ der Produktbeziehung an, die mit der Regel verknüpft ist. Optionen: `Related Products` / `Up-sells` / `Cross-sells` |
| [!UICONTROL From Date] | Wenn die Regel über einen bestimmten Zeitraum aktiv ist, bestimmt diese Einstellung das erste Datum, an dem die Regel aktiv ist. |
| [!UICONTROL To Date] | Wenn die Regel über einen bestimmten Zeitraum aktiv ist, bestimmt diese Einstellung das letzte Datum, an dem die Regel aktiv ist. |
| [!UICONTROL Result Limit] | Bestimmt die Anzahl der Produkte, die gleichzeitig in den Ergebnissen angezeigt werden. Die maximale Zahl ist 20. Wenn mehr übereinstimmende Ergebnisse gefunden werden, drehen sich die Produkte bei jeder Aktualisierung der Seite durch den Block. |
| [!UICONTROL Customer Segments] | Identifiziert die Kundensegmente, für die die Regel gilt. Optionen: `All` / `Specified` |

{style="table-layout:auto"}
