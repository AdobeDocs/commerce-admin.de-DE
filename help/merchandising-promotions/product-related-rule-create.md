---
title: Erstellen einer verwandten Produktregel
description: Erfahren Sie, wie Sie eine verwandte Produktregel erstellen, die ausgelöst werden kann, um verwandte Produkte, Upsells und Querverkäufe anzuzeigen.
exl-id: fbc059ec-d3e6-46ca-810a-a979a0631dd8
feature: Merchandising, Products, Storefront
source-git-commit: 4971fe457b7fd58d8b71951981bc889386610a99
workflow-type: tm+mt
source-wordcount: '656'
ht-degree: 0%

---

# Erstellen einer verwandten Produktregel

{{ee-feature}}

Der Prozess der Erstellung einer verwandten Produktregel ähnelt dem Einrichten einer Preisregel. Zunächst definieren Sie die Bedingungen, die erfüllt werden sollen, und wählen dann die Produkte aus, die angezeigt werden sollen. Es kann jederzeit mehrere aktive Regeln geben, die ausgelöst werden können, um verwandte Produkte, Upsells und Querverkäufe anzuzeigen. Die Priorität jeder Regel bestimmt die Reihenfolge, in der der Produktblock auf der Seite angezeigt wird.

>[!NOTE]
>
>Damit ein Attribut in einer Targeting-Regel verwendet werden kann, muss [_[!UICONTROL Use for Promo Rule Conditions]_](../catalog/product-attributes.md) -Eigenschaft muss auf `Yes`.

>[!NOTE]
>
>Die `All Store Views` Der Bereichswert wird immer für beide verwendet [!UICONTROL Products to Match] und [!UICONTROL Products to Display] -Bedingungen für alle Produktattribute. Dies gilt auch, wenn die Produktattribute unterschiedliche Werte für verschiedene Store-Ansichten und Websites haben.

## Erstellen einer verwandten Produktregel

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_>**[!UICONTROL Related Product Rules]**.

1. Klicken Sie oben rechts auf **[!UICONTROL Add Rule]**.

   ![Regel für verwandte Produkte - Informationen](./assets/catalog-related-products-rule-information.png){width="600" zoomable="yes"}

1. Führen Sie die **[!UICONTROL Rule Information]** wie folgt:

   - Geben Sie einen **[!UICONTROL Rule Name]** , um die Regel beim Arbeiten in der Admin-Konsole zu identifizieren.

   - Für **[!UICONTROL Priority]** Geben Sie eine Zahl ein, die bestimmt, in welcher Reihenfolge die Ergebnisse auf der Seite angezeigt werden, wenn Ergebnisse aus anderen Regeln auf denselben Ort abzielen. Zahl `1` höchste Priorität.

   - Um die Regel zu aktivieren, legen Sie **[!UICONTROL Status]** nach `Active`.

   - Satz **[!UICONTROL Apply To]** auf einen der folgenden Werte zu:

      - `Related Products`
      - `Up-sells`
      - `Cross-sells`

   - Wenn die Regel für einen bestimmten Zeitraum aktiv sein soll, geben Sie die **[!UICONTROL From]** und **[!UICONTROL To]** Daten.

   - Für **[!UICONTROL Result Limit]** die Anzahl der Datensätze angeben, die in der Ergebnisliste angezeigt werden sollen. Die maximale Zahl ist 20.

   - Wenn die Regel für eine bestimmte [Kundensegment](../customers/customer-segments.md), set **[!UICONTROL Customer Segments]** nach `Specified` und wählen Sie das Kundensegment aus der Liste aus.

   - (**Beta**) Wenn die Regel für eine bestimmte [Real-Time CDP-Audience](../customers/audience-activation.md), set **[!UICONTROL Real-Time CDP Audience]** nach `Specified` und wählen Sie die Real-Time CDP-Audience aus der Liste aus. Diese Funktion befindet sich in der Beta-Phase. Wenn Sie dem Betaprogramm beitreten möchten, senden Sie eine Anfrage an [dataconnection@adobe.com](mailto:dataconnection@adobe.com).

     ![Regel für verwandte Produkte - Real-Time CDP-Zielgruppe](./assets/rtcdp-related-products.png){width="500"}

1. Wählen Sie im linken Bereich die Option **[!UICONTROL Products to Match]** und erstellen Sie die Bedingungen wie für einen [Katalogpreisregel](price-rules-catalog.md).

   ![Regel für verwandte Produkte - Produkte passend](./assets/catalog-related-products-match.png){width="500"}

1. Wählen Sie im linken Bereich die Option **[!UICONTROL Products to Display]** und erstellen Sie die Ergebnisbedingungen wie für einen [Katalogpreisregel](price-rules-catalog.md).

   ![Regel für verwandte Produkte - anzuzeigende Produkte](./assets/catalog-related-products-to-display.png){width="500"}

   Füllen Sie die Bedingung aus, um die Produkte zu beschreiben, die Sie in die angezeigten Ergebnisse aufnehmen möchten.

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save]**.

## Zugehörige Produktregel löschen

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_>**[!UICONTROL Related Product Rules]**.

1. Suchen Sie die zugehörige Produktregel, die Sie löschen möchten.

1. Klicken Sie auf die Regel, um die Detailseite zu öffnen.

1. Klicken Sie oben rechts auf **[!UICONTROL Delete]**.

1. Klicken Sie zur Bestätigung der Aktion auf **[!UICONTROL OK]**.

## Demo zu verwandten Produktregeln

Sehen Sie sich dieses Video an, um mehr über das Erstellen verwandter Produktregeln zu erfahren:

>[!VIDEO](https://video.tv.adobe.com/v/343837?quality=12&learn=on)

## Feldbeschreibungen

| Feld | Beschreibung |
|--- |--- |
| [!UICONTROL Rule Name] | Ein Name, der die Regel für die interne Verwendung angibt. |
| [!UICONTROL Priority] | Bestimmt die Reihenfolge, in der die Ergebnisse der Regel angezeigt werden, wenn sie mit anderen Ergebnissätzen angezeigt werden, die auf dieselbe Stelle auf der Seite abzielen. Der Wert kann auf eine beliebige Ganzzahl mit der höchsten Priorität von 1 gesetzt werden. Wenn beispielsweise mehrere Upsell-Regeln gelten, wird die Regel mit der höchsten Priorität vor den anderen angezeigt. Die Sortierreihenfolge der Produkte in den einzelnen Ergebnismengen ist zufällig. Alle Up-Sell-, Cross-Sell- und zugehörigen Produkte, die manuell konfiguriert wurden, werden immer auf der Seite vor regelbasierten Produktpromotionen angezeigt. |
| [!UICONTROL Status] | Steuert den aktiven Status der Regel. Optionen: `Active` / `Inactive` |
| [!UICONTROL Apply To] | Identifiziert den Typ der Produktbeziehung, die mit der Regel verknüpft ist. Optionen: `Related Products` / `Up-sells` / `Cross-sells` |
| [!UICONTROL From Date] | Wenn die Regel für einen bestimmten Zeitraum aktiv ist, bestimmt diese Einstellung das erste Datum, an dem die Regel aktiv ist. |
| [!UICONTROL To Date] | Wenn die Regel für einen bestimmten Zeitraum aktiv ist, bestimmt diese Einstellung das letzte Datum, an dem die Regel aktiv ist. |
| [!UICONTROL Result Limit] | Bestimmt die Anzahl der Produkte, die in den Ergebnissen gleichzeitig angezeigt werden. Die maximale Zahl ist 20. Wenn mehr übereinstimmende Ergebnisse gefunden werden, drehen sich die Produkte jedes Mal, wenn die Seite aktualisiert wird, durch den Block. |
| [!UICONTROL Customer Segments] | Identifiziert die Kundensegmente, für die die Regel gilt. Optionen: `All` / `Specified` |

{style="table-layout:auto"}
