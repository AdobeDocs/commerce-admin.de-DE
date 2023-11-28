---
title: Produkteinstellungen - [!UICONTROL Customizable Options]
description: Bei einem Produkt muss die Variable [!UICONTROL Customizable Options] -Einstellungen ermöglichen es Ihnen, eine Auswahl von Optionen mit Text-, Auswahl- und Datumseingabetypen anzubieten.
exl-id: 7d23c5c5-2b2a-4f2a-b843-9c27b851be5f
feature: Catalog Management, Products
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '811'
ht-degree: 0%

---

# Produkteinstellungen - [!UICONTROL Customizable Options]

Das Hinzufügen anpassbarer Optionen zu einem Produkt ist eine einfache Möglichkeit, eine Auswahl von Optionen mit Text-, Auswahl- und Datumseingabetypen anzubieten. Anpassbare Optionen sind eine gute Lösung, wenn Ihre Inventaranforderungen einfach sind. Da sie jedoch auf Variationen einer einzelnen SKU basieren, können sie nicht zur Verwaltung von Aktien oder als Grundlage für Preisregelbedingungen verwendet werden. Wenn Sie mehrere Produkte mit denselben Optionen haben, können Sie ein Produkt einrichten und die Optionen in die anderen Produkte importieren.

Wenn ein Kunde ein Produkt mit einer anpassbaren Option kauft, wird unter der Produktbeschreibung eine Beschreibung jeder ausgewählten Option angezeigt und jedes zugehörige Markup (oder Markdown) wird automatisch auf den Preis des Artikels angewendet.

![Produktdetails mit anpassbarer Option](./assets/storefront-customizable-option-product-detail.png){width="700" zoomable="yes"}

Wenn eine Warenkorbpreisregel durch den Kauf ausgelöst wird, gilt die anfängliche Berechnung zunächst für den Produktpreis und anschließend für den Zeilenartikelpreis mit einer Anpassung für anwendbare anpassbare Optionen. Im folgenden Beispiel kauft der Kunde eine Tüte für 74,00 US-Dollar sowie eine anpassbare Option für ein Monogramm. Auf den Basisproduktpreis wird ein Markup von 14,80 USD angewendet, und der angepasste Preis wird als 88,80 USD angezeigt. In diesem Fall wird durch den Kauf der Tüte eine Warenkorbpreisregel auf der Grundlage der Produkt-SKU Trigger und ein Rabatt auf den Kauf, plus kostenloser Versand, gewährt. Obwohl die Regel zum Warenkorbpreis nicht durch die anpassbare Option ausgelöst wird, wendet sie den Rabatt auf den Warenkorbinhalt an, der das Markup für die anpassbare Option enthält.

![Warenkorb mit anpassbarer Option und Preisregel](./assets/storefront-customizable-option-cart-price-rule.png){width="700" zoomable="yes"}

>[!NOTE]
>
>Auf die anpassbaren Festpreis-Optionen wird kein Rabatt für Katalogpreisregeln angewendet.

## Benutzerdefinierte Optionen erstellen

1. Öffnen Sie das Produkt im Bearbeitungsmodus.

1. Hinunter scrollen und erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die _[!UICONTROL Customizable Options]_Abschnitt.

1. Klicken **[!UICONTROL Add Option]**.

   ![Anpassbare Optionen](./assets/product-customizable-options.png){width="600" zoomable="yes"}

1. Füllen Sie die neuen Optionseinstellungen aus:

   - Für **[!UICONTROL Option Title]**, geben Sie einen Namen für die Option ein.

   - Legen Sie die **[!UICONTROL Option Type]** für den Typ der Dateneingabe.

   - Wenn die Option zum Kauf des Produkts nicht erforderlich ist, heben Sie die Auswahl der **[!UICONTROL Required]** aktivieren.

1. Füllen Sie die Felder entsprechend dem Dateneingabetyp aus:

   - Für **[!UICONTROL Title]** einen Namen für diese Option eingeben.

   - (Optional) Für **[!UICONTROL Price]**, geben Sie ein Markup oder Markdown aus dem Basisproduktpreis ein, der für diese Option gilt.

   - Satz **[!UICONTROL Price Type]** auf einen der folgenden Werte zu:

      - `Fixed` - Der Preis der Variante unterscheidet sich vom Preis des Basisprodukts durch einen festen Geldbetrag, z. B. 1 USD.
      - `Percentage` - Der Preis der Variante unterscheidet sich um 10 % vom Preis des Basisprodukts.

   - (Optional) Geben Sie einen **[!UICONTROL SKU]** für die Option. Die Option SKU ist ein Suffix, das der Produkt-SKU hinzugefügt wird.

   - Wenn die Variable _[!UICONTROL Option Type]_is `File`, legen Sie die Parameter für die Datei fest. Für **[!UICONTROL Compatible File Extensions]**die gültigen Erweiterungen als kommagetrennte Werte eingeben (z. B. `png, jpg, gif`). Für **[!UICONTROL Maximum Image Size]**, geben Sie die maximale Bildgröße in Pixel ein. Wenn es sich um einen Texteintrag handelt, geben Sie den Höchstwert für **[!UICONTROL Maximum Characters]**.

   ![Option Werte zur Anpassung hinzufügen](./assets/product-customizable-options-add-values.png){width="600" zoomable="yes"}

1. (Optional) Wenn Sie eine weitere anpassbare Option hinzufügen möchten, klicken Sie auf **[!UICONTROL Add Option]**.

   - Nehmen Sie die zuvor vorgenommenen Einstellungen vor.

   - Um die Reihenfolge der Optionen zu ändern, klicken Sie auf die Schaltfläche _[!UICONTROL Order]_![Symbol &quot;Sortierung&quot;](../assets/icon-sort-order.png) und ziehen Sie die Option an eine neue Position in der Liste.

   Wiederholen Sie diesen Schritt für jede hinzuzufügende Option.

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save]**.

## Anpassbare Optionen importieren

1. Im _Anpassbare Optionen_ Abschnitt, klicken Sie auf **[!UICONTROL Import Options]**.


1. Alle Produkte mit anpassbaren Optionen werden im Raster angezeigt.

1. Aktivieren Sie in der Liste das Kontrollkästchen des Produkts mit den Optionen, die Sie importieren möchten.

1. Klicken **[!UICONTROL Import]**.

1. Wenn Sie fertig sind, können Sie weitere benutzerdefinierte Optionen hinzufügen oder auf **[!UICONTROL Save and Close]**.

## Eingabetypen

| Typ | Beschreibung |
|---------------------|---------------|
| [!UICONTROL Text] | Eine Eingabeliste oder ein Textfeld, in das der Kunde die erforderlichen Informationen eingeben kann. Optionen:<br />**[!UICONTROL Field]**- Ein einzeiliges Eingabefeld für Text.<br />**[!UICONTROL Area]** - Ein mehrzeiliges Eingabefeld. Dieser Typ unterstützt keine erweiterte Formatierung wie HTML. Verwenden Sie &quot;Max. Zeichen&quot;, um die Länge des eingegebenen Texts zu begrenzen und eine korrekte Darstellung des eingegebenen Texts in der Admin-Konsole sicherzustellen. |
| [!UICONTROL File] | Ermöglicht dem Kunden das Hochladen einer Datei. |
| [!UICONTROL Select] | Ermöglicht dem Kunden, je nach verwendetem Eingabetyp eine oder mehrere Optionen auszuwählen. Optionen:<br />**[!UICONTROL Drop-down]**- Eine Dropdown-Liste mit Optionen, die nur eine Auswahl zulassen.<br />**[!UICONTROL Radio Buttons]** - Ein Satz von Optionen, der nur eine Auswahl erlaubt.<br />**[!UICONTROL Checkbox]**- Ein Kontrollkästchen ist eine Variante einer Ja/Nein-Option. Wenn das Produkt mehr als ein Kontrollkästchen aufweist, können mehrere Auswahlen vorgenommen werden.<br />**[!UICONTROL Multiple Select]** - Ein Dropdown-Listenfeld mit Optionen, das mehrere Auswahlen akzeptiert. Um mehrere Optionen auszuwählen, halten Sie die Strg- (PC-) oder Befehlstaste (Mac) gedrückt und klicken Sie auf jede Option. |
| [!UICONTROL Date] | Ermöglicht dem Kunden die Eingabe eines Datums oder einer Uhrzeit oder die Auswahl des Werts aus einem Kalender. Optionen: <br />**[!UICONTROL Date]**- Ein Eingabefeld für einen Datumswert. Das Datum kann direkt in das Feld eingegeben oder aus einer Liste oder einem Kalender ausgewählt werden. Die Eingabemethode und das Format werden durch die [Datums- und Uhrzeitoptionen](attributes-input-types.md#date-and-time-options) Konfiguration.<br />**[!UICONTROL Date & Time]** - Ein Eingabefeld für einen Datums- und Uhrzeitwert.<br />**[!UICONTROL Time]**- Ein Eingabefeld für einen Zeitwert. |

{style="table-layout:auto"}
