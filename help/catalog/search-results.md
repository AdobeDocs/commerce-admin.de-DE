---
title: Suchergebnisse
description: Erfahren Sie, wie Sie konfigurieren können, wie Ihre Produkte den Suchkriterien entsprechen, die in das Feld "Schnellsuche"oder in das Formular "Erweiterte Suche"eingegeben wurden.
exl-id: c721fb3b-ee31-4d2b-b4ea-9ae2c80aa800
feature: Catalog Management, Search
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '820'
ht-degree: 0%

---

# Suchergebnisse

>[!NOTE]
>
>Auf dieser Seite werden die Standardsuchfunktionen beschrieben, die sich von [Live Search](https://experienceleague.adobe.com/docs/commerce-merchant-services/live-search/overview.html).

Die _Suchergebnisse_ enthält alle Produkte, die den Suchkriterien entsprechen, die im Feld Schnellsuche oder im Formular Erweiterte Suche eingegeben wurden. Jede Produktliste im Katalog hat im Wesentlichen die gleichen Steuerelemente. Der einzige Unterschied besteht darin, dass einer das Ergebnis einer Suchanfrage ist und der andere das Ergebnis von [Navigation](navigation.md).

Die Ergebnisse können entweder als Raster oder Liste formatiert und nach einer Auswahl von Attributen sortiert werden. Paginierungskontrollen werden angezeigt, wenn mehr Produkte vorhanden sind, als auf die Seite passen. Verwenden Sie diese Steuerelemente, um von einer Seite zur nächsten zu wechseln. Die Anzahl der Datensätze pro Seite wird durch die Catalog Frontend-Konfiguration bestimmt. Weitere Informationen finden Sie unter [Produktlisten](navigation-product-listings.md).

Mit **Elasticsearch**:

- Es gibt keine native Unterstützung für die Suche durch das Suffix. Beispielsweise gibt die Suche nach SKU möglicherweise nicht das erwartete Ergebnis zurück, wenn der Suchbegriff nur den Endteil der SKU enthält.
- Es gibt native Unterstützung für die Suche nach Präfix (Teilsuche nach Keywords) für `name` und `sku` nur Produktattribute. Alle anderen Produktattribute werden vom gesamten Suchbegriff mit dem genauen Abgleich gesucht.
- Suchergebnisse für `name` und `sku` Produktattribute basieren auf der Relevanz, nicht auf der exakten Übereinstimmung. Die relevantesten Übereinstimmungen, z. B. eine exakt übereinstimmende _Produktname_ oder _SKU_, werden zuerst aufgelistet. Um nach einer exakten Übereinstimmung zu suchen, kann der Kunde doppelte Anführungszeichen in der Suchabfrage verwenden. Beispiel: eine `WSH12-32-Red` Suchanfragen können mehrere Produkte zurückgeben, die nach Relevanz sortiert sind. Aber ein `"WSH12-32-Red"` Suchabfrage gibt nur ein Produkt mit **_just_** passend `sku`.

![Suchergebnisse mit Paginierungskontrollen](./assets/storefront-search-results-shorts.png){width="700" zoomable="yes"}

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

1. Im _[!UICONTROL Products]_Liste, öffnen Sie die `Montana Wind Jacket` (MJ03) im Bearbeitungsmodus.
1. Klicken Sie oben rechts auf **[!UICONTROL Add Attribute]**.
1. Im _Attribut auswählen_ Seite, klicken **[!UICONTROL Create New Attribute]**.
1. Füllen Sie die Attributeigenschaften wie folgt aus:

   **[!UICONTROL Attribute Properties]**

   - [!UICONTROL Attribute Label]  - `Search Keywords`
   - [!UICONTROL Catalog Input Type for Store Owner] - `Text Field`

   **[!UICONTROL Advanced Attribute Properties]**

   - [!UICONTROL Add to Column Options] - `Yes` (Standard)
   - [!UICONTROL Use in Filter Options] - `Yes` (Standard)

   **[!UICONTROL Storefront Properties]**

   - [!UICONTROL Use in Search] - `Yes`
   - [!UICONTROL Visible on Catalog Pages in the Storefront] - `No`
   - [!UICONTROL Used in Product Listings] - `No`

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save Attribute]**.

   Das Attribut wird dem Attributsatz für das Produkt hinzugefügt.

### Schritt 2: Zuordnen des ersten Produkts

1. Scrollen Sie auf der Seite mit den Produkteinstellungen nach unten und erweitern Sie die _[!UICONTROL Attributes]_Abschnitt.
1. Im **[!UICONTROL Search Keywords]** das SKU-Feld eingeben `MH01` , das diesem Produkt zugeordnet werden soll.

   Sie können mehrere SKUs eingeben, die durch ein Leerzeichen im Feld Suchbegriffe getrennt sind. In diesem Beispiel wird nur einer eingegeben.

   ![Abschnitt &quot;Attribute&quot;mit Suchbegriff](./assets/search-keywords-attribute.png){width="600" zoomable="yes"}

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save]**.
1. Navigieren Sie zu **[!UICONTROL System]** > _[!UICONTROL Tools]_>**[!UICONTROL Cache Management]**und aktualisieren Sie die **[!UICONTROL Page Cache]**.

### Schritt 3: Zuordnen des zweiten Produkts

1. Im _[!UICONTROL Products]_Liste, öffnen Sie die `Chaz Kangaroo Hoodie` (MH01) im Bearbeitungsmodus.
1. Scrollen Sie nach unten und erweitern Sie die **[!UICONTROL Attributes]** Abschnitt.
1. Im **[!UICONTROL Search Keywords]** das Feld SKU für das andere Produkt eingeben, `MJ03`.
1. Klicken **[!UICONTROL Save]**.
1. Navigieren Sie zu **[!UICONTROL System]** > _[!UICONTROL Tools]_>**[!UICONTROL Cache Management]**und aktualisieren Sie die **[!UICONTROL Page Cache]**.

### Schritt 4: Testen Sie es im Storefront.

1. Gehen Sie zur Storefront und geben Sie ein `MJ03` im _Schnellsuche_ ankreuzen.
1. Stellen Sie sicher, dass beide Produkte in der Liste der Suchergebnisse zurückgegeben werden.

## Gewichtete Suche

Produktattribute, die für die Katalogsuche aktiviert sind, können eine Gewichtung erhalten, um ihnen einen höheren Wert in den Suchergebnissen zu geben. Attribute mit einer höheren Gewichtung werden vor Attributen mit einer geringeren Gewichtung zurückgegeben. Wenn beispielsweise zwei Attribute im System vorhanden sind, _color_ mit einer Suchgewichtung von 3 und _description_ mit einer Suchgewichtung von 1. Eine Suche nach dem Wort _red_ gibt eine Liste von Produkten mit dem Farbattributwert `red` oben in den Suchergebnissen und gibt Produkte mit Beschreibungen zurück, die das Wort enthalten _red_ unten in den Suchergebnissen. In diesem Beispiel wird die `color` hat eine größere definierte Gewichtung als die `description` -Attribut.

**_So legen Sie die Suchgewichtseigenschaften eines Attributs fest:_**

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Product]**.

1. Suchen Sie das Attribut in der Liste und öffnen Sie es im Bearbeitungsmodus.

1. Wählen Sie im linken Bereich die Option **[!UICONTROL Storefront Properties]** und gehen Sie wie folgt vor:

   - Um das Attribut in Suchabfragen einzubeziehen, legen Sie **[!UICONTROL Use in Search]** nach `Yes`.

   - Um den Suchwert des Attributs festzulegen, legen Sie **[!UICONTROL Search Weight]** auf eine Zahl von 1 bis 10, wobei `10` hat die höchste Priorität. Wenn kein Wert eingegeben wird, wird für alle Attribute standardmäßig eine Suchgewichtung von `1`.

   ![Suchgewichtung](./assets/search-weight.png){width="600" zoomable="yes"}

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save Attribute]**.
