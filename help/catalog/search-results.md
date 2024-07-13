---
title: Suchergebnisse
description: Erfahren Sie, wie Sie konfigurieren können, wie Ihre Produkte den Suchkriterien entsprechen, die in das Feld "Schnellsuche"oder in das Formular "Erweiterte Suche"eingegeben wurden.
exl-id: c721fb3b-ee31-4d2b-b4ea-9ae2c80aa800
feature: Catalog Management, Search
source-git-commit: 4b2e1dd87a39c9be1adc49d867e44d306a969854
workflow-type: tm+mt
source-wordcount: '887'
ht-degree: 0%

---

# Suchergebnisse

>[!NOTE]
>
>Auf dieser Seite wird die Standardsuchfunktion beschrieben, die von der [Live-Suche](https://experienceleague.adobe.com/docs/commerce-merchant-services/live-search/overview.html) abweichen kann.

Die Liste _Suchergebnisse_ enthält alle Produkte, die den im Feld &quot;Schnellsuche&quot;oder im Formular &quot;Erweiterte Suche&quot;eingegebenen Suchkriterien entsprechen. Jede Produktliste im Katalog hat im Wesentlichen die gleichen Steuerelemente. Der einzige Unterschied besteht darin, dass einer das Ergebnis einer Suchabfrage ist und der andere Unterschied das Ergebnis von [Navigation](navigation.md).

Die Ergebnisse können entweder als Raster oder Liste formatiert und nach einer Auswahl von Attributen sortiert werden. Paginierungskontrollen werden angezeigt, wenn mehr Produkte vorhanden sind, als auf die Seite passen. Verwenden Sie diese Steuerelemente, um von einer Seite zur nächsten zu wechseln. Die Anzahl der Datensätze pro Seite wird durch die Catalog Frontend-Konfiguration bestimmt. Weitere Informationen finden Sie unter [Produktlisten](navigation-product-listings.md).

Mit **Elasticsearch**:

- Es gibt keine native Unterstützung für die Suche durch das Suffix. Beispielsweise gibt die Suche nach SKU möglicherweise nicht das erwartete Ergebnis zurück, wenn der Suchbegriff nur den Endteil der SKU enthält.
- Es gibt native Unterstützung für die Suche nach dem Präfix (Teilsuche nach Keywords) nur für die Produktattribute `name` und `sku`. Alle anderen Produktattribute werden vom gesamten Suchbegriff mit dem genauen Abgleich gesucht.
- Die Suchergebnisse für die Produktattribute `name` und `sku` basieren auf der Relevanz, nicht auf der exakten Übereinstimmung. Die relevantesten Übereinstimmungen wie ein genau übereinstimmender _Produktname_ oder _SKU_ werden zuerst aufgelistet. Um nach einer exakten Übereinstimmung zu suchen, kann der Kunde doppelte Anführungszeichen in der Suchabfrage verwenden. Eine Suchanfrage vom Typ `WSH12-32-Red` kann beispielsweise mehrere Produkte zurückgeben, die nach Relevanz sortiert sind. Eine Suchanfrage vom Typ `"WSH12-32-Red"` gibt jedoch nur ein Produkt zurück, bei dem der Wert **_genau_** mit `sku` übereinstimmt.

![Suchergebnisse mit Paginierungssteuerelementen](./assets/storefront-search-results-shorts.png){width="700" zoomable="yes"}

>[!IMPORTANT]
>
>Aufgrund der Ankündigung zum Ende der Unterstützung für Elasticsearch 7 vom August 2023 wird empfohlen, dass alle Adobe Commerce-Kunden zur OpenSearch 2.x-Suchmaschine migrieren. Informationen zur Migration Ihrer Suchmaschine während der Produktaktualisierung finden Sie unter [Migration zu OpenSearch](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/prepare/opensearch-migration.html) im _Upgrade-Handbuch_.

## Keyword-Zuordnung zum Erweitern der Suchergebnisse

Diese Technik verwendet ein -Attribut, um eine schlüsselwortbasierte Verknüpfung zwischen zwei Produkten zu erstellen, sodass bei einer Suche nach einem der beiden Produkte Ergebnisse für beide Produkte zurückgegeben werden. Sie können die Keyword-Zuordnung verwenden, um ein Produkt in Suchergebnissen zu bewerben, wenn es andernfalls nicht angezeigt würde.

![Suchergebnisse mit Keyword-Zuordnung](./assets/storefront-search-results-extended.png){width="700" zoomable="yes"}

Im folgenden Beispiel wird die Keyword-Zuordnung basierend auf der SKU verwendet. Wenn eine der SKU in das Suchfeld eingegeben wird, werden beide Produkte in den Ergebnissen angezeigt. Die SKUs der folgenden konfigurierbaren Produkte werden anstelle der SKUs von Produktvarianten zugeordnet:

- Montana Wind Jacket (MJ03)
- Chaz Kangaroo Hoodie (MH01)

### Schritt 1: Attribut erstellen

1. Öffnen Sie in der Liste &quot;_[!UICONTROL Products]_&quot;den Ordner &quot;`Montana Wind Jacket`&quot;(MJ03) im Bearbeitungsmodus.
1. Klicken Sie in der oberen rechten Ecke auf **[!UICONTROL Add Attribute]**.
1. Klicken Sie auf der Seite _Attribut auswählen_ auf **[!UICONTROL Create New Attribute]**.
1. Füllen Sie die Attributeigenschaften wie folgt aus:

   **[!UICONTROL Attribute Properties]**

   - [!UICONTROL Attribute Label] - `Search Keywords`
   - [!UICONTROL Catalog Input Type for Store Owner] - `Text Field`

   **[!UICONTROL Advanced Attribute Properties]**

   - [!UICONTROL Add to Column Options] - `Yes` (Standard)
   - [!UICONTROL Use in Filter Options] - `Yes` (Standard)

   **[!UICONTROL Storefront Properties]**

   - [!UICONTROL Use in Search] - `Yes`
   - [!UICONTROL Visible on Catalog Pages in the Storefront] - `No`
   - [!UICONTROL Used in Product Listings] - `No`

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save Attribute]**.

   Das Attribut wird dem Attributsatz für das Produkt hinzugefügt.

### Schritt 2: Zuordnen des ersten Produkts

1. Scrollen Sie auf der Seite mit den Produkteinstellungen nach unten und erweitern Sie den Abschnitt _[!UICONTROL Attributes]_.
1. Geben Sie im Feld **[!UICONTROL Search Keywords]** die SKU `MH01` ein, die diesem Produkt zugeordnet werden soll.

   Sie können mehrere SKUs eingeben, die durch ein Leerzeichen im Feld Suchbegriffe getrennt sind. In diesem Beispiel wird nur einer eingegeben.

   ![Abschnitt &quot;Attribute&quot;mit Suchbegriff](./assets/search-keywords-attribute.png){width="600" zoomable="yes"}

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save]**.
1. Gehen Sie zu **[!UICONTROL System]** > _[!UICONTROL Tools]_>**[!UICONTROL Cache Management]**und aktualisieren Sie die **[!UICONTROL Page Cache]**.

### Schritt 3: Zuordnen des zweiten Produkts

1. Öffnen Sie in der Liste &quot;_[!UICONTROL Products]_&quot;den Ordner &quot;`Chaz Kangaroo Hoodie`&quot;(MH01) im Bearbeitungsmodus.
1. Scrollen Sie nach unten und erweitern Sie den Abschnitt **[!UICONTROL Attributes]** .
1. Geben Sie im Feld **[!UICONTROL Search Keywords]** die SKU für das andere Produkt ein, `MJ03`.
1. Klicken Sie auf **[!UICONTROL Save]**.
1. Gehen Sie zu **[!UICONTROL System]** > _[!UICONTROL Tools]_>**[!UICONTROL Cache Management]**und aktualisieren Sie die **[!UICONTROL Page Cache]**.

### Schritt 4: Testen Sie es im Storefront.

1. Wechseln Sie zur Storefront und geben Sie im Feld _Schnellsuche_ den Wert `MJ03` ein.
1. Stellen Sie sicher, dass beide Produkte in der Liste der Suchergebnisse zurückgegeben werden.

## Gewichtete Suche

Produktattribute, die für die Katalogsuche aktiviert sind, können eine Gewichtung erhalten, um ihnen einen höheren Wert in den Suchergebnissen zu geben. Attribute mit einer höheren Gewichtung werden vor Attributen mit einer geringeren Gewichtung zurückgegeben. Wenn beispielsweise zwei Attribute im System vorhanden sind, _Farbe_ mit einer Suchgewichtung von 3 und _Beschreibung_ mit einer Suchgewichtung von 1. Bei einer Suche nach dem Wort _red_ wird oben in den Suchergebnissen eine Liste von Produkten mit dem Farbattributwert `red` zurückgegeben und es werden Produkte mit Beschreibungen zurückgegeben, die das Wort _red_ am unteren Rand der Suchergebnisse enthalten. In diesem Beispiel hat das Attribut `color` eine größere definierte Gewichtung als das Attribut `description`.

>[!IMPORTANT]
>
>Die Sortierung nach Relevanz wird durch **_multiple_** -Kriterien und -Beziehungen zwischen ihnen **_gleichzeitig_** beeinflusst. [!UICONTROL Search Weight] ist nur eines dieser Kriterien. Dies bedeutet, dass Attribute mit geringerer Suchgewichtung manchmal immer noch eine größere Relevanz haben als Attribute mit höherer Suchgewichtung. Andere Kriterien können die Anzahl der Übereinstimmungen in einem beliebigen Attribut, die Position des gefundenen Suchbegriffs und die gesamte Textstruktur vor und nach einem Suchbegriff umfassen.

**_So legen Sie die Suchgewichtseigenschaften eines Attributs fest:_**

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Product]**.

1. Suchen Sie das Attribut in der Liste und öffnen Sie es im Bearbeitungsmodus.

1. Wählen Sie im linken Bereich **[!UICONTROL Storefront Properties]** aus und gehen Sie wie folgt vor:

   - Um das Attribut in Suchabfragen einzubeziehen, setzen Sie **[!UICONTROL Use in Search]** auf `Yes`.

   - Um den Suchwert des Attributs festzulegen, setzen Sie **[!UICONTROL Search Weight]** auf eine Zahl zwischen 1 und 10, wobei `10` die höchste Priorität hat. Wenn kein Wert eingegeben wird, wird für alle Attribute standardmäßig eine Suchgewichtung von `1` verwendet.

   ![Suchgewichtung](./assets/search-weight.png){width="600" zoomable="yes"}

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save Attribute]**.
