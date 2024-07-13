---
title: Produktattribute erstellen und löschen
description: Erfahren Sie mehr über das Erstellen und Entfernen von Produktattributen, mit denen bestimmte Eigenschaften der Produkte in Ihrem Katalog beschrieben werden.
exl-id: fd0e5d5b-a917-4e55-8ec2-7ebb040d3d06
feature: Catalog Management, Products
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '1166'
ht-degree: 0%

---

# Produktattribute erstellen und löschen

Sie können Attribute während der Arbeit an einem Produkt oder von der Seite _[!UICONTROL Product Attributes]_aus erstellen. Die folgenden Schritte zeigen, wie Sie Attribute über das Menü_[!UICONTROL Stores]_ erstellen.

## Schritt 1: Grundlegende Attributeigenschaften beschreiben

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Product]**.

1. Klicken Sie auf **[!UICONTROL Add New Attribute]**.

   ![Neue Attributeigenschaften](./assets/attribute-properties.png){width="600" zoomable="yes"}

1. Geben Sie für &quot;**[!UICONTROL Default Label]**&quot;eine Beschriftung ein, die das Attribut angibt.

1. Um den Typ des Eingabeditors zu bestimmen, der für die Dateneingabe verwendet wird, setzen Sie **[!UICONTROL Catalog Input Type for Store Owner]** auf einen der folgenden Werte:

   | Eigenschaft | Beschreibung |
   |--- |--- |
   | `Text Field` | Ein einzeiliges Eingabefeld für Text. |
   | `Text Area` | Ein mehrzeiliges Eingabefeld für die Eingabe von Textabsätzen, z. B. eine Produktbeschreibung. Sie können den WYSIWYG-Editor verwenden, um den Text mit HTML-Tags zu formatieren, oder die Tags direkt in den Text eingeben. |
   | `Text Editor` | Ein voll funktionsfähiger Texteditor am Attributstandort. |
   | Datum | Zeigt einen Datumswert im Format [Bevorzugtes Format](attributes-input-types.md#date-and-time-options) und [Zeitzone](../getting-started/store-details.md#locale-options) an. Datumswerte können aus einer Liste oder einem Kalender ausgewählt werden ( ![Kalendersymbol](../assets/icon-calendar.png) ). <br/><br/>**_Hinweis:_**Je nach Systemkonfiguration können Benutzer mit_Administrator _Daten direkt in ein Feld eingeben oder ein Datum aus dem Kalender oder der Liste auswählen. Informationen zum Festlegen von Datums- und Uhrzeitwerten finden Sie unter [Datums- und Uhrzeitoptionen](attributes-input-types.md#date-and-time-options). |
   | `Yes/No` | Zeigt eine Dropdownliste mit den vordefinierten Optionen `Yes` und `No` an. |
   | `Dropdown` | Zeigt eine Dropdown-Liste mit Werten an, die nur eine Auswahl zulassen. Der Dropdown-Eingabetyp ist eine Schlüsselkomponente von [konfigurierbaren Produkten](product-create-configurable.md). |
   | `Multiple Select` | Zeigt eine Dropdown-Liste mit Werten an, die mehrere Auswahlen akzeptieren. |
   | `Price` | Dieser Eingabetyp wird verwendet, um Preisfelder zu erstellen, die zusätzlich zu den vordefinierten Attributen verwendet werden: Preis, Sonderpreis, Statuspreis und Kosten. Die verwendete Währung wird durch Ihre Systemkonfiguration bestimmt. |
   | `Media Image` | Verbindet ein zusätzliches Bild mit einem Produkt, z. B. einem Produktlogo, Pflegeanleitungen oder Zutaten aus einem Lebensmitteletikett. Wenn Sie dem Attributsatz eines Produkts ein Medienbildattribut hinzufügen, wird es zu einem zusätzlichen Bildtyp, zusammen mit &quot;Base&quot;, &quot;Small&quot;und &quot;Thumbnail&quot;. Das Medienbild-Attribut kann aus dem [StoreFront-Media-Browser](catalog-images-video.md#storefront-media-browser) ausgeschlossen werden. |
   | `Fixed Product Tax` | Ermöglicht die Definition von [FPT-Raten](../stores-purchase/fixed-product-tax.md) anhand der Anforderungen Ihres Gebietsschemas. |
   | `Visual Swatch` | Zeigt ein Muster an, das die Farbe, Textur oder das Muster eines konfigurierbaren Produkts darstellt. Ein [visuelles Muster](swatches.md) kann mit einem hexadezimalen Farbwert gefüllt werden oder ein hochgeladenes Bild anzeigen, das die Farbe, das Material, die Textur oder das Muster der Option darstellt. |
   | `Text Swatch` | Eine textbasierte Darstellung einer konfigurierbaren Produktoption, die häufig für die Größe verwendet wird. [Textmuster](swatches.md#text-based-swatches) können auch hexadezimale Farbwerte enthalten. |
   | `Page Builder` | Ein voll funktionierender Arbeitsbereich für den [Seitenaufbau](../page-builder/introduction.md) am Attributstandort, der das Hinzufügen ansprechender Inhalte zur Produktseite erleichtert. |

   {style="table-layout:auto"}

1. Wenn Sie eine Optionsauswahl benötigen möchten, bevor der Kunde das Produkt erwerben kann, setzen Sie **[!UICONTROL Values Required]** auf `Yes`.

1. Gehen Sie für die Eingabetypen [!UICONTROL Dropdown] und [!UICONTROL Multiple Select] wie folgt vor:

   - Klicken Sie unter _[!UICONTROL Manage Options]_auf **[!UICONTROL Add Option]**.

   - Geben Sie den ersten Wert ein, der in der Liste angezeigt werden soll.

     Sie können einen Wert für den Administrator und eine Übersetzung des Werts für jede Store-Ansicht eingeben. Wenn Sie nur eine Store-Ansicht haben, können Sie nur den Admin-Wert eingeben, der auch für die Storefront verwendet wird.

   - Klicken Sie auf **[!UICONTROL Add Option]** und wiederholen Sie den vorherigen Schritt für jede Option, die Sie in die Liste aufnehmen möchten.

   - Wählen Sie **[!UICONTROL Is Default]** aus, um die Option als Standardwert zu verwenden.

   ![Produktattribut - Optionen verwalten](./assets/product-attribute-add-values-colors.png){width="600" zoomable="yes"}

## Schritt 2: Beschreibung der erweiterten Eigenschaften (falls erforderlich)

1. Geben Sie ein eindeutiges **[!UICONTROL Attribute Code]** in Kleinbuchstaben und ohne Leerzeichen ein.

   ![Produktattribut - Erweiterte Eigenschaften](./assets/product-attribute-advanced-attribute-properties.png){width="600" zoomable="yes"}

   Die verfügbaren Optionen hängen von der Einstellung _[!UICONTROL Catalog Input Type for Store Owner]_ab.

1. Legen Sie **[!UICONTROL Scope]** fest, um anzugeben, wo in Ihrer [Store-Hierarchie](../getting-started/websites-stores-views.md) das Attribut verwendet werden kann.

1. Wenn Sie einen doppelten Werteeintrag verhindern möchten, setzen Sie **[!UICONTROL Unique Value]** auf `Yes`.

1. Führen Sie für eingegebenen Eingabetypen einen Gültigkeitstest für alle in ein Textfeld eingegebenen Daten durch, indem Sie **[!UICONTROL Input Validation for Store Owner]** auf den Datentyp setzen, den das Feld enthalten soll.

   Dieses Feld ist nicht für Eingabetypen mit ausgewählten Werten verfügbar. Der Test kann Folgendes validieren:

   - `Decimal Number`
   - `Integer Number`
   - `Email`
   - `URL`
   - `Letters`
   - `Letters (a-z, A-Z) or Numbers (0-9)`

   ![Eingabevalidierung](./assets/product-attribute-input-validation.png){width="400"}

1. Um dieses Attribut zur Liste [Produkte](products-list.md) hinzuzufügen, setzen Sie die folgenden Optionen auf `Yes`.

   - **Zu Spaltenoptionen hinzufügen** - Umfasst das Attribut als Spalte in der Liste _[!UICONTROL Products]_.
   - **In Filteroptionen verwenden** - Fügt der Spaltenüberschrift in der Liste _[!UICONTROL Products]_ein Filtersteuerelement hinzu.

## Schritt 3: Feldbezeichnung eingeben

1. Wählen Sie im linken Navigationsbereich **[!UICONTROL Manage Labels]** aus.

1. Geben Sie eine **[!UICONTROL Title]** ein, die als Beschriftung für das Feld verwendet werden soll.

   Wenn Ihr Store in verschiedenen Sprachen verfügbar ist, können Sie für jede Ansicht einen übersetzten Titel eingeben.

   ![Produktattribut - Titel verwalten](./assets/product-attribute-add-manage-titles.png){width="600" zoomable="yes"}

## Schritt 4: Beschreibung der Storefront-Eigenschaften

1. Wählen Sie im linken Navigationsbereich **[!UICONTROL Storefront Properties]** aus.

   ![Produktattribute - Storefront-Eigenschaften](./assets/product-attribute-add-storefront-properties.png){width="600" zoomable="yes"}

   Die verfügbaren Optionen hängen von der Einstellung _[!UICONTROL Catalog Input Type for Store Owner]_ab.

1. Wenn das Attribut für die Suche verfügbar sein soll, setzen Sie **[!UICONTROL Use in Search]** auf `Yes`.

   - Stellen Sie den Wert **[!UICONTROL Search Weight]** ein, um zu steuern, wo das Element in den Suchergebnissen angezeigt wird: 1 (niedrigste Gewichtung) auf 10 (höchste Gewichtung).

   - Legen Sie den **[!UICONTROL Visible in Advanced Search]** nach Bedarf fest. Weitere Informationen finden Sie unter [Erweiterte Suche](search.md#advanced-search).

1. Um das Attribut in den Produktvergleich einzubeziehen, setzen Sie **[!UICONTROL Comparable on Storefront]** auf `Yes`.

1. Gehen Sie für Dropdown-Listen, mehrere Auswahl- und Preisfelder wie folgt vor:

   - Um das Attribut als Filter in der Navigation mit Ebenen zu verwenden, setzen Sie **[!UICONTROL Use in Layered Navigation]** auf `Yes`.

   - Um das Attribut in mehrschichtiger Navigation auf Suchergebnisseiten zu verwenden, setzen Sie **[!UICONTROL Use in Search Results Layered Navigation]** auf `Yes`.

   - Geben Sie für &quot;**[!UICONTROL Position]**&quot; eine Zahl ein, um die relative Position des Attributs im Navigationsblock mit Ebenen anzugeben.

1. Um das Attribut in den Preisregeln zu verwenden, setzen Sie **[!UICONTROL Use for Promo Rule Conditions]** auf `Yes`.

1. Damit der Text mit HTML formatiert werden kann, setzen Sie **[!UICONTROL Allow HTML Tags on Frontend]** auf `Yes`.

   Durch diese Einstellung wird der WYSIWYG-Editor für das Feld verfügbar gemacht.

1. Um das Attribut auf der Produktseite einzubeziehen, setzen Sie **[!UICONTROL Visible on Catalog Pages on Storefront]** auf `Yes`.

1. Nehmen Sie die folgenden Einstellungen vor, sofern sie von Ihrem Design unterstützt werden:

   - Um das Attribut in Produktlisten aufzunehmen, setzen Sie **[!UICONTROL Used in Product Listing]** auf `Yes`.

   - Um das Attribut als Sortierparameter für Produktlisten zu verwenden, setzen Sie **[!UICONTROL Used for Sorting in Product Listing]** auf `Yes`.

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save Attribute]**.

## Schritt 5: Dem Attributsatz das erstellte Attribut zuweisen

Damit ein Attribut auf der Produkterstellungsseite sichtbar ist, fügen Sie es zu einem bestimmten Attributsatz hinzu.

1. Gehen Sie nach Abschluss der vorherigen Schritte zu **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Attribute Set]**.

1. Wählen Sie den benötigten Attributsatz in der Liste aus und öffnen Sie ihn im Bearbeitungsmodus.

1. Ziehen Sie das erstellte Attribut aus der Liste **[!UICONTROL Unassigned Attributes]** in den entsprechenden Ordner in der Spalte **Gruppen** .

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save]**.

## Attribute für konfigurierbare Produkte

Jedes Attribut, das als Dropdown-Liste mit Optionen für ein [konfigurierbares Produkt](product-create-configurable.md) verwendet wird, muss die folgenden Eigenschaften aufweisen:

| Eigenschaft | Wert |
|----------|------ |
| Katalogeingabetyp für Store Owner | Dropdown |
| Anwendungsbereich | Global |

{style="table-layout:auto"}

## Attribut löschen

Wenn ein Attribut gelöscht wird, wird es aus allen zugehörigen Produkten und Attributsätzen entfernt. Systemattribute sind Teil der Kernfunktionalität Ihres Stores und können nicht gelöscht werden.

Bevor Sie ein Attribut löschen, stellen Sie sicher, dass es derzeit von keinem Produkt in Ihrem Katalog verwendet wird. Ob ein Attribut verwendet wird, lässt sich einfach ermitteln, indem Sie das Tool [Export](../systems/data-export.md) verwenden, um die Liste der Entitätsattribute des Produkts zu überprüfen. Wenn das Attribut nicht in der Liste enthalten ist, wird es von keinem Produkt im Katalog verwendet.

**_So löschen Sie ein Attribut:_**

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Product]**.

1. Suchen Sie das Attribut in der Liste und öffnen Sie es im Bearbeitungsmodus.

1. Klicken Sie auf **[!UICONTROL Delete Attribute]**.

   ![Attribut löschen](./assets/attribute-delete.png){width="600" zoomable="yes"}

1. Klicken Sie bei Aufforderung zur Bestätigung auf **[!UICONTROL OK]**.
