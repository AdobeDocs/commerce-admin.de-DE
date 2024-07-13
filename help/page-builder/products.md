---
title: Inhalt hinzufügen - Produkte
description: Erfahren Sie mehr über den Inhaltstyp Produkte , der zum Hinzufügen einer Liste von Produkten zur Phase [!DNL Page Builder] verwendet wird.
exl-id: 8ef38669-a6f6-493b-b963-b0fc4e3bbff4
feature: Page Builder, Page Content, Products
source-git-commit: 167e9d906cebb645f76a5112fa629a73ba823ebc
workflow-type: tm+mt
source-wordcount: '1913'
ht-degree: 0%

---

# Inhalt hinzufügen - Produkte

Verwenden Sie den Inhaltstyp _Produkte_ , um der [[!DNL Page Builder] Bühne](workspace.md#stage) eine Liste von Produkten hinzuzufügen, indem Sie entweder ein Raster- oder ein Karusselllayout verwenden. Verwenden Sie das Tool [Inhalt hinzufügen - Block](block.md) , um den Block auf der [!DNL Page Builder] -Bühne zu platzieren und dann eine Produktliste innerhalb des Blocks zu platzieren. Alternativ können Sie die Produktliste direkt in einer Zeile auf einer Seite hinzufügen.

## Richtlinien für die Verwendung des Produktkarussells

Das Produktkarussell bietet eine leistungsstarke und ansprechende Möglichkeit, Ihre Produkte anzuzeigen. Die folgenden Richtlinien werden empfohlen, um das bestmögliche Ergebnis zu erzielen:

- Fügen Sie Produktkarussells direkt zu Seitenbreitenbehältern wie Zeilen, Registerkarten oder einspaltigen Layouts hinzu. Die Verwendung von Layouts mit Seitenbreite gewährleistet die optimale responsive Anzeige Ihrer Produkte. [!DNL Page Builder] reduziert die Anzahl der angezeigten Produkte in Abhängigkeit von der Breite der Seite und nicht von der Breite des Containers.

- Fügen Sie einer schmalen Spalte kein Produktkarussell hinzu. Wie bereits erwähnt, bestimmt [!DNL Page Builder] standardmäßig die Anzahl der anzuzeigenden Produkte basierend auf der Seitenbreite und nicht auf der Spaltenbreite.

- Wenn Sie möchten, dass Ihr Produktkarussell kontinuierlich automatisch scrollt, setzen Sie sowohl **[!UICONTROL Autoplay]** als auch **[!UICONTROL Infinite Loop]** auf `Yes`. Wenn &quot;Autoplay&quot;auf &quot;`Yes`&quot;festgelegt ist, die &quot;Unendliche Schleife&quot;jedoch auf &quot;`No`&quot;gesetzt ist, stoppt der automatische Bildlauf am Ende Ihrer Produktliste.

- Setzen Sie die **[!UICONTROL Carousel Mode]** auf `Continuous`, um ein Produkt gleichzeitig im Karussell hervorzuheben, zu zentrieren und zu scrollen. Die anderen Produkte sind in der Liste sichtbar, aber transparent, um das zentrierte Produkt hervorzuheben.

  ![Produktliste im kontinuierlichen Karussellmodus](./assets/pb-products-settings-carousel-continuous.png){width="600"}

- Um bis zu fünf Produkte gleichzeitig im Karussell anzuzeigen und zu scrollen, halten Sie die **[!UICONTROL Carousel Mode]** auf `Default` eingestellt.

  ![Produktliste im standardmäßigen Karussellmodus](./assets/pb-products-settings-carousel-default.png){width="600"}

Die folgenden Anweisungen zeigen, wie Sie einem Baustein eine Produktliste hinzufügen. Anschließend können Sie das Widget [widget](../content-design/widgets.md) verwenden, um den Block an einer bestimmten Stelle auf einer beliebigen Seite in Ihrem Store zu platzieren.

{{$include /help/_includes/page-builder-save-timeout.md}}

## Produkt-Toolbox

| Tool | Symbol | Beschreibung |
| --------- | ------------- | ----------------- |
| Verschieben | ![Symbol &quot;Verschieben&quot;](./assets/pb-icon-move.png){width="25"} | Verschiebt den Produkt-Container und seinen Inhalt an eine andere Position auf der Bühne. |
| Einstellungen | ![Einstellungssymbol](./assets/pb-icon-settings.png){width="25"} | Öffnet die Seite _Produkte bearbeiten_ , auf der Sie die Produktliste auswählen und die Eigenschaften des Containers ändern können. |
| Ausblenden | ![Symbol zum Ausblenden](./assets/pb-icon-hide.png){width="25"} | Blendet den aktuellen Produkt-Container und seinen Inhalt aus. |
| Anzeigen | ![Symbol &quot;Anzeigen&quot;](./assets/pb-icon-show.png){width="25"} | Zeigt den ausgeblendeten Produktbehälter und seinen Inhalt an. |
| Duplizieren | ![Symbol &quot;Duplizieren&quot;](./assets/pb-icon-duplicate.png){width="25"} | Kopiert den Produktcontainer und seinen Inhalt. |
| Entfernen | ![Symbol &quot;Entfernen&quot;](./assets/pb-icon-remove.png){width="25"} | Löscht den Produkt-Container und seinen Inhalt aus der Phase. |

{style="table-layout:auto"}

{{$include /help/_includes/page-builder-hidden-element-note.md}}

## Produktlistenbaustein erstellen

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Blocks]**.

1. Klicken Sie auf **[!UICONTROL Add New Block]**.

1. Geben Sie die Werte **[!UICONTROL Block Title]** und **[!UICONTROL Identifier]** ein.

1. Wählen Sie die **[!UICONTROL Store View]** aus, wo der Block verfügbar sein soll.

1. Scrollen Sie nach unten und klicken Sie auf **[!UICONTROL Edit with Page Builder]** oder innerhalb des Inhaltsvorschaubereichs, um den Arbeitsbereich [!DNL Page Builder] zu öffnen.

1. Erweitern Sie im Bedienfeld [!DNL Page Builder] den Wert **[!UICONTROL Add Content]** und ziehen Sie einen Platzhalter **[!UICONTROL Products]** auf die Bühne.

   ![Hinzufügen des Inhaltstyps &quot;Produkte&quot;](./assets/pb-add-content-products-drag.png){width="600" zoomable="yes"}

## Konfigurieren des Produktlistencontainers

Bewegen Sie den Mauszeiger über den leeren Behälter _Produkte_ , um die Toolbox anzuzeigen, und klicken Sie auf das Symbol _Einstellungen_ (![Einstellungssymbol](./assets/pb-icon-settings.png){width="20"} ).

![Produktsymbolleiste](./assets/pb-add-content-products-toolbox.png){width="500" zoomable="yes"}

Füllen Sie die _Einstellungen_ gemäß den folgenden Abschnitten aus:

### Erscheinungsbild

1. Um zu bestimmen, wie die Produktliste auf der Seite angezeigt wird, wählen Sie einen der folgenden Darstellungstypen aus:

   | Typ | Beschreibung |
   | ---- | ----------- |
   | Produktraster | Zeigt die Produkte in einem Raster an, das (standardmäßig) fünf Produkte pro Zeile anzeigt und so viele Zeilen enthält, wie für die Anzeige der in der Einstellung &quot;**[!UICONTROL Number of Products to Display]**&quot; eingegebenen Zahl erforderlich sind. |
   | Karussell | Zeigt die Produkte in einem Karussell an (auch als Regler bezeichnet). Das Karussell zeigt bis zu fünf Produkte pro Folie. <br/><br/>**Reaktionswarnung**: Wenn Sie dieses Erscheinungsbild auswählen, ist es am besten, den Inhaltstyp &quot;Produkte&quot;direkt zu einem Zeilen-, Tab- oder einspaltigen Layout hinzuzufügen, wo er responsiv ist, wobei auf kleineren Bildschirmen weniger Produkte pro Seite angezeigt werden. Wenn Sie sie zu Content-Typen hinzufügen, die kleiner als die Breite der Seite sind (z. B. eine schmale Spalte), zeigt das Karussell mehr Produkte pro Folie an, als der Container zulässt, unabhängig von der Bildschirmgröße. |

   {style="table-layout:auto"}

   ![Produkterscheinung](./assets/pb-products-appearances.png){width="300"}

   Wenn Sie das Karussell auswählen, müssen Sie auch die [Karusselleinstellungen](#carousel-settings) konfigurieren.

1. Wählen Sie für &quot;**[!UICONTROL Select Products By]**&quot;die Methode für die Produktauswahl:

   Sie können Ihre Produkte nach Kategorie, SKU oder Bedingung auswählen. Diese Optionen schließen sich gegenseitig aus. Sie können beispielsweise nicht die Option Kategorie auswählen, die Auswahl Kategorie verwenden und dann zur Option Bedingung wechseln, um einige Bedingungen hinzuzufügen. Ihre Produkte werden nur basierend auf dem ausgewählt, was Sie für _eine_ dieser drei Optionen festgelegt haben.

   - **[!UICONTROL Category]** - Wählen Sie diese Option, um Produkte mit einer ausgewählten Kategorie anzuzeigen.

     ![Produktauswahl nach Kategorie](./assets/pb-products-settings_category.png){width="500"}

     Wenn diese Option aktiviert ist, wird der Selektor **[!UICONTROL Category]** angezeigt. Klicken Sie auf den Pfeil und führen Sie einen Drilldown durch, um die Kategorie der anzuzeigenden Produkte auszuwählen. Beispielsweise werden in den Beispieldaten [!DNL Commerce] beim Einbohren und Auswählen von _Frauen > Tops > Tees_ alle Produkte für diese Kategorie angezeigt.

     ![Auswählen einer Katalogkategorie](./assets/pb-select-products-by-category.png){width="500"}

   - **[!UICONTROL SKU]** - Wählen Sie diese Option, um Produkte mit einer oder mehreren SKUs anzuzeigen.

     Wenn diese Option aktiviert ist, wird das Textfeld &quot;**[!UICONTROL Product SKUs]**&quot;angezeigt, in das Sie eine kommagetrennte Liste der anzuzeigenden SKUs eingeben müssen.

     ![Produktauswahl nach SKU](./assets/pb-products-settings_sku.png){width="500"}

   - **[!UICONTROL Condition]** - Wählen Sie diese Option, um Produkte gemäß einer oder mehreren von Ihnen definierten Bedingungen anzuzeigen.

     Wenn diese Option aktiviert ist, stehen Tools zum Hinzufügen von Bedingungen zur Produktauswahl zur Verfügung. Sie können beispielsweise nur Produkte auswählen, deren Geschlecht auf &quot;Unisex&quot;eingestellt ist.

     ![Produktauswahl nach Bedingung](./assets/pb-products-settings_condition.png){width="500"}

     >[!NOTE]
     >
     >Wenn Sie die Option Kategorie oder SKU auswählen, erhalten Sie die Option **[!UICONTROL Sort By]** von `Position`. Bei dieser Sortieroption werden die Produkte in derselben Reihenfolge angezeigt wie in Ihrem Katalog.</br>
     >
     >Bei der Option Kategorie zeigt die Sortierung nach Position die Produkte in derselben Reihenfolge an, in der sie in Ihrem Katalog angezeigt werden. Bei der SKU-Option zeigt die Sortierung nach Position die Produkte in der Reihenfolge an, in der Sie sie im Textfeld **[!UICONTROL Product SKUs]** eingeben.

1. Wählen Sie für **[!UICONTROL Sort By]** die Sortierreihenfolge für die Produkte in der Liste aus:

   | Option | Beschreibung |
   | ------ | ----------- |
   | `Position` (nur für Kategorie- und SKU-Optionen) | Wenn Sie die Option Kategorie auswählen, zeigt die Position Produkte in derselben Reihenfolge an wie ihre Position im Katalog. Wenn Sie die SKU-Option auswählen, zeigt die Position Produkte in derselben Reihenfolge an wie die SKUs im Textfeld Produkt-SKUs . |
   | `Newest products first` | Sortiert Produkte nach dem Datum, an dem sie zum Katalog hinzugefügt wurden, und zeigt zuerst die Produkte mit den neuesten Eintragsdaten an. |
   | `Oldest products first` | Sortiert Produkte nach dem Datum, an dem sie zum Katalog hinzugefügt wurden, und zeigt zuerst die Produkte mit den ältesten Eintragsdaten an. |
   | `Name: A - Z` | Sortiert Produkte in alphabetischer Reihenfolge. |
   | `Name: Z - A` | Sortiert Produkte in umgekehrter alphabetischer Reihenfolge. |
   | `SKU: ascending` | Sortiert Produkte nach SKU in alphanumerischer Reihenfolge. |
   | `SKU: descending` | Sortiert Produkte nach SKU in umgekehrter alphanumerischer Reihenfolge. |
   | `Stock: low stock first` | Sortiert Produkte vom niedrigsten zum höchsten verfügbaren Lager. |
   | `Stock: high stock first` | Sortiert Produkte vom höchsten zum niedrigsten verfügbaren Lager. |
   | `Price: high to low` | Sortiert Produkte vom höchsten zum niedrigsten Preis. |
   | `Price: low to high` | Sortiert Produkte vom niedrigsten zum höchsten Preis. |

   {style="table-layout:auto"}

   ![Produktsortierungsoptionen](./assets/pb-products-sortby.png){width="300"}

1. Geben Sie den Wert **[!UICONTROL Number of Products to Display]** in das Karussell oder Raster ein.

   Die Werte können zwischen `1` und `999` liegen. Der Standardwert ist `5` für ein Raster und `20` für ein Karussell.

   >[!NOTE]
   >
   >Einige Produkte in den Einstellungen für Kategorie, SKU oder Bedingung werden möglicherweise nicht in Ihrem Produktraster oder Karussell angezeigt. So werden zum Beispiel nicht vorhandene Produkte, als nicht sichtbar markierte Produkte, nicht vorrätige Produkte und Produkte, die einer anderen Website zugewiesen sind, nicht angezeigt.

   >[!IMPORTANT]
   >
   >Die Preise für konfigurierbare, gruppierte und gebündelte (dynamische Preise) Produkte sind im Admin nicht definiert. Daher werden diese Produkte nicht im **[!UICONTROL Preview]** angezeigt, wenn die Produkte nach Preis gefiltert werden. Diese Produkte können nicht richtig im **[!UICONTROL Preview]** bestellt werden, wenn sie nach Preis sortiert sind.

### Karusselleinstellungen

1. Um zu bestimmen, wie die Produkte im Karussell angezeigt werden, wählen Sie den Wert **[!UICONTROL Carousel Mode]**:

   | Option | Beschreibung |
   | ------ | ----------- |
   | `Default` | Das Karussell zeigt standardmäßig fünf Produkte pro Folie an und reduziert diese Anzahl nach Bedarf responsiv. |
   | `Continuous` | Das Karussell zeigt standardmäßig fünf Produkte pro Folie an (mit der Hälfte eines Produkts auf der rechten und linken Seite), zentriert und scrollt jedoch jeweils ein Produkt in einer Endlosschleife. Produkte links und rechts vom zentrierten Produkt werden abgeblendet dargestellt, sodass das mittlere Produkt hervorgehoben wird. |

   {style="table-layout:auto"}

   Wenn Sie zwischen diesen beiden Modi wechseln, werden die anderen Karusselleinstellungen beibehalten, mit Ausnahme der Einstellung &quot;**[!UICONTROL Infinite Loop]**&quot;, die im kontinuierlichen Modus immer auf &quot;`Yes`&quot; gesetzt und das Feld deaktiviert ist.

   ![Karusselleinstellungen](./assets/pb-products-carousel-settings.png){width="600" zoomable="yes"}

1. Setzen Sie bei Bedarf die Option **[!UICONTROL Autoplay]** auf `Yes`.

   Wenn die automatische Wiedergabe aktiviert ist, beginnt das Karussell beim Laden der Seite automatisch mit dem Scrollen. Wenn Sie die Standardeinstellung (`No`) beibehalten, muss der Kunde auf die Foliennavigation (Punkte oder Pfeile) klicken, um jede Folie nacheinander anzuzeigen.

   Wenn Sie diese Funktion aktivieren, geben Sie **[!UICONTROL Autoplay Speed]** ein, um die Verzögerung in Millisekunden zwischen den einzelnen Folien anzugeben. Der Standardwert ist `4000` (4 Sekunden).

1. Setzen Sie bei Bedarf die Option **[!UICONTROL Infinite Loop]** auf `Yes`.

   Wenn die Endlosschleife aktiviert ist, wird die Diashow unbegrenzt wiederholt, während die Seite geöffnet ist. Wenn Sie die Standardeinstellung (`No`) beibehalten, wird die Diashow nur einmal wiedergegeben.

   >[!NOTE]
   >
   >Wenn Sie **[!UICONTROL Infinite Loop]** auf `No` und **[!UICONTROL Autoplay]** auf `Yes` setzen, stoppt die automatische Wiedergabe am Ende der Anzahl der anzuzeigenden Produkte.

1. Setzen Sie bei Bedarf die Option **[!UICONTROL Show Arrows]** auf `Yes`.

   Wenn diese Option aktiviert ist, enthält jede Folie die Navigationspfeile &quot;_next_&quot;und &quot;_previous_&quot;auf der linken und rechten Seite. Wenn Sie die Standardeinstellung (`No`) beibehalten, werden auf den Folien keine Navigationspfeile angezeigt.

1. Setzen Sie bei Bedarf die Option **[!UICONTROL Show Dots]** auf `No`.

   Wenn die Standardeinstellung (`Yes`) festgelegt ist, werden die Navigationspunkte unten im Karussell-Schieberegler angezeigt. Wenn Sie diese Einstellung deaktivieren, zeigt der Karussellregler keine Navigationspunkte an.

### Erweitert

1. Um die Positionierung der Liste &quot;Products&quot;innerhalb des übergeordneten Containers zu steuern, wählen Sie den Wert **[!UICONTROL Alignment]** aus:

   | Option | Beschreibung |
   | ------ | ----------- |
   | `Default` | Wendet die Standardeinstellung für die Ausrichtung an, die im Stylesheet des aktuellen Designs angegeben ist. |
   | `Left` | Richtet die Liste am linken Rand des übergeordneten Containers aus, wobei der angegebene Abstand berücksichtigt wird. |
   | `Center` | Richtet die Liste in der Mitte des übergeordneten Containers aus, wobei der angegebene Abstand berücksichtigt wird. |
   | `Right` | Richtet die Liste am rechten Rand des übergeordneten Containers aus, wobei der angegebene Abstand berücksichtigt wird. |

   {style="table-layout:auto"}

1. Legen Sie den **[!UICONTROL Border]** -Stil fest, der auf alle vier Seiten des Container &quot;Products&quot;angewendet wird:

   | Option | Beschreibung |
   | ------ | ----------- |
   | `Default` | Wendet den standardmäßigen Randstil an, der vom zugehörigen Stylesheet angegeben wird. |
   | `None` | liefert keine sichtbare Anzeige der Containergrenzen. |
   | `Dotted` | Der Container-Rahmen wird als gepunktete Linie angezeigt. |
   | `Dashed` | Der Container-Rahmen wird als gestrichelte Linie angezeigt. |
   | `Solid` | Der Container-Rahmen wird als durchgehende Linie angezeigt. |
   | `Double` | Der Container-Rahmen wird als doppelte Linie angezeigt. |
   | `Groove` | Der Container-Rahmen wird als Rillenlinie angezeigt. |
   | `Ridge` | Der Container-Rahmen wird als gekürzte Linie angezeigt. |
   | `Inset` | Der Container-Rahmen wird als Inset-Zeile angezeigt. |
   | `Outset` | Der Container-Rahmen wird als Ausgangspunkt angezeigt. |

   {style="table-layout:auto"}

1. Wenn Sie einen anderen Rahmenstil als `None` festlegen, füllen Sie die Anzeigeoptionen für die Rahmenanzeige aus:

   | Option | Beschreibung |
   | ------ |------------ |
   | [!UICONTROL Border Color] | Geben Sie die Farbe an, indem Sie ein Muster auswählen, auf die Farbauswahl klicken oder einen gültigen Farbnamen oder einen entsprechenden Hexadezimalwert eingeben. |
   | [!UICONTROL Border Width] | Geben Sie die Anzahl Pixel für die Rahmenlinienbreite an. |
   | [!UICONTROL Border Radius] | Geben Sie die Anzahl der Pixel an, um die die Größe des Radius definiert wird, mit dem die einzelnen Ecken des Rands gerundet werden. |

   {style="table-layout:auto"}

1. (Optional) Geben Sie die Namen von **[!UICONTROL CSS classes]** aus dem aktuellen Stylesheet an, das auf den Container angewendet werden soll.

   Trennen Sie mehrere Klassennamen durch ein Leerzeichen.

1. Geben Sie Werte in Pixel für den Wert **[!UICONTROL Margins and Padding]** ein, um die äußeren Ränder und den inneren Abstand des Containers &quot;Products&quot;zu bestimmen.

   Geben Sie die entsprechenden Werte in das Diagramm ein.

   | Container-Bereich | Beschreibung |
   | -------------- | ----------- |
   | [!UICONTROL Margins] | Die Menge an leerem Raum, die auf den äußeren Rand aller Seiten des Containers angewendet wird. Optionen: `Top` / `Right` / `Bottom` / `Left` |
   | [!UICONTROL Padding] | Die Menge an leerem Raum, die auf den inneren Rand aller Seiten des Containers angewendet wird. Optionen: `Top` / `Right` / `Bottom` / `Left` |


## Speichern und Vorschau auf der Bühne anzeigen

Klicken Sie oben rechts auf **[!UICONTROL Save]** , um die Einstellungen anzuwenden und zum Arbeitsbereich [!DNL Page Builder] zurückzukehren.

Wenn Sie ein Produktkarussell konfiguriert haben, sollte es in etwa wie im folgenden Beispiel aussehen:

![Karussell auf der Bühne](./assets/pb-products-admin-carousel.png){width="600"}

Sie können jetzt ein [Widget](../content-design/widgets.md) verwenden, um diesen Block an die Stelle zu setzen, an der er im Store angezeigt werden soll. Sie können auch [Inhalt hinzufügen - Block](block.md) verwenden, um den Baustein zu einer vorhandenen Seite, Registerkarte oder Baustein hinzuzufügen.
