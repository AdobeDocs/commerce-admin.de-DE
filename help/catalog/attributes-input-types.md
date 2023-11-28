---
title: Attributeingabetypen
description: Erfahren Sie mehr über die Eingabetypen, die für Produktattribute verfügbar sind und die den Datentyp, der eingegeben werden kann, sowie das Format des Felds oder Eingabedialogik bestimmen.
exl-id: c35b3b9d-57b0-4c33-abdb-662ac6d0260e
feature: Catalog Management, Products
source-git-commit: 370131cd73a320b04ee92fa9609cb24ad4c07eca
workflow-type: tm+mt
source-wordcount: '637'
ht-degree: 0%

---

# Attributeingabetypen

Beim Anzeigen über den Administrator sind Attribute die Felder, die Sie beim Erstellen eines Produkts ausfüllen. Der Eingabetyp, der einem Attribut zugewiesen wird, bestimmt den Datentyp, der eingegeben werden kann, sowie das Format des Felds oder Eingabefelds. Vom Standpunkt des Kunden aus liefern Attribute Informationen über das Produkt und sind die Optionen und Dateneingabefelder, die zum Kauf eines Produkts ausgefüllt werden müssen.

## Eingabetypen

| Eigenschaft | Beschreibung |
|--- |--- |
| [!UICONTROL Text Field] | Ein einzeiliges Eingabefeld für Text. |
| [!UICONTROL Text Area] | Ein mehrzeiliges Eingabefeld für die Eingabe von Textabsätzen, z. B. eine Produktbeschreibung. Sie können den WYSIWYG-Editor verwenden, um den Text mit HTML-Tags zu formatieren, oder die Tags direkt in den Text eingeben. |
| [!UICONTROL Text Editor] | Ein voll funktionsfähiger Texteditor am Attributstandort. |
| [!UICONTROL Date] | Zeigt einen Datumswert im [bevorzugtes Format](#date-and-time-options) und [Zeitzone](../getting-started/store-details.md#locale-options). Datumswerte können aus einer Liste oder einem Kalender ausgewählt werden ( ![Kalendersymbol](../assets/icon-calendar.png) ). <br/><br/>**_Hinweis:_**Abhängig von Ihrer Systemkonfiguration_Admin _Benutzer können Datumsangaben direkt in ein Feld eingeben oder ein Datum aus dem Kalender oder der Liste auswählen. Informationen zum Festlegen von Datums- und Uhrzeitwerten finden Sie unter [Datums- und Uhrzeitoptionen](#date-and-time-options). |
| [!UICONTROL Date and Time] | Zeigt den Datums- und Uhrzeitwert im [bevorzugtes Format](#date-and-time-options) und [Zeitzone](../getting-started/store-details.md#locale-options). Datum und Uhrzeit können manuell eingegeben oder aus einem Kalender ausgewählt werden. Beispielformat: MM/TT/JJJJ HH:MM |
| [!UICONTROL Yes/No] | Zeigt eine Dropdownliste mit vordefinierten Optionen von `Yes` und `No`. |
| Dropdown | Zeigt eine Dropdown-Liste mit Werten an, die nur eine Auswahl zulassen. Der Dropdown-Eingabetyp ist eine Schlüsselkomponente von [konfigurierbare Produkte](../catalog/product-create-configurable.md). |
| [!UICONTROL Multiple Select] | Zeigt eine Dropdown-Liste mit Werten an, die mehrere Auswahlen akzeptieren. |
| [!UICONTROL Price] | Dieser Eingabetyp wird verwendet, um Preisfelder zu erstellen, die zusätzlich zu den vordefinierten Attributen verwendet werden: `Price`, `Special Price`, `Tier Price`, und `Cost`. Die verwendete Währung wird durch Ihre Systemkonfiguration bestimmt. |
| [!UICONTROL Media Image] | Verbindet ein zusätzliches Bild mit einem Produkt, z. B. einem Produktlogo, Pflegeanleitungen oder Zutaten aus einem Lebensmitteletikett. Wenn Sie dem Attributsatz eines Produkts ein Medienbildattribut hinzufügen, wird es zu einem zusätzlichen Bildtyp, zusammen mit &quot;Base&quot;, &quot;Small&quot;und &quot;Thumbnail&quot;. Das Medienbildattribut kann aus dem [Storefront-Medienbrowser](catalog-images-video.md#storefront-media-browser). |
| [!UICONTROL Fixed Product Tax] | Ermöglicht die Definition [FPT-Raten](../stores-purchase/fixed-product-tax.md) basierend auf den Anforderungen Ihres Gebietsschemas. |
| [!UICONTROL Visual Swatch] | Zeigt ein Muster an, das die Farbe, Textur oder das Muster eines konfigurierbaren Produkts darstellt. A [visuelles Muster](swatches.md) kann mit einem hexadezimalen Farbwert gefüllt werden oder ein hochgeladenes Bild anzeigen, das die Farbe, das Material, die Textur oder das Muster der Option darstellt. |
| [!UICONTROL Text Swatch] | Eine textbasierte Darstellung einer konfigurierbaren Produktoption, die häufig für die Größe verwendet wird. [Textmuster](swatches.md) kann auch hexadezimale Farbwerte enthalten. |
| [!UICONTROL Page Builder] | A [[!DNL Page Builder]](../page-builder/workspace.md) Arbeitsbereich am Attributstandort, der es erleichtert, ansprechende Inhalte zur Produktseite hinzuzufügen. |

{style="table-layout:auto"}

## Datums- und Uhrzeitoptionen

Sie können das Format der Datums- und Uhrzeitfelder anpassen und das Eingabefeld für die Dateneingabe auswählen. Datumswerte können aus einer Dropdown-Liste oder einem Popup-Kalender ausgewählt werden.

![Beispiel: Popup-Kalender für Storefront](./assets/storefront-popup-calendar.png){width="700" zoomable="yes"}

**_So formatieren Sie Datums-/Uhrzeitfelder:_**

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im Bedienfeld auf der linken Seite **[!UICONTROL Catalog]** und klicken Sie auf **[!UICONTROL Catalog]** Unterelement.

1. Erweitern Sie die **[!UICONTROL Date & Time Custom Options]** Abschnitt.

   ![Katalogkonfiguration - Datums- und Uhrzeitoptionen](../configuration-reference/catalog/assets/catalog-date-time-custom-options.png){width="600" zoomable="yes"}

   Eine detaillierte Liste dieser Optionen finden Sie unter [_Benutzerdefinierte Optionen für Datum und Uhrzeit_](../configuration-reference/catalog/catalog.md) im _Konfigurationsreferenz_.

1. Um einen Popup-Kalender als Eingabedialog für Datumsfelder zu verwenden, legen Sie **[!UICONTROL Use JavaScript Calendar]** nach `Yes`.

1. Zur Festlegung der **[!UICONTROL Date Fields Order]**, legen Sie die Reihenfolge der einzelnen Teile des Datumsfelds nach Bedarf fest:

   - Monat
   - Tag
   - Jahr

1. Um Ihr bevorzugtes Zeitformat festzulegen, legen Sie **Zeitformat** auf einen der folgenden Werte zu:

   - `12h AM/PM`
   - `24h`

1. Zur Festlegung der **[!UICONTROL Year Range]** Geben Sie für die Dropdown-Werte das Jahr (YYYY) ein, für das die Variable **[!UICONTROL from]** und **[!UICONTROL to]** Daten.

   Wenn das Feld leer ist, wird standardmäßig das aktuelle Jahr verwendet.

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save Config]**.
