---
title: Tabellenversand
description: Erfahren Sie, wie Sie eine Versandoption mit Tabellenraten für Ihren Store einrichten.
exl-id: f73adc9a-4c6c-477d-9553-3a3f28647bdd
feature: Shipping/Delivery
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '999'
ht-degree: 3%

---

# Tabellenversand

Die _Tabellenrate_ Die Versandmethode verweist auf eine Datentabelle, um Versandtarife anhand einer Kombination von Bedingungen zu berechnen, darunter:

- Gewichtung v. Ziel
- Preis v. Ziel
- Anzahl der Elemente v. Ziel

Wenn Ihr Lager beispielsweise in Los Angeles liegt, kostet es weniger, nach San Diego zu verschicken als nach Vermont. Sie können den Versand von Tabellen verwenden, um die Einsparungen an Ihre Kunden weiterzugeben.

Die Daten, die zur Berechnung der Tabellenraten verwendet werden, werden in einer Tabelle vorbereitet und in Ihren Speicher importiert. Wenn der Kunde ein Angebot anfordert, werden die Ergebnisse im Abschnitt Versandschätzung des Warenkorbs angezeigt.

>[!NOTE]
>
>Es kann jeweils nur ein Datensatz mit Tabellenraten aktiv sein.

![Versandoption &quot;Tabellenrate&quot;in der Zusammenfassung der Warenkorbbestellungen](./assets/storefront-cart-table-rate.png){width="700" zoomable="yes"}

## Schritt 1: Standardeinstellungen festlegen

Der erste Schritt besteht darin, die Standardeinstellungen für Tabellenraten abzuschließen. Sie können diesen Schritt abschließen, ohne den Umfang der Konfiguration zu ändern.

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Im _[!UICONTROL Sales]_Wählen Sie im linken Bereich **[!UICONTROL Delivery Methods]**.

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL Table Rates]** Abschnitt.

   >[!NOTE]
   >
   >Bei Bedarf muss zunächst die **[!UICONTROL Use system value]** aktivieren, um die folgenden Einstellungen wie beschrieben zu ändern.

   ![Tabellenraten](../configuration-reference/sales/assets/delivery-methods-table-rates.png){width="600" zoomable="yes"}

1. Satz **[!UICONTROL Enabled]** nach `Yes`.

1. Geben Sie die **[!UICONTROL Title]** die Sie beim Checkout für den Bereich Tabellenraten anzeigen möchten.

   Der Standardtitel lautet `Best Way`.

1. Geben Sie die **[!UICONTROL Method Name]** die als Beschriftung neben der berechneten Rate im Warenkorb angezeigt werden sollen.

1. Satz **[!UICONTROL Condition]** einer der folgenden Berechnungsmethoden:

   - `Weight v. Destination`
   - `Price v. Destination`
   - `Number of Items v. Destination`

1. Für Bestellungen, die virtuelle Produkte beinhalten, legen Sie **[!UICONTROL Include Virtual Products in Price Calculation]** nach `Yes` , wenn Sie die virtuellen Produkte in die Berechnung einbeziehen möchten.

   >[!NOTE]
   >
   >Da virtuelle Produkte - wie z. B. Dienste - keine Gewichtung haben, können sie das Ergebnis einer Berechnung nicht ändern, die auf der Bedingung Gewicht v Ziel basiert. Virtual Produkte können jedoch das Ergebnis einer Berechnung ändern, die entweder auf der Bedingung Preis v. Ziel oder Anzahl der Elemente vs. Ziel basiert.

1. Konfigurieren Sie die Optionen für die Bearbeitungsgebühr entsprechend Ihren Anforderungen.

   Die Bearbeitungsgebühr ist optional und erscheint als zusätzliche Gebühr, die zu den Versandkosten hinzukommt. Wenn Sie eine Bearbeitungsgebühr einbeziehen möchten, gehen Sie wie folgt vor:

   - Satz **[!UICONTROL Calculate Handling Fee]**:

      - `Fixed`
      - `Percent`

   - Geben Sie die **[!UICONTROL Handling Fee]** Tarif nach der Methode zur Berechnung der Gebühr.

     Wenn die Gebühr beispielsweise auf einer festen Gebühr basiert, geben Sie den Betrag als Dezimalzahl ein, z. B. `4.90`. Wenn die Bearbeitungsgebühr jedoch auf einem Prozentsatz der Bestellung basiert, geben Sie den Betrag als Prozentsatz an. Wenn Sie beispielsweise sechs Prozent der Bestellung aufladen, geben Sie den Wert als `.06`.

1. Ändern Sie bei Bedarf die **[!UICONTROL Displayed Error Message]**.

   Dieses Textfeld enthält eine Standardnachricht. Sie können jedoch eine andere Nachricht eingeben, die angezeigt werden soll, wenn diese Versandmethode nicht mehr verfügbar ist.

1. Satz **[!UICONTROL Ship to Applicable Countries]**:

   - `All Allowed Countries` - Kunden von allen [Länder](../getting-started/store-details.md#country-options) Diese in Ihrer Store-Konfiguration angegebene Versandmethode kann verwendet werden.
   - `Specific Countries` - Wenn Sie diese Option wählen, wird die _[!UICONTROL Ship to Specific Countries]_angezeigt. Wählen Sie jedes Land in der Liste aus, in dem diese Versandmethode verwendet werden kann.

1. Satz **[!UICONTROL Show Method if Not Applicable]** nach `Yes` wenn Sie die Tabellenzahlen immer anzeigen möchten

1. Für **[!UICONTROL Sort Order]** Geben Sie eine Zahl ein, um die Reihenfolge zu bestimmen, in der der Tabellenquotenversand angezeigt wird, wenn er beim Checkout mit anderen Versandmethoden aufgelistet wird.

   `0` = first, `1` = Sekunde, `2` = drittes Element usw.

1. Klicken **[!UICONTROL Save Config]**.

## Schritt 2: Tabellensatzdaten vorbereiten

1. Legen Sie in der oberen linken Ecke **[!UICONTROL Store View]** nach `Main Website`oder auf jeder anderen Website, auf der die Konfiguration angewendet wird.

   >[!NOTE]
   >
   >Heben Sie bei Bedarf die Auswahl der **[!UICONTROL Use system value]** aktivieren, um die folgenden Einstellungen wie beschrieben zu ändern.

1. Ändern Sie die **[!UICONTROL Condition]** nach Bedarf.

1. Klicken **[!UICONTROL Export CSV]**.

   ![CSV exportieren](./assets/shipping-table-rates-export.png){width="700" zoomable="yes"}

1. Speichern Sie die `tablerates.csv` -Datei auf Ihr System.

1. Öffnen Sie die Datei in einer Tabellenkalkulationsanwendung.

1. Füllen Sie die Tabelle mit den entsprechenden Werten für die Versandberechnungsbedingung aus.

   - Verwenden Sie ein Sternchen (*) als Platzhalter, der alle in einer Kategorie möglichen Werte darstellt.
   - Die _[!UICONTROL Country]_-Spalte muss [gültiger dreistelliger Code][1] für jede Zeile.
   - Sortieren Sie die Daten nach _[!UICONTROL Region/State]_sodass sich die jeweiligen Standorte oben in der Liste und die Platzhalterstandorte unten befinden. Bei Verwendung dieser Methode werden die Regeln zuerst mit den absoluten Werten und später mit den Platzhalterwerten verarbeitet.
   - Werte in der _[!UICONTROL Weight (and above)]_kann maximal vier Dezimalstellen haben (z. B. `2.5075`). Wenn Sie mehr Dezimalstellen in den Daten verwenden, schlägt der Import fehl.

   ![Gewichtung vs. Ziel (Australien)](./assets/table-rates-weight-destination-csv.png){width="500"}

1. Speichern Sie die `tablerates.csv` -Datei.

## 3. Schritt: Tabellensatzdaten importieren

1. Kehren Sie zu **[!UICONTROL Table Rates]** -Abschnitt Ihrer Store-Konfiguration.

1. Legen Sie in der oberen linken Ecke **[!UICONTROL Store View]** auf der Website, auf der diese Methode verwendet wird.

1. Für **[!UICONTROL Import]** klicken **[!UICONTROL Choose File]** und wählen Sie abgeschlossene `tablerates.csv` -Datei, um die Tarife zu importieren.

   ![Importieren von Tabellenraten](./assets/shipping-table-rates-import.png){width="600" zoomable="yes"}

1. Klicken **[!UICONTROL Save Config]**.

## Schritt 4: Überprüfen der Raten

Um sicherzustellen, dass die Daten der Tabellenrate korrekt sind, gehen Sie den Zahlungsprozess mit mehreren unterschiedlichen Adressen durch, um sicherzustellen, dass die Versand- und Bearbeitungsraten korrekt berechnet werden.

### Beispiel 1: Preis und Ziel

In diesem Beispiel wird die Bedingung Preis v. Ziel verwendet, um eine Reihe von drei verschiedenen Versandtarifen zu erstellen, basierend auf der Menge der Auftragsubsumme für die kontinentalen Vereinigten Staaten, Alaska und Hawaii. Das Sternchen (*) ist ein Platzhalter, der alle Werte darstellt.

| LAND | REGION/STAAT | Postleitzahl | BESTELLUNGS-ZWISCHENSUMME (und höher) | VERSANDPREIS |
|--- |--- |--- |--- |--- |
| USA | HI | * | 100 | 10 |
| USA | HI | * | 50 | 15 |
| USA | HI | * | 0 | 20 |
| USA | AK | * | 100 | 10 |
| USA | AK | * | 50 | 15 |
| USA | AK | * | 0 | 20 |
| USA | * | * | 100 | 5 |
| USA | * | * | 50 | 10 |
| USA | * | * | 0 | 15 |

{style="table-layout:auto"}

### Beispiel 2: Gewichtung und Ziel

In diesem Beispiel wird die Bedingung Gewicht v. Ziel verwendet, um basierend auf der Gewichtung der Bestellung unterschiedliche Versandraten zu erstellen.

| LAND | REGION/STAAT | Postleitzahl | GEWICHT (und höher) | VERSANDPREIS |
|--- |--- |--- |--- |--- |
| AUS | NT | * | 9 | 39.95 |
| AUS | NT | * | 0 | 19.95 |
| AUS | VIC | * | 9 | 19.95 |
| AUS | VIC | * | 0 | 5.95 |
| AUS | WA | * | 9 | 39.95 |
| AUS | WA | * | 0 | 19.95 |
| AUS | * | * | 9 | 29.95 |
| AUS | * | * | 0 | 9.95 |

{style="table-layout:auto"}

### Beispiel 3: Beschränkung des freien Seeverkehrs auf die kontinentalen Vereinigten Staaten

1. Erstellen Sie eine `tablerates.csv` -Datei, die alle Staatsziele enthält, für die Sie einen kostenlosen Versand bereitstellen möchten.

1. Schließen Sie die Konfiguration der Tabellenrate mit den folgenden Einstellungen ab:

   | Einstellung | Wert |
   |----------|-------|
   | [!UICONTROL Condition] | `Price v. Destination` |
   | [!UICONTROL Method Name] | `Free Shipping` |
   | [!UICONTROL Ship to Applicable Countries] | `Specific Countries` |
   | [!UICONTROL Ship to Specific Countries] | `Select only United States` |
   | [!UICONTROL Show method if not applicable] | `No` |

   {style="table-layout:auto"}

1. Legen Sie in der oberen linken Ecke **[!UICONTROL Store View]** nach `Main Website`oder auf jeder anderen Website, auf der die Konfiguration angewendet wird.

1. Für **[!UICONTROL Import]** klicken **[!UICONTROL Choose File]** und wählen Sie abgeschlossene `tablerates.csv` -Datei, um die Tarife zu importieren.


[1]: https://en.wikipedia.org/wiki/ISO_3166-1_alpha-3
