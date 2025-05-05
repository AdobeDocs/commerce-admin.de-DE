---
title: Attributeingabetypen
description: Erfahren Sie mehr über die für Produktattribute verfügbaren Eingabetypen, die den Typ der einzugebenden Daten und das Format des Felds oder Eingabesteuerelements bestimmen.
exl-id: c35b3b9d-57b0-4c33-abdb-662ac6d0260e
feature: Catalog Management, Products
source-git-commit: 370131cd73a320b04ee92fa9609cb24ad4c07eca
workflow-type: tm+mt
source-wordcount: '637'
ht-degree: 0%

---

# Attributeingabetypen

In der Administratoransicht sind Attribute die Felder, die Sie ausfüllen, wenn Sie ein Produkt erstellen. Der Eingabetyp, der einem Attribut zugewiesen ist, bestimmt den Typ der einzugebenden Daten und das Format des Felds oder Eingabesteuerelements. Aus Sicht des Kunden liefern Attribute Informationen über das Produkt und sind die Optionen und Dateneingabefelder, die zum Kauf eines Produkts ausgefüllt werden müssen.

## Eingabetypen

| Eigenschaft | Beschreibung |
|--- |--- |
| [!UICONTROL Text Field] | Ein einzeiliges Eingabefeld für Text. |
| [!UICONTROL Text Area] | Ein mehrzeiliges Eingabefeld zum Eingeben von Textabsätzen, z. B. eine Produktbeschreibung. Sie können den WYSIWYG-Editor verwenden, um den Text mit HTML-Tags zu formatieren, oder die Tags direkt in den Text eingeben. |
| [!UICONTROL Text Editor] | Ein voll funktionsfähiger Texteditor am Attributspeicherort. |
| [!UICONTROL Date] | Zeigt einen Datumswert im [bevorzugten Format](#date-and-time-options) und [Zeitzone](../getting-started/store-details.md#locale-options) an. Datumswerte können aus einer Liste oder einem Kalender ausgewählt werden ( ![Kalendersymbol](../assets/icon-calendar.png) ). <br/><br/>**_Hinweis _**&#x200B;Je nach Systemkonfiguration können_Admin _-Benutzer Datumsangaben direkt in ein Feld eingeben oder ein Datum aus dem Kalender oder der Liste auswählen. Weitere Informationen zum Angeben von Datums- und Uhrzeitwerten finden Sie unter [Optionen für Datum und Uhrzeit](#date-and-time-options). |
| [!UICONTROL Date and Time] | Zeigt einen Datums- und Uhrzeitwert im [bevorzugten Format](#date-and-time-options) und [Zeitzone](../getting-started/store-details.md#locale-options) an. Datum und Uhrzeit können manuell eingegeben oder aus einem Kalender ausgewählt werden. Beispielformat: MM/TT/JJJJ hh:MM |
| [!UICONTROL Yes/No] | Zeigt eine Dropdown-Liste mit vordefinierten Optionen `Yes` und `No` an. |
| Dropdown | Zeigt eine Dropdown-Liste mit Werten an, die nur eine einzige Auswahl akzeptieren. Der Dropdown-Eingabetyp ist eine Schlüsselkomponente von [konfigurierbaren Produkten](../catalog/product-create-configurable.md). |
| [!UICONTROL Multiple Select] | Zeigt eine Dropdown-Liste mit Werten an, die mehrere Auswahlmöglichkeiten akzeptieren. |
| [!UICONTROL Price] | Dieser Eingabetyp wird verwendet, um Preisfelder zu erstellen, die zusätzlich zu den vordefinierten Attributen erstellt werden: `Price`, `Special Price`, `Tier Price` und `Cost`. Die verwendete Währung wird von Ihrer Systemkonfiguration bestimmt. |
| [!UICONTROL Media Image] | Ordnet einem Produkt ein zusätzliches Bild zu, z. B. ein Produktlogo, Pflegehinweise oder Zutaten von einem Lebensmitteletikett. Wenn Sie dem Attributsatz eines Produkts ein Medienbildattribut hinzufügen, wird es zu einem zusätzlichen Bildtyp, zusammen mit „Basis“, „Klein“ und „Miniatur“. Das Medienbildattribut kann aus dem „Storefront[Medienbrowser“ ](catalog-images-video.md#storefront-media-browser) werden. |
| [!UICONTROL Fixed Product Tax] | Ermöglicht die Definition [FPT](../stores-purchase/fixed-product-tax.md)Tarife basierend auf den Anforderungen Ihres Gebietsschemas. |
| [!UICONTROL Visual Swatch] | Zeigt ein Farbfeld an, das die Farbe, Textur oder das Muster eines konfigurierbaren Produkts darstellt. Ein [visuelles Farbfeld](swatches.md) kann mit einem hexadezimalen Farbwert ausgefüllt werden oder ein hochgeladenes Bild anzeigen, das die Farbe, das Material, die Textur oder das Muster der Option darstellt. |
| [!UICONTROL Text Swatch] | Eine textbasierte Darstellung einer konfigurierbaren Produktoption, die häufig für die Größe verwendet wird. [Textmuster](swatches.md) können auch hexadezimale Farbwerte enthalten. |
| [!UICONTROL Page Builder] | Ein [[!DNL Page Builder]](../page-builder/workspace.md) Arbeitsbereich am Attributspeicherort, der das Hinzufügen ansprechender Inhalte zur Produktseite erleichtert. |

{style="table-layout:auto"}

## Optionen für Datum und Uhrzeit

Sie können das Format von Datums- und Uhrzeitfeldern anpassen und das Eingabedialog-Steuerelement auswählen, das für die Dateneingabe verwendet wird. Datumswerte können aus einer Dropdown-Liste oder einem Popup-Kalender ausgewählt werden.

![Beispiel - Popup-Kalender der Storefront](./assets/storefront-popup-calendar.png){width="700" zoomable="yes"}

**_So formatieren Sie Datums-/Uhrzeitfelder:_**

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im Bedienfeld auf der linken Seite **[!UICONTROL Catalog]** und klicken Sie auf das Unterelement **[!UICONTROL Catalog]** .

1. Erweitern Sie den Abschnitt **[!UICONTROL Date & Time Custom Options]** .

   ![Katalogkonfiguration - Datums- und Uhrzeitoptionen](../configuration-reference/catalog/assets/catalog-date-time-custom-options.png){width="600" zoomable="yes"}

   Eine detaillierte Liste dieser Optionen finden Sie unter [_Benutzerdefinierte Datums- und Uhrzeitoptionen_](../configuration-reference/catalog/catalog.md) in _Konfigurationsreferenz_.

1. Um einen Popup-Kalender als Eingabedialog für Datumsfelder zu verwenden, setzen Sie **[!UICONTROL Use JavaScript Calendar]** auf `Yes`.

1. Um die **[!UICONTROL Date Fields Order]** festzulegen, legen Sie die Reihenfolge der einzelnen Teile des Datumsfelds nach Bedarf fest:

   - Monat
   - Tag
   - Jahr

1. Um Ihr bevorzugtes Zeitformat festzulegen, **Sie (**) auf eine der folgenden Optionen:

   - `12h AM/PM`
   - `24h`

1. Um die **[!UICONTROL Year Range]** für die Dropdown-Werte festzulegen, geben Sie das Jahr (JJJJ) ein, um das **[!UICONTROL from]**- und **[!UICONTROL to]** festzulegen.

   Wenn dieses Feld leer ist, wird standardmäßig das aktuelle Jahr angezeigt.

1. Klicken Sie abschließend auf **[!UICONTROL Save Config]**.
