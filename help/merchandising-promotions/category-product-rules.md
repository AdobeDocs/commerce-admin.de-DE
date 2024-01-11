---
title: Kategorieregeln für Merchandising
description: Erfahren Sie, wie Sie eine Regel erstellen, um die Produktauswahl anhand eines Bedingungssatzes dynamisch zu ändern.
exl-id: 765b863a-bb83-418b-9fca-ef0a148b09eb
feature: Categories, Merchandising
source-git-commit: 50951e5aae51067cdba2d8b50c1e530c7f79007a
workflow-type: tm+mt
source-wordcount: '1081'
ht-degree: 0%

---

# Kategorieregeln für Merchandising

{{ee-feature}}

Kategorieregeln ändern die Produktauswahl dynamisch anhand eines Bedingungssatzes. Jede Kategorie kann nur eine Kategorieregel enthalten, obwohl die einzelne Regel mehrere Bedingungen haben kann. Sie können beispielsweise eine Kategorieregel für eine bestimmte Marke erstellen. Produkte derselben Marke werden automatisch der Liste hinzugefügt, auch wenn sie nicht derselben Kategorie zugeordnet sind. Sie können dem Ausdruck beliebig viele Bedingungen hinzufügen, um die Produkte zu beschreiben, die Sie einbeziehen möchten.

>[!TIP]
>
>Bei der Einrichtung von Kategorieregeln werden die Produkte _sortiert_, _passend_, _assigned_, und _nicht zugewiesen_ gemäß dieser Regel **_only_** wenn diese Kategorie gespeichert wird. Wenn Sie beispielsweise ein Produkt zum Katalog hinzufügen und es gemäß der Regel zuweisen möchten, müssen Sie **muss jede Kategorie neu schreiben** festgelegt ist, um Produkte anhand der Regel abzugleichen. Außerdem, wenn der Status eines Produktbestands in `In Stock` oder `Out of Stock` und die Erzeugnisse der Kategorie _sortiert_ gemäß **[!UICONTROL Automatic Sorting]** Regel, müssen Sie auf **[!UICONTROL Save Category]**.

Jede Bedingung besteht aus einem Attribut, einem Wert und einem logischen Operator. Nur Attribute mit _[[!UICONTROL Use in Product Listing]](../catalog/attribute-product-create.md)_Eigenschaft festgelegt auf `Yes` kann in Kategorieregeln verwendet werden. Sie müssen diese Eigenschaft für das -Attribut festlegen, wenn Sie ein Attribut verwenden möchten, das nicht in Produktlisten enthalten ist. Datumsattribute werden zwar nicht unterstützt, Sie können aber die Attribute Erstellungsdatum oder Änderungsdatum verwenden, um ein Datum oder einen Datumsbereich zu definieren. Um beispielsweise nur Produkte einzubeziehen, die in der letzten Woche erstellt wurden, setzen Sie &quot;Erstellungsdatum&quot;auf den Wert von `<7`.

>[!NOTE]
>
>Konfigurieren Sie jedes Attribut, das in der Regel als [_smart_ attribute](smart-attributes-configure.md).

![Kategorieproduktregel](../catalog/assets/category-product-rule-with-stock.png){width="600" zoomable="yes"}

Kategorieproduktregeln können die Zuweisung bestimmter Produkte zu Kategorien beschleunigen, basierend auf Bedingungen, die bestimmen, welche Produkte in der Kategorie erscheinen. Die &quot;Smart&quot;-Attribute, die mit Kategorieproduktregeln verwendet werden können, werden im Abschnitt [Visual Merchandiser](visual-merchandiser.md) Konfiguration.

>[!NOTE]
>
>Seien Sie beim Anwenden einer Kategorieproduktregel vorsichtig, da alle Produkte, die die Bedingung nicht erfüllen, aus der Kategorie entfernt werden. Wenn Sie beispielsweise eine Regel erstellen, die nur violette Tankoberflächen enthält, werden alle anderen Tankoberflächen aus der Kategorie entfernt.

## Schritt 1: Konfigurieren Sie die _smart_ attributes

1. Stellen Sie für jedes Attribut, das in der Regel verwendet werden soll, sicher, dass die [[!UICONTROL Use in Product Listing]](../catalog/product-attributes.md) storefront property set to `Yes`.

   >[!NOTE]
   >
   >Vergewissern Sie sich, dass das ausgewählte Attribut KEIN Multiselect ist. _[!UICONTROL Input Type]_.

1. Führen Sie die [Konfiguration](smart-attributes-configure.md) zur Identifizierung _smart_ -Attribut, das mit Visual Merchandiser verwendet werden soll.

## Schritt 2: Erstellung der Kategorieregel

1. Öffnen Sie in der Kategorienstruktur die zu bearbeitende Kategorie.

1. Im **[!UICONTROL Products in Category]** Abschnitt, festlegen **[!UICONTROL Match products by rule]** nach `Yes`.

   Die automatischen Sortierungs- und Bedingungsoptionen werden angezeigt.

1. Klicks **[!UICONTROL Add Condition]**.

1. Wählen Sie die **[!UICONTROL Attribute]** Dies ist die Grundlage der Bedingung.

1. Satz **[!UICONTROL Operator]** auf einen der folgenden Werte zu:

   - `Equal`
   - `Not equal`
   - `Greater than`
   - `Greater than or equal to`
   - `Less than`
   - `Less than or equal to`
   - `Contains`

1. Geben Sie die **[!UICONTROL Value]** , der abgeglichen werden soll.

   ![Bedingung zur Kategorieregel hinzufügen](../catalog/assets/category-rule-create.png){width="500"}

1. Wiederholen Sie diesen Vorgang für jedes Attribut, das zur Beschreibung der zu erfüllenden Bedingungen erforderlich ist.

   Um beispielsweise Produkte abzugleichen, die vor 7 bis 30 Tagen erstellt wurden, gehen Sie wie folgt vor:

   - Satz **[!UICONTROL Date Created]** nach `Less than 30`.

   - Satz **[!UICONTROL Logic]** nach `AND`.

     >[!NOTE]
     >
     >Wenn Sie `AND`, gilt die Regel für Produkte, bei denen alle Bedingungen erfüllt sind. Auswählen `OR`, gilt sie für Produkte, bei denen mindestens eine Bedingung erfüllt ist.

   - Satz **[!UICONTROL Date Modified]** nach `Greater than 7`.

1. Um eine Sortierreihenfolge automatisch auf die dynamisch generierte Produktliste anzuwenden, legen Sie **[!UICONTROL Automatic Sorting]**.

   ![Automatische Sortierung](./assets/automatic-sorting-field.png){width="600" zoomable="yes"}

   Optionen für Sortierreihenfolge werden global definiert und basierend auf aktuellen Bedingungen angewendet. Sie können keine andere Sortierreihenfolge für die Website-, Store- oder Store-Ansichtsebene festlegen.

   | Sortieroption | Beschreibung |
   |-----------| -----------|
   | [!UICONTROL Stock quantity] | Sortieren nach Lager, von oben oder unten: `Move low stock to top` oder `Move out of stock to bottom` |
   | [!UICONTROL Special price] | Sortieren nach Preis, von oben oder unten: `Special price to top` oder `Special price to bottom` |
   | [!UICONTROL New Products] | Neueste Produkte auflisten: `Newest products first` |
   | [!UICONTROL Color] | Sortieren Sie alphabetisch nach Farbe: `Sort by color` |
   | [!UICONTROL Product Names] | Sortieren Sie nach Namen in auf- oder absteigender Reihenfolge: `Name A - Z` oder `Name Z -A` |
   | [!UICONTROL SKU] | Sortieren nach SKU in auf- oder absteigender Reihenfolge: `SKU: Ascending` oder `SKU: Descending` |
   | [!UICONTROL Price] | Sortieren nach Preis in auf- oder absteigender Reihenfolge: `Price: High to low` oder `Price: Low to high` |

   {style="table-layout:auto"}

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save Category]**.

>[!NOTE]
>
>Beim Einrichten einer Kategorieregel werden die Produkte zugeordnet und der Regel beim Speichern der Kategorie zugewiesen. Wenn Sie ein Produkt zum Katalog hinzufügen und in die Regel einbeziehen möchten, müssen Sie jede Kategorie erneut speichern, die so eingestellt ist, dass Produkte nach Regel übereinstimmen. Dadurch wird sichergestellt, dass das neue Produkt einbezogen wird.

### Menüoptionen

- **[!UICONTROL Match products by rule]** - Bestimmt, ob die Liste der Produkte in der Kategorie von einer Kategorieregel dynamisch generiert wird. Optionen: `Yes` / `No`

- **[!UICONTROL Automatic Sorting]** - wendet automatisch eine Sortierreihenfolge auf die Liste der Kategorieprodukte an. Optionen: `None`, `Move low stock to top`, `Move low stock to bottom`, `Special price to top`, `Special price to bottom`, `Newest products first`, `Sort by color`, `Name: A - Z`, `Name: Z - A`, `SKU: Ascending`, `SKU: Descending`, `Price: High to Low`, und `Price: Low to High`

  >[!NOTE]
  >
  >Wenn Sie über ein konfigurierbares Produkt mit untergeordneten Produkten verfügen, wird der übergeordnete Produktbestand auf der Grundlage der kombinierten Gesamtzahl der untergeordneten Produktvorräte berechnet. Betrachten Sie ein Beispiel mit einem konfigurierbaren Produkt. _Proteus Fitness Shirt_ mit orangefarbenen, roten und gelben Kinderprodukten mit jeweils unterschiedlichen Lagerbeständen. Der übergeordnete Produktbestand wird auf der Grundlage des Gesamtbestands an orangefarbenen, roten und gelben untergeordneten Produkten berechnet. Mit dem `Move low stock to top` berechnet er den Bestand der Mutterprodukte, indem er alle zum Verkauf stehenden untergeordneten Produkte kombiniert und entsprechend sortiert.

- **[!UICONTROL Add Condition]** - Fügt der Regel eine weitere Bedingung hinzu.

- **[!UICONTROL Attribute]** - Bestimmt das Attribut, das als Grundlage für die Bedingung verwendet wird. Optionen:

  | Option | Beschreibung |
  | ------ | ----------- |
  | `Clone Category ID(s)` | Dynamisches Klonen von Produkten ohne Sortierung und Reihenfolge aus mehreren Kategorien basierend auf Kategorie-ID. |
  | `Color` | Umfasst farbbasierte Produkte. |
  | `Date Created (days ago)` | Umfasst Produkte basierend auf der Anzahl der Tage seit dem Hinzufügen der Produkte zum Katalog. |
  | `Date Modified (days ago)` | Umfasst Produkte auf der Grundlage der Anzahl der Tage seit der letzten Änderung der Produkte. |
  | `Name` | Umfasst Produkte, die auf dem Produktnamen basieren. |
  | `Price` | Enthält Produkte, die auf dem Preis basieren. Dieses Attribut gilt nicht für konfigurierbare Produkte, da sie keinen eigenen Preis haben. |
  | `Quantity` | Umfasst Produkte auf der Basis der Lagermenge. |
  | `SKU` | Enthält Produkte, die auf der SKU basieren. |

  {style="table-layout:auto"}

  >[!NOTE]
  >
  >Die Menge eines konfigurierbaren Produkts mit untergeordneten Optionen wird durch Kombination aller verkaufbaren untergeordneten Produktmengen berechnet. Betrachten Sie ein Beispiel mit einem konfigurierbaren Produkt. _Grundlegender Fitnessbereich_ mit lilafarbenen, roten und gelben Farboptionen und unterschiedlichen Mengen. In diesem Fall ist die Menge des übergeordneten Produkts (Basis-Fitness-Tank) die verkäufliche Menge der lilafarbenen, roten und gelben untergeordneten Produkte.

- **[!UICONTROL Operator]** - Gibt den Operator an, der auf den Attributwert angewendet wird, um die Bedingung zu erfüllen. Wenn kein Benutzer angegeben ist, `Equal` wird als Standard verwendet. Optionen: `Equal`, `Not equal`, `Greater than`, `Greater than or equal to`, `Less than`, `Less than or equal to`, und `Contains`

- **[!UICONTROL Value]** - Gibt den Wert an, den das Attribut aufweisen muss, um die Bedingung zu erfüllen.

- **[!UICONTROL Logic]** - Die Spalte &quot;Logik&quot;dient zur Definition mehrerer Bedingungen und wird nur angezeigt, wenn eine andere Bedingung hinzugefügt wird. Die Benutzer befolgen die Rangregeln für MySQL [boolesche Operatoren](https://dev.mysql.com/doc/refman/8.0/en/operator-precedence.html). Optionen: `AND` / `OR`
