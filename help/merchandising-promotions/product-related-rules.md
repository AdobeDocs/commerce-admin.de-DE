---
title: Verwandte Produktregeln
description: Erfahren Sie mehr über verwandte Produktregeln und wie sie verwendet werden, um verwandte Produkte, Upsell-Angebote und Crosssell-Angebote dynamisch Ihren Kunden zu präsentieren.
exl-id: ff566e13-cbe8-42f1-be3a-684e364b86dd
feature: Merchandising, Products, Storefront
source-git-commit: 4971fe457b7fd58d8b71951981bc889386610a99
workflow-type: tm+mt
source-wordcount: '884'
ht-degree: 0%

---

# Verwandte Produktregeln (Zielgruppenregeln)

{{ee-feature}}

Mit Regeln für verwandte Produkte können Sie die Auswahl von Produkten auswählen, die Kunden als verwandte Produkte, Upsell und Crosssell präsentiert werden. Jede Produktregel kann mit einem [Kundensegment“ verknüpft werden](../customers/customer-segments.md) um eine dynamische Anzeige zielgerichteter Merchandising-Ereignisse zu erzeugen.

Da mehrere aktive Regeln gleichzeitig ausgelöst werden können, können Sie für jede Regel eine Priorität festlegen. Sie definiert die Reihenfolge, in der Regeln angewendet und Produkte auf der Seite angezeigt werden.

Um auf die zugehörigen Produktregeln zuzugreifen, gehen Sie zu **[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_>**[!UICONTROL Related Product Rules]**.

![Liste verwandter Produktregeln](./assets/related-products-rules.png){width="700" zoomable="yes"}

## Spaltenbeschreibungen

| Spalte | Beschreibung |
|--- |--- |
| [!UICONTROL ID] | Eine eindeutige numerische Kennung, die jeder zugehörigen Produktregel zugewiesen ist |
| [!UICONTROL Rule] | Der Name der zugehörigen Produktregel |
| [!UICONTROL Start] | Verwenden Sie die dynamischen Kalenderfelder (_[!UICONTROL To:]_&#x200B;und&#x200B;_[!UICONTROL From:]_), um die Liste nach dem Startdatum für die Regel zu filtern, wie es bei der Erstellung der Regel definiert wurde. |
| [!UICONTROL End] | Verwenden Sie die dynamischen Kalenderfelder (_[!UICONTROL To:]_&#x200B;und&#x200B;_[!UICONTROL From:]_), um die Liste nach dem Enddatum für die Regel zu filtern, wie es bei der Erstellung der Regel definiert wurde. |
| [!UICONTROL Priority] | Geben Sie Text in dieses Feld ein, um die Liste nach der für eine Regel definierten Priorität zu filtern. |
| [!UICONTROL Applies To] | Diese Option filtert die Liste der Regeln, die für `Related Products`, `Up-sells` und `Cross-sells` gelten. |
| [!UICONTROL Status] | Verwenden Sie diese Option, um die Liste nach Regelstatus (`Active` oder `Inactive`) zu filtern. |

{style="table-layout:auto"}

## Regelpriorität

Es kann immer mehrere aktive Regeln geben, die ausgelöst werden können, um verwandte Produkte, Upsell und Crosssell anzuzeigen. Die Priorität jeder Regel bestimmt die Reihenfolge, in der die Produkte auf der Seite angezeigt werden. Der Wert kann auf eine beliebige Ganzzahl festgelegt werden, wobei `1` die höchste Priorität hat.

Die Anzahl der Produkt-IDs, die in eine Produktbeziehungsregel aufgenommen werden können, wird durch den `Result Limit` bestimmt, der maximal 20 aufweist. Der `Result Limit`-Wert wird zusammen mit dem `Configurable Maximum` für die spezifische regelbasierte Produktwerbung zum `Real Limit` und bestimmt die tatsächliche Anzahl der übereinstimmenden Produkte, die in der Liste angezeigt werden können.

[Ergebnis-Limit] + [konfigurierbares Maximum] = [echtes Limit]

Angenommen, Sie haben drei Regeln mit der Priorität `1`, `2` und `3`.

- Es werden zwei übereinstimmende Produkte für _Regel 1_ zurückgegeben, sechs übereinstimmende Produkte für _Regel 2_ und 20 übereinstimmende Produkte für _Regel 3_.
- In der -Konfiguration ist der _[!UICONTROL Maximum Number of Products for Related Products List]_&#x200B;auf `6` festgelegt.

  | Regeln | Priorität | Übereinstimmende Produkte |
  |---|---|-----|
  | Artikel 1 | `1` | `2` |
  | Regel 2 | `2` | `6` |
  | Artikel 3 | `3` | `20` |

Wenn die erste Regel mehr übereinstimmende Produkte zurückgibt, als durch das _konfigurierbare Maximum_ zulässig sind, aber weniger als das _echte Limit_, werden die übereinstimmenden Produkte aus den anderen Regeln verwendet (in der Reihenfolge der Priorität), bis das _echte Limit_ erreicht ist.

Mit Priorität können die von (Regel _) zurückgegebenen passenden Produkte_ verwendet werden, um alle 26 verfügbaren Slots zu füllen. Da Regel 1 nur zwei übereinstimmende Produkte zurückgibt, ist noch Platz für 24 weitere. _Regel 2_ hat die nächsthöhere Priorität und gibt sechs weitere übereinstimmende Produkte zurück. Inzwischen stehen 18 Slots zur Verfügung. _Regel 3_ hat die nächste Prioritätsstufe, mit genügend passenden Produkten, um die restlichen 18 Slots zu füllen. Wenn alle verfügbaren Slots gefüllt sind, und abhängig vom eingestellten Rotationsmodus, können Produkte innerhalb jeder Priorität nach ID gemischt oder sortiert und dann auf das konfigurierbare obere Limit reduziert werden. In diesem Fall erscheinen die restlichen sechs Produkte im Geschäft.

>[!NOTE]
>
>Ausgewählte Produkte werden unabhängig vom Rotationsmodus immer vor den regelbasierten Produkten angezeigt.

## Konfigurieren von regelbasierten Produktbeziehungen

Das Verhalten von Produktbeziehungsregeln und die Anzeige übereinstimmender Produkte werden durch die Konfigurationseinstellungen bestimmt. Diese Einstellungen bestimmen, wie viele der Produkte, die der Regel entsprechen, angezeigt werden können und in welcher Reihenfolge sie angezeigt werden.

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im Bedienfeld auf der linken Seite **[!UICONTROL Catalog]** und wählen Sie darunter **[!UICONTROL Catalog]** aus.

1. Erweitern Sie ![Erweiterung](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Rules-Based Product Relations]** .

   ![Katalogkonfiguration - Regelbasierte Produktbeziehungen](../configuration-reference/catalog/assets/catalog-rule-based-product-relations.png){width="600" zoomable="yes"}

1. Geben Sie die **[!UICONTROL Maximum Number of Products in the Related Products List]** ein.

1. Legen Sie **[!UICONTROL Show Related Products]** auf eine der folgenden Einstellungen fest:

   - `Both Selected and Rule Based`
   - `Selected Only`
   - `Rule-Based Only`

1. Legen Sie **[!UICONTROL Rotation Mode for Products in Related Product List]** auf eine der folgenden Einstellungen fest:

   - `By Priority, Then by ID`
   - `By Priority, Then Random`
   - `Weighted Random`

1. Gehen Sie wie folgt vor, um die Crosssell-Produkteinstellungen abzuschließen:

   - Geben Sie die **[!UICONTROL Maximum Number of Products in the Cross-Sell Product List]** ein.

   - Legen Sie **[!UICONTROL Show Cross-Sell Products]** auf eine der folgenden Einstellungen fest:

      - `Both Selected and Rule Based`
      - `Selected Only`
      - `Rule-Based Only`

   - Legen Sie **[!UICONTROL Rotation Mode for Products in Cross-Sell Product List]** auf eine der folgenden Einstellungen fest:

      - `By Priority, Then by ID`
      - `By Priority, Then Random`
      - `Weighted Random`

1. Gehen Sie wie folgt vor, um die Upsell-Produkteinstellungen abzuschließen:

   - Geben Sie die **[!UICONTROL Maximum Number of Products in the Upsell Product List]** ein.

   - Legen Sie **[!UICONTROL Show Upsell Products]** auf eine der folgenden Einstellungen fest:

      - `Both Selected and Rule Based`
      - `Selected Only`
      - `Rule-Based Only`

   - Legen Sie **[!UICONTROL Rotation Mode for Products in Upsell Product List]** auf eine der folgenden Einstellungen fest:

      - `By Priority, Then by ID`
      - `By Priority, Then Random`
      - `Weighted Random`

1. Klicken Sie abschließend auf **[!UICONTROL Save Config]**.

### Drehungsmodi

| Modus | Beschreibung |
|---|---|
| [!UICONTROL By Priority, Then by ID] | Die Produkte werden nach Priorität sortiert und dann innerhalb jeder Priorität nach ID neu angeordnet. Produkte aus Regeln mit niedrigerer Priorität werden nur angezeigt, wenn sie keine Produkte mehr aus Regeln mit höherer Priorität haben, um die verfügbaren Slots zu füllen. |
| [!UICONTROL By Priority, Then Random] | Die Produkte werden nach Priorität sortiert und innerhalb jeder Priorität randomisiert. Produkte aus Regeln mit niedrigerer Priorität werden nur angezeigt, wenn sie keine Produkte mehr aus Regeln mit höherer Priorität haben, um die verfügbaren Slots zu füllen. |
| [!UICONTROL Weighted Random] | Produkte werden so randomisiert, dass Produkte, die zu einer Regel mit höherer Priorität gehören, eine höhere Wahrscheinlichkeit haben, zu erscheinen als diejenigen, die zu einer Regel mit niedrigerer Priorität gehören. Die Produkte werden dann auf das konfigurierbare Limit reduziert und nach Priorität neu gruppiert. Dieser Modus bietet die Möglichkeit, dass Produkte mit niedrigerer Priorität manchmal auch dann angezeigt werden, wenn die verbleibenden Slots mit Produkten aus einer Regel mit höherer Priorität gefüllt werden könnten |

{style="table-layout:auto"}

## Real-Time CDP-Zielgruppen verwenden, um über zugehörige Produktregeln zu informieren

>[!NOTE]
>
>Diese Funktion befindet sich in der Betaphase. Wenn Sie am Beta-Programm teilnehmen möchten, senden Sie eine Anfrage an [dataconnection@adobe.com](mailto:dataconnection@adobe.com).


Erfahren Sie, wie [&#x200B; Real-Time CDP](../customers/audience-activation.md)Zielgruppen in Ihrer Adobe Commerce-Instanz aktivieren, um Informationen zu verwandten Produktregeln zu erhalten.
