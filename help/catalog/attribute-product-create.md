---
title: Produktattribute erstellen und löschen
description: Erfahren Sie mehr über das Erstellen und Entfernen von Produktattributen, mit denen bestimmte Eigenschaften der Produkte in Ihrem Katalog beschrieben werden.
exl-id: fd0e5d5b-a917-4e55-8ec2-7ebb040d3d06
feature: Catalog Management, Products
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '1159'
ht-degree: 0%

---

# Produktattribute erstellen und löschen

Sie können Attribute erstellen, während Sie an einem Produkt arbeiten, oder aus der _[!UICONTROL Product Attributes]_Seite. Die folgenden Schritte zeigen, wie Attribute aus dem_[!UICONTROL Stores]_ Menü.

## Schritt 1: Grundlegende Attributeigenschaften beschreiben

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Product]**.

1. Klicken **[!UICONTROL Add New Attribute]**.

   ![Neue Attributeigenschaften](./assets/attribute-properties.png){width="600" zoomable="yes"}

1. Für **[!UICONTROL Default Label]**, geben Sie einen Titel ein, der das Attribut angibt.

1. Um den Typ des Eingabeditors zu bestimmen, der für die Dateneingabe verwendet wird, legen Sie **[!UICONTROL Catalog Input Type for Store Owner]** auf einen der folgenden Werte zu:

   | Eigenschaft | Beschreibung |
   |--- |--- |
   | `Text Field` | Ein einzeiliges Eingabefeld für Text. |
   | `Text Area` | Ein mehrzeiliges Eingabefeld für die Eingabe von Textabsätzen, z. B. eine Produktbeschreibung. Sie können den WYSIWYG-Editor verwenden, um den Text mit HTML-Tags zu formatieren, oder die Tags direkt in den Text eingeben. |
   | `Text Editor` | Ein voll funktionsfähiger Texteditor am Attributstandort. |
   | Datum | Zeigt einen Datumswert im [bevorzugtes Format](attributes-input-types.md#date-and-time-options) und [Zeitzone](../getting-started/store-details.md#locale-options). Datumswerte können aus einer Liste oder einem Kalender ausgewählt werden ( ![Kalendersymbol](../assets/icon-calendar.png) ). <br/><br/>**_Hinweis:_**Abhängig von Ihrer Systemkonfiguration_Admin _Benutzer können Datumsangaben direkt in ein Feld eingeben oder ein Datum aus dem Kalender oder der Liste auswählen. Informationen zum Festlegen von Datums- und Uhrzeitwerten finden Sie unter [Datums- und Uhrzeitoptionen](attributes-input-types.md#date-and-time-options). |
   | `Yes/No` | Zeigt eine Dropdownliste mit vordefinierten Optionen von `Yes` und `No`. |
   | `Dropdown` | Zeigt eine Dropdown-Liste mit Werten an, die nur eine Auswahl zulassen. Der Dropdown-Eingabetyp ist eine Schlüsselkomponente von [konfigurierbare Produkte](product-create-configurable.md). |
   | `Multiple Select` | Zeigt eine Dropdown-Liste mit Werten an, die mehrere Auswahlen akzeptieren. |
   | `Price` | Dieser Eingabetyp wird verwendet, um Preisfelder zu erstellen, die zusätzlich zu den vordefinierten Attributen verwendet werden: Preis, Sonderpreis, Statuspreis und Kosten. Die verwendete Währung wird durch Ihre Systemkonfiguration bestimmt. |
   | `Media Image` | Verbindet ein zusätzliches Bild mit einem Produkt, z. B. einem Produktlogo, Pflegeanleitungen oder Zutaten aus einem Lebensmitteletikett. Wenn Sie dem Attributsatz eines Produkts ein Medienbildattribut hinzufügen, wird es zu einem zusätzlichen Bildtyp, zusammen mit &quot;Base&quot;, &quot;Small&quot;und &quot;Thumbnail&quot;. Das Medienbildattribut kann aus dem [Storefront-Medienbrowser](catalog-images-video.md#storefront-media-browser). |
   | `Fixed Product Tax` | Ermöglicht die Definition [FPT-Raten](../stores-purchase/fixed-product-tax.md) basierend auf den Anforderungen Ihres Gebietsschemas. |
   | `Visual Swatch` | Zeigt ein Muster an, das die Farbe, Textur oder das Muster eines konfigurierbaren Produkts darstellt. A [visuelles Muster](swatches.md) kann mit einem hexadezimalen Farbwert gefüllt werden oder ein hochgeladenes Bild anzeigen, das die Farbe, das Material, die Textur oder das Muster der Option darstellt. |
   | `Text Swatch` | Eine textbasierte Darstellung einer konfigurierbaren Produktoption, die häufig für die Größe verwendet wird. [Textmuster](swatches.md#text-based-swatches) kann auch hexadezimale Farbwerte enthalten. |
   | `Page Builder` | Eine voll funktionsfähige [Page Builder](../page-builder/introduction.md) Arbeitsbereich am Attributstandort, der es erleichtert, ansprechende Inhalte zur Produktseite hinzuzufügen. |

   {style="table-layout:auto"}

1. Wenn Sie eine Optionsauswahl benötigen möchten, bevor der Kunde das Produkt erwerben kann, legen Sie **[!UICONTROL Values Required]** nach `Yes`.

1. Für [!UICONTROL Dropdown] und [!UICONTROL Multiple Select] Eingabetypen verwenden Sie folgende Schritte:

   - under _[!UICONTROL Manage Options]_klicken **[!UICONTROL Add Option]**.

   - Geben Sie den ersten Wert ein, der in der Liste angezeigt werden soll.

     Sie können einen Wert für den Administrator und eine Übersetzung des Werts für jede Store-Ansicht eingeben. Wenn Sie nur eine Store-Ansicht haben, können Sie nur den Admin-Wert eingeben, der auch für die Storefront verwendet wird.

   - Klicks **[!UICONTROL Add Option]** und wiederholen Sie den vorherigen Schritt für jede Option, die Sie in die Liste aufnehmen möchten.

   - Auswählen **[!UICONTROL Is Default]** , um die Option als Standardwert zu verwenden.

   ![Produktattribut - Verwaltungsoptionen](./assets/product-attribute-add-values-colors.png){width="600" zoomable="yes"}

## Schritt 2: Beschreibung der erweiterten Eigenschaften (falls erforderlich)

1. Eindeutige Eingabe **[!UICONTROL Attribute Code]** in Kleinbuchstaben und ohne Leerzeichen.

   ![Produktattribut - erweiterte Eigenschaften](./assets/product-attribute-advanced-attribute-properties.png){width="600" zoomable="yes"}

   Die verfügbaren Optionen hängen von der _[!UICONTROL Catalog Input Type for Store Owner]_-Einstellung.

1. Satz **[!UICONTROL Scope]** um anzugeben, wo in der [Store-Hierarchie](../getting-started/websites-stores-views.md) dass das Attribut verwendet werden kann.

1. Wenn Sie einen doppelten Werteeintrag verhindern möchten, legen Sie **[!UICONTROL Unique Value]** nach `Yes`.

1. Führen Sie für eingegebenen Eingabetypen einen Gültigkeitstest für alle in ein Textfeld eingegebenen Daten durch, indem Sie **[!UICONTROL Input Validation for Store Owner]** auf den Datentyp, den das Feld enthalten soll.

   Dieses Feld ist nicht für Eingabetypen mit ausgewählten Werten verfügbar. Der Test kann Folgendes validieren:

   - `Decimal Number`
   - `Integer Number`
   - `Email`
   - `URL`
   - `Letters`
   - `Letters (a-z, A-Z) or Numbers (0-9)`

   ![Eingabevalidierung](./assets/product-attribute-input-validation.png){width="400"}

1. So fügen Sie dieses Attribut zum [Liste der Produkte](products-list.md), legen Sie die folgenden Optionen auf `Yes`.

   - **Zu Spaltenoptionen hinzufügen** - Umfasst das Attribut als Spalte im _[!UICONTROL Products]_Liste.
   - **Verwenden in Filteroptionen** - Fügt der Spaltenüberschrift im _[!UICONTROL Products]_Liste.

## Schritt 3: Feldbezeichnung eingeben

1. Wählen Sie in der linken Seitennavigation die Option **[!UICONTROL Manage Labels]**.

1. Geben Sie einen **[!UICONTROL Title]** als Beschriftung für das Feld verwendet werden.

   Wenn Ihr Store in verschiedenen Sprachen verfügbar ist, können Sie für jede Ansicht einen übersetzten Titel eingeben.

   ![Produktattribut - Titel verwalten](./assets/product-attribute-add-manage-titles.png){width="600" zoomable="yes"}

## Schritt 4: Beschreibung der Storefront-Eigenschaften

1. Wählen Sie in der linken Seitennavigation die Option **[!UICONTROL Storefront Properties]**.

   ![Produktattribute - Storefront-Eigenschaften](./assets/product-attribute-add-storefront-properties.png){width="600" zoomable="yes"}

   Die verfügbaren Optionen hängen von der _[!UICONTROL Catalog Input Type for Store Owner]_-Einstellung.

1. Wenn das Attribut für die Suche verfügbar sein soll, legen Sie **[!UICONTROL Use in Search]** nach `Yes`.

   - Legen Sie die **[!UICONTROL Search Weight]** -Wert zu bestimmen, wo das Element in den Suchergebnissen angezeigt wird: 1 (niedrigste Gewichtung) bis 10 (höchste Gewichtung).

   - Legen Sie die **[!UICONTROL Visible in Advanced Search]** nach Bedarf. Weitere Informationen finden Sie unter [Erweiterte Suche](search.md#advanced-search).

1. Um das -Attribut in den Produktvergleich einzubeziehen, legen Sie **[!UICONTROL Comparable on Storefront]** nach `Yes`.

1. Gehen Sie für Dropdown-Listen, mehrere Auswahl- und Preisfelder wie folgt vor:

   - Um das Attribut als Filter in der Navigation mit Ebenen zu verwenden, legen Sie **[!UICONTROL Use in Layered Navigation]** nach `Yes`.

   - Um das Attribut in der mehrstufigen Navigation auf Suchergebnisseiten zu verwenden, legen Sie **[!UICONTROL Use in Search Results Layered Navigation]** nach `Yes`.

   - Für **[!UICONTROL Position]** Geben Sie eine Zahl ein, um die relative Position des Attributs im Navigationsblock mit Ebenen anzugeben.

1. Um das Attribut in den Preisregeln zu verwenden, legen Sie **[!UICONTROL Use for Promo Rule Conditions]** nach `Yes`.

1. Damit der Text mit HTML formatiert werden kann, legen Sie **[!UICONTROL Allow HTML Tags on Frontend]** nach `Yes`.

   Durch diese Einstellung wird der WYSIWYG-Editor für das Feld verfügbar gemacht.

1. Um das Attribut auf der Produktseite einzubeziehen, legen Sie **[!UICONTROL Visible on Catalog Pages on Storefront]** nach `Yes`.

1. Nehmen Sie die folgenden Einstellungen vor, sofern sie von Ihrem Design unterstützt werden:

   - Um das -Attribut in Produktlisten aufzunehmen, legen Sie **[!UICONTROL Used in Product Listing]** nach `Yes`.

   - Um das Attribut als Sortierparameter für Produktlisten zu verwenden, legen Sie **[!UICONTROL Used for Sorting in Product Listing]** nach `Yes`.

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save Attribute]**.

## Schritt 5: Dem Attributsatz das erstellte Attribut zuweisen

Damit ein Attribut auf der Produkterstellungsseite sichtbar ist, fügen Sie es zu einem bestimmten Attributsatz hinzu.

1. Nachdem Sie die vorherigen Schritte ausgeführt haben, gehen Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Attribute Set]**.

1. Wählen Sie den benötigten Attributsatz in der Liste aus und öffnen Sie ihn im Bearbeitungsmodus.

1. Ziehen Sie das erstellte Attribut aus dem **[!UICONTROL Unassigned Attributes]** Liste zum entsprechenden Ordner im **Gruppen** Spalte.

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save]**.

## Attribute für konfigurierbare Produkte

Jedes Attribut, das als Dropdown-Liste mit Optionen für eine [konfigurierbares Produkt](product-create-configurable.md) muss die folgenden Eigenschaften aufweisen:

| Eigenschaft | Wert |
|----------|------ |
| Katalogeingabetyp für Store Owner | Dropdown |
| Anwendungsbereich | Global |

{style="table-layout:auto"}

## Attribut löschen

Wenn ein Attribut gelöscht wird, wird es aus allen zugehörigen Produkten und Attributsätzen entfernt. Systemattribute sind Teil der Kernfunktionalität Ihres Stores und können nicht gelöscht werden.

Bevor Sie ein Attribut löschen, stellen Sie sicher, dass es derzeit von keinem Produkt in Ihrem Katalog verwendet wird. Ob ein Attribut verwendet wird, können Sie einfach anhand der [Export](../systems/data-export.md) -Tool, um die Liste der Entitätsattribute des Produkts zu überprüfen. Wenn das Attribut nicht in der Liste enthalten ist, wird es von keinem Produkt im Katalog verwendet.

**_So löschen Sie ein Attribut:_**

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Product]**.

1. Suchen Sie das Attribut in der Liste und öffnen Sie es im Bearbeitungsmodus.

1. Klicken **[!UICONTROL Delete Attribute]**.

   ![Attribut löschen](./assets/attribute-delete.png){width="600" zoomable="yes"}

1. Klicken Sie bei Aufforderung zur Bestätigung auf **[!UICONTROL OK]**.
