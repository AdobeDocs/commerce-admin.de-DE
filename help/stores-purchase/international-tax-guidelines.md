---
title: Steuerrichtlinien nach Land
description: Überprüfen Sie die empfohlenen Steuereinstellungen je nach Land.
exl-id: 027da0a2-0ff4-40a7-9b9c-eefad888bb7a
feature: Taxes
source-git-commit: f8254db7d69e58c8e9a78948ee6e40f5ea88cea0
workflow-type: tm+mt
source-wordcount: '1311'
ht-degree: 0%

---

# Steuerrichtlinien nach Land

## US-Steuerkonfiguration

Diese empfohlenen Einstellungen können für die meisten Steuerkonfigurationen für Geschäfte in den USA verwendet werden.

| Steueroption | Empfehlung |
|--- |--- |
| Katalogpreise laden | Ohne Steuer |
| FPT | Nein, denn FTP wird nicht besteuert. |
| Steuer auf Basis der | Versandherkunft |
| Steuerberechnung | Insgesamt |
| Versand besteuern? | Nein |
| Rabatt anwenden | Vor Steuern |
| Kommentar | Alle Steuerzonen haben dieselbe Priorität; idealerweise eine Zone für den Bundesstaat und eine oder mehrere Zonen für die Suche nach Postleitzahlen. |

{style="table-layout:auto"}

### Steuerklassen

| Steuerklasse | Empfohlene Einstellung |
|--- |--- |
| Steuerklasse für den Versand | Keine |

{style="table-layout:auto"}

### Berechnungsparameter

| Option | Empfohlene Einstellung |
|--- |--- |
| [!UICONTROL Tax Calculation Method Based On] | `Total` |
| [!UICONTROL Tax Calculation Based On] | `Shipping Origin` |
| [!UICONTROL Catalog Prices] | `Excluding Tax` |
| [!UICONTROL Shipping Prices] | `Excluding Tax` |
| [!UICONTROL Apply Customer Tax] | `After Discount` |
| [!UICONTROL Apply Discount on Prices] | `Excluding Tax` |

{style="table-layout:auto"}

### Standardmäßige Steuerzielberechnung

| Option | Empfohlene Einstellung |
|--- |--- |
| [!UICONTROL Default Country] | `United States` |
| [!UICONTROL Default State] | Bundesland, in dem das Unternehmen seinen Sitz hat. |
| [!UICONTROL Default Post Code] | Die in Ihren Steuerzonen verwendete Postleitzahl. |

{style="table-layout:auto"}

### Einstellungen zur Preisanzeige

| Option | Empfohlene Einstellung |
|--- |--- |
| [!UICONTROL Display Product Prices in Catalog] | `Excluding Tax` |
| [!UICONTROL Display Shipping Prices] | `Excluding Tax` |

{style="table-layout:auto"}

### Anzeigeeinstellungen für den Warenkorb

| Option | Empfohlene Einstellung |
|--- |--- |
| [!UICONTROL Display Prices] | `Excluding Tax` |
| [!UICONTROL Display Subtotal] | `Excluding Tax` |
| [!UICONTROL Display Shipping Amount] | `Excluding Tax` |
| [!UICONTROL Display Gift Wrapping Prices] | `Excluding Tax` |
| [!UICONTROL Display Printed Card Prices] | `Excluding Tax` |
| [!UICONTROL Include Tax in Grand Total] | `Yes` |
| [!UICONTROL Display Full Tax Summary] | `Yes` |
| [!UICONTROL Display Zero Tax Subtotal] | `Yes` |

{style="table-layout:auto"}

### Bestellungen, Rechnungen, Gutschriften und Anzeigeeinstellungen

| Option | Empfohlene Einstellung |
|--- |--- |
| [!UICONTROL Display Prices] | `Excluding Tax` |
| [!UICONTROL Display Subtotal] | `Excluding Tax` |
| [!UICONTROL Display Shipping Amount] | `Excluding Tax` |
| [!UICONTROL Include Tax in Grand Total] | `Yes` |
| [!UICONTROL Display Full Tax Summary] | `Yes` |
| [!UICONTROL Display Zero Tax Subtotal] | `Yes` |

{style="table-layout:auto"}

### Feste Produktsteuern (FPT)

| Option | Empfohlene Einstellung |
|--- |--- |
| [!UICONTROL Enable FPT] | `No` außer in Kalifornien. |

{style="table-layout:auto"}

## Steuerkonfiguration für Großbritannien

Diese empfohlenen Einstellungen können für die meisten Steuerkonfigurationen für Geschäfte in Großbritannien verwendet werden.

### GB B2C-Steuerkonfiguration

| Steueroption | Empfehlung |
|--- |--- |
| Katalogpreise laden | Ohne Steuer |
| FPT | Ja, einschließlich FTP und Beschreibung |
| Steuer auf Basis der | [!UICONTROL Shipping Address] |
| Steuerberechnung | Insgesamt |
| Versand besteuern? | Ja |
| Rabatt anwenden | Vor Steuern, Rabatt auf Preise, einschließlich Steuern. |
| Kommentar | Für Händler, die Lieferantenrechnungen (einschließlich MwSt.) markieren. |

{style="table-layout:auto"}

### Britische B2B-Steuerkonfiguration

| Steueroption | Empfehlung |
|--- |--- |
| Katalogpreise laden | Ohne Steuer |
| FPT | Ja, einschließlich FTP und Beschreibung |
| Steuer auf Basis der | [!UICONTROL Shipping Address] |
| Steuerberechnung | Bei Element |
| Versand besteuern? | Ja |
| Rabatt anwenden | Vor Steuern, Rabatt auf Preise, einschließlich Steuern. |
| Kommentar | B2B-Händler sollten einfachere Überlegungen zur MwSt.-Lieferkette anstellen. Die Steuerberechnung in Zeile ist ebenfalls gültig. Wenden Sie sich jedoch an Ihre Steuerzuständigkeit. Setup geht davon aus, dass sich ein Händler in der Lieferkette befindet und die verkauften Waren von anderen Anbietern für Mehrwertsteuerrabatte usw. verwendet werden. Diese Definition erleichtert die Unterscheidung der Steuern nach Posten, was eine schnellere Rabatterstellung ermöglicht. <br/><br/>**_Hinweis _**&#x200B;Einige Länder und Gebiete erfordern unterschiedliche Rundungsstrategien, die derzeit nicht von Commerce unterstützt werden, und nicht alle Länder und Gebiete erlauben eine Steuer auf Element- oder Zeilenebene. |

{style="table-layout:auto"}

## Steuerkonfiguration für Kanada

>[!IMPORTANT]
>
>Händler, die sich in einer GST/PST-Provinz (Montreal) befinden, sollten eine Steuerregel erstellen und einen kombinierten Steuerbetrag anzeigen. Bei Fragen wenden Sie sich bitte an eine qualifizierte Steuerbehörde.

| Steueroption | Empfehlung |
|--- |--- |
| Katalogpreise laden | Ohne Steuer |
| FPT | Ja, einschließlich FTP, Beschreibung, und Steuern auf FTP erheben. |
| Steuer auf Basis der | Versandherkunft |
| Steuerberechnung | Insgesamt |
| Versand besteuern? | Ja |
| Rabatt anwenden | Vor Steuern |

{style="table-layout:auto"}

Das folgende Beispiel zeigt, wie Sie GST-Steuersätze für Kanada und PST-Steuersätze für Saskatchewan mit Steuerregeln einrichten, die die beiden Steuersätze berechnen und anzeigen. In diesen Informationen wird eine Beispielkonfiguration beschrieben. Überprüfen Sie die korrekten Steuersätze und -regeln für Ihre Steuergebiete. Legen Sie bei der Einrichtung von Steuern den Bereich des Stores fest, um die Konfiguration auf alle entsprechenden Stores und Websites anzuwenden.

- Die feste Produktsteuer ist für relevante Waren als Produktattribut enthalten.
- In Quebec wird PST als TVQ bezeichnet. Wenn Sie einen Tarif für Quebec einrichten möchten, stellen Sie sicher, dass Sie TVQ als Kennung verwenden.

### Schritt 1: Einstellungen für die Steuerberechnung abschließen

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Legen Sie für eine Multi-Site-Konfiguration **[!UICONTROL Store View]** auf die Website und den Store fest, der das Ziel der Konfiguration ist.

1. Erweitern Sie im linken Bereich **[!UICONTROL Sales]** und wählen Sie **[!UICONTROL Tax]**.

1. Klicken Sie auf , um die einzelnen Abschnitte auf der Seite zu erweitern und die folgenden Einstellungen vorzunehmen:

#### Einstellungen für die Steuerberechnung

| Feld | Empfohlene Einstellung |
|--- |--- |
| [!UICONTROL Tax Calculation Method Based On] | `Total` |
| [!UICONTROL Tax Calculation Based On] | `Shipping Address` |
| [!UICONTROL Catalog Prices] | `Excluding Tax` |
| [!UICONTROL Shipping Prices] | `Excluding Tax` |
| [!UICONTROL Apply Customer Tax] | `After Discount` |
| [!UICONTROL Apply Discount on Prices] | `Excluding Tax` |
| [!UICONTROL Apply Tax On] | `Custom Price` (falls verfügbar) |

{style="table-layout:auto"}

#### Steuerklassen

| Feld | Empfohlene Einstellung |
|--- |--- |
| [!UICONTROL Tax Class for Shipping] | `Shipping` (Versand wird besteuert) |

{style="table-layout:auto"}

#### Zielberechnung der Standardsteuer

| Feld | Empfohlene Einstellung |
|--- |--- |
| [!UICONTROL Default Country] | `Canada` |
| [!UICONTROL Default State] | (falls zutreffend) |
| [!UICONTROL Default Postal Code] | `*` (Sternchen) |

{style="table-layout:auto"}

#### Anzeigeeinstellungen für den Warenkorb

| Feld | Empfohlene Einstellung |
|--- |--- |
| [!UICONTROL Include Tax in Grand Total] | `Yes` |
| [!UICONTROL Display Full Tax Summary] | `Yes` |
| [!UICONTROL Display Zero in Tax Subtotal] | `Yes` |

{style="table-layout:auto"}

#### Feste Produktsteuern

| Feld | Empfohlene Einstellung |
|--- |--- |
| [!UICONTROL Enable FPT] | `Yes` |
| Alle FTP-Anzeigeeinstellungen | `Including FPT and FPT description` |
| [!UICONTROL Apply Discounts to FPT] | `No` |
| [!UICONTROL Apply Tax to FPT] | `Yes` |
| [!UICONTROL Include FPT in Subtotal] | `No` |

{style="table-layout:auto"}

### Schritt 2: Einrichten der kanadischen Waren- und Dienstleistungssteuer (GST)

Wenn Sie die GST-Nummer auf Rechnungen und anderen Verkaufsbelegen drucken möchten, fügen Sie sie dem Namen der anwendbaren Steuersätze hinzu. Die globale Gutschrift wird als Teil des Gesamtbetrags der Gutschrift in jeder Auftragszusammenfassung angezeigt.

#### Verwalten von Steuerzonen und Steuersätzen

| Feld | Empfohlene Einstellung |
|--- |--- |
| [!UICONTROL Tax Identifier] | `Canada-GST` |
| [!UICONTROL Country] | `Canada` |
| [!UICONTROL State] | `*` (Sternchen) |
| [!UICONTROL Zip/Post is Range] | `No` |
| [!UICONTROL Zip/Post Code] | `*` (Sternchen) |
| [!UICONTROL Rate Percent] | `5.0000` |

{style="table-layout:auto"}

### Schritt 3: Einrichten der Canadian Provincial Sales Tax (PST)

Richten Sie einen anderen Steuersatz für die entsprechende Provinz ein.

#### Informationen zum Steuersatz

| Feld | Empfohlene Einstellung |
|--- |--- |
| [!UICONTROL Tax Identifier] | `Canada-SK-PST` |
| [!UICONTROL Country] | `Canada` |
| [!UICONTROL State] | `Saskatchewan` |
| [!UICONTROL Zip/Post is Range] | `No` |
| [!UICONTROL Zip/Post Code] | `*` (Sternchen) |
| [!UICONTROL Rate Percent] | `5.0000` |

{style="table-layout:auto"}

### Schritt 4: Erstellen einer GST-Steuerregel

Um eine Aufrechnung der Steuer zu vermeiden und die berechnete Steuer korrekt als separate Zeileneinträge für GST und PST anzuzeigen, legen Sie für jede Regel unterschiedliche Prioritäten fest und aktivieren Sie das Kontrollkästchen **Nur Zwischensumme berechnen**. Jede Steuer wird als separater Zeileneintrag angezeigt, die Steuerbeträge werden jedoch nicht zusammengerechnet.

#### Informationen zur Steuerregel

| Feld | Empfohlene Einstellung |
|--- |--- |
| -Name | `Retail-Canada-GST` |
| [!UICONTROL Customer Tax Class] | `Retail Customer` |
| [!UICONTROL Product Tax Class] | `Taxable GoodsShipping` |
| [!UICONTROL Tax Rate] | `Canada-GST` |
| [!UICONTROL Priority] | `0` |
| [!UICONTROL Calculate off subtotal only] | Aktivieren Sie dieses Kontrollkästchen. |
| [!UICONTROL Sort Order] | `0` |

{style="table-layout:auto"}

### Schritt 5: Erstellen einer PST-Steuerregel für Saskatchewan

Stellen Sie für diese Steuerregel sicher, dass Sie die Priorität auf 0 setzen und das Kontrollkästchen **Nur Zwischensumme berechnen** aktivieren. Jede Steuer wird als separater Zeileneintrag angezeigt, die Steuerbeträge werden jedoch nicht zusammengerechnet.

#### Informationen zur Steuerregel

| Feld | Empfohlene Einstellung |
|--- |--- |
| [!UICONTROL Name] | `Retail-Canada-PST` |
| [!UICONTROL Customer Tax Class] | `Retail Customer` |
| [!UICONTROL Product Tax Class] | `Taxable GoodsShipping` |
| [!UICONTROL Tax Rate] | `Canada-SK-PT` |
| [!UICONTROL Priority] | `1` |
| [!UICONTROL Calculate off subtotal only] | Aktivieren Sie dieses Kontrollkästchen. |
| [!UICONTROL Sort Order] | `0` |

{style="table-layout:auto"}

### Schritt 6: Speichern und Testen der Ergebnisse

1. Klicken Sie abschließend auf **[!UICONTROL Save Config]**.

1. Kehren Sie zu Ihrer Storefront zurück und erstellen Sie eine Beispielreihenfolge, um die Ergebnisse zu testen.

## EU-Steuerregelung

Das folgende Beispiel zeigt ein Geschäft mit Sitz in Frankreich, das in Frankreich über 100.000 Euro und in Deutschland über 100.000 Euro verkauft.

- Steuerberechnungen werden auf Website-Ebene verwaltet.
- Die Optionen für die Währungsumrechnung und die Steueranzeige werden einzeln auf der Store-Ansichtsebene gesteuert (aktivieren Sie das Kontrollkästchen „Website verwenden“, um die Standardeinstellung zu überschreiben).
- Wenn Sie das standardmäßige Steuerland festlegen, können Sie die korrekte Steuer für die Gerichtsbarkeit dynamisch anzeigen.
- Die feste Produktsteuer ist für relevante Waren als Produktattribut enthalten.
- Möglicherweise muss der Katalog bearbeitet werden, um sicherzustellen, dass er in der richtigen Kategorie-/Website-/Store-Ansicht angezeigt wird.

### Schritt 1: Erstellen Sie drei Produktsteuerklassen

Bei diesem Beispiel wird davon ausgegangen, dass mehrere mehrwertsteuerermäßigte Produktsteuerklassen nicht erforderlich sind.

1. Erstellen Sie eine MwSt.-Standard-Produktsteuerklasse.

1. Erstellen Sie eine Klasse mit ermäßigter MwSt. für Produkte.

1. Erstellen Sie eine MwSt.-freie Produktsteuerklasse.

### Schritt 2: Steuersätze für Frankreich und Deutschland erstellen

Erstellen Sie die folgenden Steuersätze:

| Steuersätze | Einstellungen |
|--- |--- |
| Frankreich - MwSt | Land: Frankreich <br/>Bundesland/Region: * <br/>Postleitzahl: * <br/>Tarif: 20% |
| Frankreich - ermäßigte MwSt | Land: Frankreich <br/>Bundesland/Region: * <br/>Postleitzahl: * <br/>Tarif: 5% |
| Germany-StandardVAT | Land: Deutschland <br/>Bundesland/Region: * <br/>Postleitzahl: * Tarif: 19% |
| Deutschland-ermäßigte MwSt | Land: Deutschland <br/>Bundesland/Region: * <br/>Postleitzahl: * <br/>Tarif: 7% |

{style="table-layout:auto"}

### Schritt 3: Einrichten der Steuerregeln

Erstellen Sie die folgenden Steuerregeln:

| Steuervorschriften | Einstellungen |
|--- |--- |
| Retail-France-StandardMwSt | Kundenklasse: Einzelhandelskunde <br/>Steuerklasse: MwSt.-Standard <br/>Steuersatz: Frankreich-StandardMwSt. <br/>Priorität: 0 <br/>Sortierreihenfolge: 0 |
| Einzelhandel - Frankreich - ermäßigte MwSt | Kundenklasse: Einzelhandelskunde <br/>Steuerklasse: MwSt. ermäßigt <br/>Steuersatz: Frankreich-ermäßigtMwSt. <br/>Priorität: 0 <br/>Sortierreihenfolge: 0 |
| Retail-Germany-StandardVAT | Kundenklasse: Einzelhandelskunde <br/>Steuerklasse: MwSt.-Standard <br/>Steuersatz: Deutschland-StandardMwSt. <br/>Priorität: 0 <br/>Sortierreihenfolge: 0 |
| Einzelhandel-Deutschland-ermäßigte MwSt | Kundenklasse: Einzelhandelskunde <br/>Steuerklasse: MwSt.-ermäßigt <br/>Steuersatz: Deutschland-ermäßigtMwSt. <br/>Priorität: 0 <br/>Sortierreihenfolge: 0 |

{style="table-layout:auto"}

### Schritt 4: Einrichten einer Shop-Ansicht für Deutschland

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL All Stores]**.

1. Erstellen Sie unter der Standard-Website eine Store-Ansicht für **[!UICONTROL Germany]**.

1. Gehen Sie dann wie folgt vor:

   - Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

   - Setzen Sie sich in der oberen linken Ecke **[!UICONTROL Default Config]** den französischen Laden.

   - Erweitern Sie auf der Seite Allgemein ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Countries Options]** und legen Sie das Standardland auf `France` fest.

   - Füllen Sie die Gebietsschema-Optionen nach Bedarf aus.

1. Wählen Sie oben links die deutsche **[!UICONTROL Store View]** aus.

1. Erweitern Sie auf der _Allgemein_ die **[!UICONTROL Countries Options]** ![Erweiterungsauswahl](../assets/icon-display-expand.png) und legen Sie das Standardland auf `Germany` fest.

1. Füllen Sie die Gebietsschema-Optionen nach Bedarf aus.

### Schritt 5: Konfigurieren der Steuereinstellungen für Frankreich

Füllen Sie die folgenden allgemeinen Steuereinstellungen aus:

| Feld | Empfohlene Einstellung |
|--- |--- |
| [[!UICONTROL Tax Classes]](../configuration-reference/sales/tax.md#tax-classes) |  |
| [!UICONTROL Tax Class for Shipping] | `Shipping` (Versand wird besteuert) |
| [[!UICONTROL Calculation Settings]](../configuration-reference/sales/tax.md#calculation-settings) |  |
| [!UICONTROL Tax Calculation Method Based On] | `Total` |
| [!UICONTROL Tax Calculation Based On] | `Shipping Address` |
| [!UICONTROL Catalog Prices] | `Including Tax` |
| [!UICONTROL Shipping Prices] | `Including Tax` |
| [!UICONTROL Apply Customer Tax] | `After Discount` |
| [!UICONTROL Apply Discount on Prices] | `Including Tax` |
| [!UICONTROL Apply Tax On] | `Custom Price if available` |
| [[!UICONTROL Default Tax Destination Calculation]](../configuration-reference/sales/tax.md#default-tax-destination-calculation) |  |
| [!UICONTROL Default Country] | `France` |
| [!UICONTROL Default State] |  |
| [!UICONTROL Default Postal Code] | `*` (Sternchen) |
| [[!UICONTROL Fixed Product taxes]](../configuration-reference/sales/tax.md#fixed-product-taxes) |  |
| [!UICONTROL Enable FPT] | `Yes` |
| [!UICONTROL All FPT Display Settings] | `Including FPT and FPT description` |
| [!UICONTROL Apply Discounts to FPT] | `No` |
| [!UICONTROL Apply Tax to FPT] | `Yes` |
| [!UICONTROL Include FPT in Subtotal] | `Yes` |

{style="table-layout:auto"}

### Schritt 6: Steuereinstellungen für Deutschland konfigurieren

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Setzen Sie in der oberen rechten Ecke **[!UICONTROL Store View]** auf die Ansicht zum deutschen Geschäft und klicken Sie zur Bestätigung auf **[!UICONTROL OK]** .

1. Erweitern Sie im linken Bereich **[!UICONTROL Sales]** und wählen Sie **[!UICONTROL Tax]**.

1. Gehen Sie im Abschnitt **[!UICONTROL Default Tax Destination Calculation]** wie folgt vor:

   - Deaktivieren Sie das Kontrollkästchen **[!UICONTROL Use Website]** nach jedem Feld.

   - Aktualisieren Sie die folgenden Werte, um den Versandeinstellungen [ Website (](shipping-settings.md#point-of-origin)) zu entsprechen:

      - Standardland
      - Standardzustand
      - Standard-Postleitzahl

     Diese Einstellung stellt sicher, dass die Steuer korrekt berechnet wird, wenn die Produktpreise die Steuer enthalten.

     ![Standardmäßige Zielberechnung der Steuer](./assets/destination-calc-french.png){width="600" zoomable="yes"}

1. Klicken Sie abschließend auf **[!UICONTROL Save Config]**.
