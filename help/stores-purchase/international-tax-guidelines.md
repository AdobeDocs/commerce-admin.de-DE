---
title: Steuerleitlinien nach Ländern
description: Überprüfen Sie die empfohlenen Steuereinstellungen nach Land.
exl-id: 027da0a2-0ff4-40a7-9b9c-eefad888bb7a
feature: Taxes
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '1336'
ht-degree: 0%

---

# Steuerleitlinien nach Ländern

## US-Steuerkonfiguration

Diese empfohlenen Einstellungen können für die meisten Steuerkonfigurationen für Geschäfte in den USA verwendet werden.

| Steueroption | Empfehlung |
|--- |--- |
| Katalogpreise | Steuern ausschließen |
| FPT | Nein, weil FPT nicht besteuert wird. |
| Auf Steuerbasis | Versandursprung |
| Steuerberechnung | Gesamt |
| Steuerliche Schifffahrt? | Nein |
| Rabatt anwenden | Vor Steuern |
| Kommentar | Alle Steuerzonen haben dieselbe Priorität. Idealerweise eine Zone für den Bundesstaat und eine oder mehrere Zonen für die Postleitzahlensuche. |

{style="table-layout:auto"}

### Steuerklassen

| Steuerklasse | Empfohlene Einstellung |
|--- |--- |
| Steuerklasse für die Schifffahrt | Keines |

{style="table-layout:auto"}

### Berechnungseinstellungen

| Option | Empfohlene Einstellung |
|--- |--- |
| [!UICONTROL Tax Calculation Method Based On] | `Total` |
| [!UICONTROL Tax Calculation Based On] | `Shipping Origin` |
| [!UICONTROL Catalog Prices] | `Excluding Tax` |
| [!UICONTROL Shipping Prices] | `Excluding Tax` |
| [!UICONTROL Apply Customer Tax] | `After Discount` |
| [!UICONTROL Apply Discount on Prices] | `Excluding Tax` |

{style="table-layout:auto"}

### Standardmäßige Zielbestimmungsberechnung

| Option | Empfohlene Einstellung |
|--- |--- |
| [!UICONTROL Default Country] | `United States` |
| [!UICONTROL Default State] | Staat, in dem das Unternehmen seinen Sitz hat. |
| [!UICONTROL Default Post Code] | Die Postleitzahl, die in Ihren Steuerzonen verwendet wird. |

{style="table-layout:auto"}

### Anzeigeparameter des Preises

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

### Bestellungen, Rechnungen, Kreditkarten und Anzeigeeinstellungen

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
| [!UICONTROL Enable FPT] | 0, außer in Kalifornien.`No` |

{style="table-layout:auto"}

## Steuerkonfiguration im Vereinigten Königreich

Diese empfohlenen Einstellungen können für die meisten Steuerkonfigurationen für Geschäfte im Vereinigten Königreich verwendet werden.

### UK - B2C-Steuerkonfiguration

| Steueroption | Empfehlung |
|--- |--- |
| Katalogpreise | Steuern ausschließen |
| FPT | Ja, einschließlich FPT und Beschreibung |
| Auf Steuerbasis | [!UICONTROL Shipping Address] |
| Steuerberechnung | Gesamt |
| Steuerliche Schifffahrt? | Ja |
| Rabatt anwenden | Vor Steuern, Rabatt auf die Preise, einschließlich Steuern. |
| Kommentar | Bei Händlern, die Lieferantenrechnungen ausweisen (einschließlich MwSt.). |

{style="table-layout:auto"}

### U.K. B2B-Steuerkonfiguration

| Steueroption | Empfehlung |
|--- |--- |
| Katalogpreise | Steuern ausschließen |
| FPT | Ja, einschließlich FPT und Beschreibung |
| Auf Steuerbasis | [!UICONTROL Shipping Address] |
| Steuerberechnung | Zum Element |
| Steuerliche Schifffahrt? | Ja |
| Rabatt anwenden | Vor Steuern, Rabatt auf die Preise, einschließlich Steuern. |
| Kommentar | B2B-Händler sollten einfachere Aspekte der MwSt-Lieferkette vorlegen. Die Berechnung der Steuern in der Zeile ist ebenfalls gültig. Bitte fragen Sie jedoch bei Ihrem Steuergericht nach. Bei der Einrichtung wird davon ausgegangen, dass sich ein Händler in der Lieferkette befindet und dass verkaufte Waren von anderen Anbietern für MwSt-Rabatte usw. verwendet werden. Durch diese Definition ist es leicht, die Steuern für eine schnellere Rabatterzeugung nach Einzelposten zu ermitteln. <br/><br/>**_Hinweis:_**Einige Rechtssysteme erfordern unterschiedliche Rundungsstrategien, die derzeit nicht von Commerce unterstützt werden, und dass nicht alle Rechtssysteme eine Steuer auf Element- oder Zeilenebene zulassen. |

{style="table-layout:auto"}

## Kanadische Steuerkonfiguration

>[!IMPORTANT]
>
>Händler in der Provinz GST/PST (Montreal) sollten eine Steuerregel erstellen und einen kombinierten Steuerbetrag anzeigen. Wenden Sie sich bei Fragen an eine qualifizierte Steuerbehörde. Weitere Informationen zu den steuerlichen Anforderungen bestimmter Provinzen finden Sie unter: [Revenu Québec][1], [Government of Saskatchewan][2] und [Manitoba Information für Anbieter][3]

| Steueroption | Empfehlung |
|--- |--- |
| Katalogpreise | Steuern ausschließen |
| FPT | Ja, einschließlich FPT, Beschreibung und Anwendung der Steuer auf FPT. |
| Auf Steuerbasis | Versandursprung |
| Steuerberechnung | Gesamt |
| Steuerliche Schifffahrt? | Ja |
| Rabatt anwenden | Vor Steuern |

{style="table-layout:auto"}

Im folgenden Beispiel wird gezeigt, wie GST-Steuersätze für Kanada und PST-Steuersätze für Saskatchewan eingerichtet werden, mit Steuerregeln, die die beiden Steuersätze berechnen und anzeigen. In diesen Informationen wird eine Beispielkonfiguration beschrieben. Stellen Sie sicher, dass Sie die richtigen Steuersätze und -regeln für Ihre Steuergebiete überprüfen. Legen Sie beim Einrichten von Steuern den Speicherbereich fest, um die Konfiguration auf alle zutreffenden Stores und Websites anzuwenden.

- Die feste Produktsteuer ist für relevante Waren als Produktattribut enthalten.
- In Quebec wird PST als TVQ bezeichnet. Wenn Sie eine Rate für Quebec einrichten möchten, stellen Sie sicher, dass Sie TVQ als Kennung verwenden.

### Schritt 1: Vollständige Steuerberechnungseinstellungen

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Legen Sie für eine Multisite-Konfiguration **[!UICONTROL Store View]** auf die Website fest und speichern Sie, das das Ziel der Konfiguration ist.

1. Erweitern Sie im linken Bereich den Wert **[!UICONTROL Sales]** und wählen Sie **[!UICONTROL Tax]** aus.

1. Klicken Sie auf , um die einzelnen Abschnitte auf der Seite zu erweitern und die folgenden Einstellungen abzuschließen:

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

#### Standardmäßige Berechnung des Steuerziels

| Feld | Empfohlene Einstellung |
|--- |--- |
| [!UICONTROL Default Country] | `Canada` |
| [!UICONTROL Default State] | (gegebenenfalls) |
| [!UICONTROL Default Postal Code] | `*` (Sternchen) |

{style="table-layout:auto"}

#### Anzeigeeinstellungen für Warenkorb

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
| Alle FPT-Anzeigeeinstellungen | `Including FPT and FPT description` |
| [!UICONTROL Apply Discounts to FPT] | `No` |
| [!UICONTROL Apply Tax to FPT] | `Yes` |
| [!UICONTROL Include FPT in Subtotal] | `No` |

{style="table-layout:auto"}

### Schritt 2: Einrichten der kanadischen Waren- und Dienstleistungssteuer (GST)

Um die GST-Nummer auf Rechnungen und anderen Verkaufsunterlagen auszudrucken, geben Sie sie in die Bezeichnung der anwendbaren Steuersätze ein. Der GST wird als Teil des GST-Betrags in einer beliebigen Bestellübersicht angezeigt.

#### Steuerzonen und -sätze verwalten

| Feld | Empfohlene Einstellung |
|--- |--- |
| [!UICONTROL Tax Identifier] | `Canada-GST` |
| [!UICONTROL Country] | `Canada` |
| [!UICONTROL State] | `*` (Sternchen) |
| [!UICONTROL Zip/Post is Range] | `No` |
| [!UICONTROL Zip/Post Code] | `*` (Sternchen) |
| [!UICONTROL Rate Percent] | `5.0000` |

{style="table-layout:auto"}

### Schritt 3: Einrichten der kanadischen Provinzsteuer (PST)

einen weiteren Steuersatz für die betreffende Provinz einrichten.

#### Informationen über Steuersätze

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

Um eine Verschmelzung der Steuer zu vermeiden und die berechnete Steuer ordnungsgemäß als separate Zeileneinträge für GST und PST anzuzeigen, legen Sie für jede Regel unterschiedliche Prioritäten fest und aktivieren Sie das Kontrollkästchen **Nur Zwischensumme berechnen** . Jede Steuer wird als separater Zeileneintrag angezeigt, die Steuerbeträge werden jedoch nicht addiert.

#### Informationen zu Steuerregeln

| Feld | Empfohlene Einstellung |
|--- |--- |
| Name | `Retail-Canada-GST` |
| [!UICONTROL Customer Tax Class] | `Retail Customer` |
| [!UICONTROL Product Tax Class] | `Taxable GoodsShipping` |
| [!UICONTROL Tax Rate] | `Canada-GST` |
| [!UICONTROL Priority] | `0` |
| [!UICONTROL Calculate off subtotal only] | Aktivieren Sie dieses Kontrollkästchen. |
| [!UICONTROL Sort Order] | `0` |

{style="table-layout:auto"}

### Schritt 5: Erstellen einer PST-Steuerregel für Saskatchewan

Stellen Sie für diese Steuerregel sicher, dass Sie die Priorität auf 0 setzen, und aktivieren Sie das Kontrollkästchen **Nur Zwischensumme berechnen** . Jede Steuer wird als separater Zeileneintrag angezeigt, die Steuerbeträge werden jedoch nicht addiert.

#### Informationen zu Steuerregeln

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

### Schritt 6: Ergebnisse speichern und testen

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save Config]**.

1. Kehren Sie zu Ihrer Storefront zurück und erstellen Sie eine Beispielreihenfolge, um die Ergebnisse zu testen.

## EU-Steuerkonfiguration

Das folgende Beispiel zeigt einen in Frankreich ansässigen Laden, der 100.000 Euro+ in Frankreich und 100.000 Euro+ in Deutschland verkauft.

- Steuerberechnungen werden auf Website-Ebene verwaltet.
- Die Optionen für Währungsumrechnung und Steueranzeige werden einzeln auf der Ebene der Store-Ansicht gesteuert (Aktivieren Sie das Kontrollkästchen Website verwenden , um die Standardeinstellung zu überschreiben).
- Wenn Sie das Standardsteuerland festlegen, können Sie die richtige Steuer für die Gerichtsbarkeit dynamisch anzeigen.
- Die feste Produktsteuer ist für relevante Waren als Produktattribut enthalten.
- Es kann erforderlich sein, den Katalog zu bearbeiten, um sicherzustellen, dass er in der richtigen Kategorie/Website/Store-Ansicht angezeigt wird.

### Schritt 1: Erstellen Sie drei Produktsteuerklassen

In diesem Beispiel wird davon ausgegangen, dass nicht mehrere mehrwertsteuerermäßigte Produktsteuerklassen benötigt werden.

1. Erstellen Sie eine MwSt-Standardproduktsteuerklasse.

1. Erstellen Sie eine MwSt-ermäßigte Produktsteuerklasse.

1. Erstellen Sie eine MwSt-freie Produktsteuerklasse.

### 2. Schritt: Einführung von Steuersätzen für Frankreich und Deutschland

Erstellen Sie die folgenden Steuersätze:

| Steuersätze | Einstellungen |
|--- |--- |
| Frankreich-StandardMwSt | Land: Frankreich <br/>Bundesland/-region: * <br/>Postleitzahl: * <br/>Fördersatz: 20 % |
| Frankreich - Ermäßigte Mehrwertsteuer | Land: Frankreich <br/>Bundesland/-region: * <br/>Postleitzahl: * <br/>Rate: 5% |
| Deutschland-StandardMwSt | Land: Deutschland <br/>Bundesland/-region: * <br/>Postleitzahl: * Rate: 19% |
| Deutschland - ermäßigte MwSt | Land: Deutschland <br/>Bundesland/-region: * <br/>Postleitzahl: * <br/>Fördersatz: 7% |

{style="table-layout:auto"}

### Schritt 3: Einrichten der Steuerregeln

Erstellen Sie die folgenden Steuerregeln:

| Steuervorschriften | Einstellungen |
|--- |--- |
| Einzelhandel-Frankreich-StandardVAT | Kundenklasse: Einzelhandelskunde <br/>Steuerklasse: MwSt-Standard <br/>Steuersatz: Frankreich-StandardMwSt <br/>Priorität: 0 <br/>Sortierreihenfolge: 0 |
| Einzelhandel - Frankreich - ermäßigte Mehrwertsteuer | Kundenklasse: Einzelhandelskunde <br/>Steuerklasse: Ermäßigter Mehrwertsteuersatz <br/>Steuersatz: Frankreich-Ermäßigte Mehrwertsteuer <br/>Priorität: 0 <br/>Sortierreihenfolge: 0 |
| Einzelhandel-Deutschland-StandardVAT | Kundenklasse: Einzelhandelskunde <br/>Steuerklasse: MwSt-Standard <br/>Steuersatz: Deutschland-StandardMwSt <br/>Priorität: 0 <br/>Sortierreihenfolge: 0 |
| Einzelhandel - Deutschland - ermäßigte Mehrwertsteuer | Kundenklasse: Einzelhandelskunde <br/>Steuerklasse: MwSt.-ermäßigter <br/>Steuersatz: Deutschland-ReducedVAT <br/>Priorität: 0 <br/>Sortierreihenfolge: 0 |

{style="table-layout:auto"}

### Schritt 4: Einrichten einer Store-Ansicht für Deutschland

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL All Stores]**.

1. Erstellen Sie unter der Standardwebsite eine Store-Ansicht für **[!UICONTROL Germany]**.

1. Führen Sie als Nächstes die folgenden Schritte aus:

   - Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

   - Setzen Sie oben links **[!UICONTROL Default Config]** auf den französischen Store.

   - Erweitern Sie auf der Seite Allgemein den Abschnitt **[!UICONTROL Countries Options]** um den Eintrag ![Expansion selector](../assets/icon-display-expand.png) und setzen Sie das Standardland auf `France`.

   - Füllen Sie die Gebietsschemaoptionen nach Bedarf aus.

1. Wählen Sie in der linken oberen Ecke die deutsche **[!UICONTROL Store View]** aus.

1. Erweitern Sie auf der Seite _Allgemein_ den Erweiterungs-Selektor ![ 3} **[!UICONTROL Countries Options]** und setzen Sie das Standardland auf `Germany`.](../assets/icon-display-expand.png)

1. Füllen Sie die Gebietsschemaoptionen nach Bedarf aus.

### Schritt 5: Konfiguration der Steuereinstellungen für Frankreich

Führen Sie die folgenden allgemeinen Steuereinstellungen aus:

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

### Schritt 6: Konfiguration der Steuereinstellungen für Deutschland

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Setzen Sie oben rechts **[!UICONTROL Store View]** auf die Ansicht des deutschen Stores und klicken Sie zur Bestätigung auf **[!UICONTROL OK]** .

1. Erweitern Sie im linken Bereich den Wert **[!UICONTROL Sales]** und wählen Sie **[!UICONTROL Tax]** aus.

1. Gehen Sie im Abschnitt **[!UICONTROL Default Tax Destination Calculation]** wie folgt vor:

   - Deaktivieren Sie das Kontrollkästchen **[!UICONTROL Use Website]** nach jedem Feld.

   - Aktualisieren Sie die folgenden Werte, um die Versandeinstellungen [des Herkunftspunkts](shipping-settings.md#point-of-origin) Ihrer Site anzupassen:

      - Standardland
      - Standardstatus
      - Post-Standardcode

     Diese Einstellung stellt sicher, dass die Steuer korrekt berechnet wird, wenn die Produktpreise die Steuer enthalten.

     ![Berechnung des steuerlichen Ziels ](./assets/destination-calc-french.png){width="600" zoomable="yes"}

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save Config]**.

[1]: https://www.revenuquebec.ca/en/businesses/
[2]: https://www.saskatchewan.ca/finance
[3]: https://www.gov.mb.ca/finance/taxation/bulletins/004.pdf
