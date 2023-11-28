---
title: Inhalt hinzufügen - Produkte
description: Erfahren Sie mehr über den Inhaltstyp Produkte , der zum Hinzufügen einer Liste von Produkten zum [!DNL Page Builder] Bühne.
exl-id: 8ef38669-a6f6-493b-b963-b0fc4e3bbff4
feature: Page Builder, Page Content, Products
source-git-commit: 167e9d906cebb645f76a5112fa629a73ba823ebc
workflow-type: tm+mt
source-wordcount: '1912'
ht-degree: 0%

---

# Inhalt hinzufügen - Produkte

Verwenden Sie die _Produkte_ Inhaltstyp , um der [[!DNL Page Builder] Schritt](workspace.md#stage), entweder mit einem Raster- oder Karusselllayout. Verwenden Sie die [Inhalt hinzufügen - Block](block.md) -Tool, um den Block auf der [!DNL Page Builder] und fügen Sie dann eine Produktliste in den Block ein. Alternativ können Sie die Produktliste direkt in einer Zeile auf einer Seite hinzufügen.

## Richtlinien für die Verwendung des Produktkarussells

Das Produktkarussell bietet eine leistungsstarke und ansprechende Möglichkeit, Ihre Produkte anzuzeigen. Die folgenden Richtlinien werden empfohlen, um das bestmögliche Ergebnis zu erzielen:

- Fügen Sie Produktkarussells direkt zu Seitenbreitenbehältern wie Zeilen, Registerkarten oder einspaltigen Layouts hinzu. Die Verwendung von Layouts mit Seitenbreite gewährleistet die optimale responsive Anzeige Ihrer Produkte. [!DNL Page Builder] verringert die Anzahl der angezeigten Produkte in Abhängigkeit von der Breite der Seite und nicht von der Breite des Containers.

- Fügen Sie einer schmalen Spalte kein Produktkarussell hinzu. Wie bereits erwähnt [!DNL Page Builder]bestimmt standardmäßig die Anzahl der anzuzeigenden Produkte basierend auf der Seitenbreite, nicht auf der Spaltenbreite.

- Wenn Sie möchten, dass das Produktkarussell kontinuierlich automatisch scrollt, legen Sie beide fest. **[!UICONTROL Autoplay]** und **[!UICONTROL Infinite Loop]** nach `Yes`. Wenn die automatische Wiedergabe auf `Yes` aber Unendliche Schleife auf `No`, stoppt der automatische Bildlauf am Ende Ihrer Produktliste.

- Legen Sie die **[!UICONTROL Carousel Mode]** nach `Continuous` , um ein Produkt im Karussell einzeln hervorzuheben, zu zentrieren und zu scrollen. Die anderen Produkte sind in der Liste sichtbar, aber transparent, um das zentrierte Produkt hervorzuheben.

  ![Produktliste im kontinuierlichen Karussellmodus](./assets/pb-products-settings-carousel-continuous.png){width="600"}

- Um bis zu fünf Produkte gleichzeitig im Karussell anzuzeigen und zu scrollen, halten Sie die **[!UICONTROL Carousel Mode]** auf `Default`.

  ![Produktliste im standardmäßigen Karussellmodus](./assets/pb-products-settings-carousel-default.png){width="600"}

Die folgenden Anweisungen zeigen, wie Sie einem Baustein eine Produktliste hinzufügen. Sie können dann eine [Widget](../content-design/widgets.md) , um den Block an einer bestimmten Stelle auf einer beliebigen Seite in Ihrem Geschäft zu platzieren.

{{$include /help/_includes/page-builder-save-timeout.md}}

## Produkt-Toolbox

| Tool | Symbol | Beschreibung |
| --------- | ------------- | ----------------- |
| Verschieben | ![Symbol Verschieben](./assets/pb-icon-move.png){width="25"} | Verschiebt den Produkt-Container und seinen Inhalt an eine andere Position auf der Bühne. |
| Einstellungen | ![Symbol Einstellungen](./assets/pb-icon-settings.png){width="25"} | Öffnet die _Produkte bearbeiten_ Seite, auf der Sie die Produktliste auswählen und die Eigenschaften des Containers ändern können. |
| Ausblenden | ![Symbol &quot;Ausblenden&quot;](./assets/pb-icon-hide.png){width="25"} | Blendet den aktuellen Produkt-Container und seinen Inhalt aus. |
| Anzeigen | ![Symbol &quot;Anzeigen&quot;](./assets/pb-icon-show.png){width="25"} | Zeigt den ausgeblendeten Produktbehälter und seinen Inhalt an. |
| Duplizieren | ![Symbol &quot;Duplizieren&quot;](./assets/pb-icon-duplicate.png){width="25"} | Kopiert den Produktcontainer und seinen Inhalt. |
| Entfernen | ![Symbol &quot;Entfernen&quot;](./assets/pb-icon-remove.png){width="25"} | Löscht den Produkt-Container und seinen Inhalt aus der Phase. |

{style="table-layout:auto"}

{{$include /help/_includes/page-builder-hidden-element-note.md}}

## Produktlistenbaustein erstellen

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Blocks]**.

1. Klicken **[!UICONTROL Add New Block]**.

1. Geben Sie die **[!UICONTROL Block Title]** und **[!UICONTROL Identifier]**.

1. Wählen Sie die **[!UICONTROL Store View]** wo der Block verfügbar sein soll.

1. Scrollen Sie nach unten und klicken Sie auf **[!UICONTROL Edit with Page Builder]** oder innerhalb des Inhaltsvorschaubereichs, um die [!DNL Page Builder] Arbeitsbereich.

1. Im [!DNL Page Builder] Bedienfeld, erweitern **[!UICONTROL Add Content]** und ziehen Sie eine **[!UICONTROL Products]** Platzhalter zur Bühne.

   ![Inhaltstyp &quot;Produkte hinzufügen&quot;](./assets/pb-add-content-products-drag.png){width="600" zoomable="yes"}

## Konfigurieren des Produktlistencontainers

Bewegen Sie den Mauszeiger über das leere Element _Produkte_ Container zum Anzeigen der Toolbox und klicken Sie auf _Einstellungen_ (![Symbol Einstellungen](./assets/pb-icon-settings.png){width="20"} ).

![Produkt-Toolbox](./assets/pb-add-content-products-toolbox.png){width="500" zoomable="yes"}

Führen Sie die _Einstellungen_ entsprechend den folgenden Abschnitten:

### Erscheinungsbild

1. Um zu bestimmen, wie die Produktliste auf der Seite angezeigt wird, wählen Sie einen der folgenden Darstellungstypen aus:

   | Typ | Beschreibung |
   | ---- | ----------- |
   | Produktraster | Zeigt die Produkte in einem Raster an, das standardmäßig fünf Produkte pro Zeile anzeigt (mit so vielen Zeilen wie erforderlich), um die in der Variablen **[!UICONTROL Number of Products to Display]** -Einstellung. |
   | Karussell | Zeigt die Produkte in einem Karussell an (auch als Regler bezeichnet). Das Karussell zeigt bis zu fünf Produkte pro Folie. <br/><br/>**Reaktionswarnung**: Wenn Sie dieses Erscheinungsbild auswählen, empfiehlt es sich, den Inhaltstyp Produkte direkt zu einer Zeile, einem Tab oder einem einspaltigen Layout hinzuzufügen, wo er responsiv ist und auf kleineren Bildschirmen weniger Produkte pro Seite anzeigt. Wenn Sie sie zu Content-Typen hinzufügen, die kleiner als die Breite der Seite sind (z. B. eine schmale Spalte), zeigt das Karussell mehr Produkte pro Folie an, als der Container zulässt, unabhängig von der Bildschirmgröße. |

   {style="table-layout:auto"}

   ![Produkterscheinung](./assets/pb-products-appearances.png){width="300"}

   Wenn Sie das Karussell auswählen, müssen Sie auch die [Karusselleinstellungen](#carousel-settings).

1. Für **[!UICONTROL Select Products By]** wählen Sie die Methode für die Produktauswahl aus:

   Sie können Ihre Produkte nach Kategorie, SKU oder Bedingung auswählen. Diese Optionen schließen sich gegenseitig aus. Sie können beispielsweise nicht die Option Kategorie auswählen, die Auswahl Kategorie verwenden und dann zur Option Bedingung wechseln, um einige Bedingungen hinzuzufügen. Ihre Produkte werden nur basierend auf dem ausgewählt, was Sie für _one_ von diesen drei Optionen.

   - **[!UICONTROL Category]** - Wählen Sie diese Option, um Produkte mit einer ausgewählten Kategorie anzuzeigen.

     ![Produktauswahl nach Kategorie](./assets/pb-products-settings_category.png){width="500"}

     Bei Auswahl dieser Option wird eine **[!UICONTROL Category]** auswählen. Klicken Sie auf den Pfeil und führen Sie einen Drilldown durch, um die Kategorie der anzuzeigenden Produkte auszuwählen. Beispiel: in der [!DNL Commerce] Beispieldaten, Einbohren und Auswählen _Frauen > Tops > Tees_ zeigt alle Produkte für diese Kategorie an.

     ![Auswählen einer Katalogkategorie](./assets/pb-select-products-by-category.png){width="500"}

   - **[!UICONTROL SKU]** - Wählen Sie diese Option, um Produkte mit einer oder mehreren SKUs anzuzeigen.

     Bei Auswahl dieser Option wird eine **[!UICONTROL Product SKUs]** Textfeld, in das Sie eine kommagetrennte Liste der anzuzeigenden SKUs eingeben müssen.

     ![Produktauswahl nach SKU](./assets/pb-products-settings_sku.png){width="500"}

   - **[!UICONTROL Condition]** - Wählen Sie diese Option, um Produkte gemäß einer oder mehreren von Ihnen definierten Bedingungen anzuzeigen.

     Wenn diese Option aktiviert ist, stehen Tools zum Hinzufügen von Bedingungen zur Produktauswahl zur Verfügung. Sie können beispielsweise nur Produkte auswählen, deren Geschlecht auf &quot;Unisex&quot;eingestellt ist.

     ![Produktauswahl nach Bedingung](./assets/pb-products-settings_condition.png){width="500"}

     >[!NOTE]
     >
     >Wenn Sie die Option Kategorie oder SKU auswählen, wird das **[!UICONTROL Sort By]** Option `Position`. Bei dieser Sortierungsoption werden die Produkte in derselben Reihenfolge angezeigt wie in Ihrem Katalog.</br>
     >
     >Bei der Option Kategorie zeigt die Sortierung nach Position die Produkte in derselben Reihenfolge an, in der sie in Ihrem Katalog angezeigt werden. Bei der SKU-Option zeigt die Sortierung nach Position die Produkte in der Reihenfolge an, in der Sie sie in der **[!UICONTROL Product SKUs]** Textfeld.

1. Für **[!UICONTROL Sort By]** die Sortierreihenfolge für die Produkte in der Liste auswählen:

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

   ![Sortierungsoptionen für Produkte](./assets/pb-products-sortby.png){width="300"}

1. Geben Sie die **[!UICONTROL Number of Products to Display]** im Karussell oder Raster angezeigt.

   Werte können aus `1` nach `999`. Der Standardwert ist `5` für ein Raster und `20` für ein Karussell.

   >[!NOTE]
   >
   >Einige Produkte in den Einstellungen für Kategorie, SKU oder Bedingung werden möglicherweise nicht in Ihrem Produktraster oder Karussell angezeigt. So werden zum Beispiel nicht vorhandene Produkte, als nicht sichtbar markierte Produkte, nicht vorrätige Produkte und Produkte, die einer anderen Website zugewiesen sind, nicht angezeigt.

   >[!IMPORTANT]
   >
   >Die Preise für konfigurierbare, gruppierte und gebündelte (dynamische Preise) Produkte sind im Admin nicht definiert. Daher werden diese Produkte nicht im **[!UICONTROL Preview]** wenn die Erzeugnisse nach Preis gefiltert werden. Diese Produkte können nicht korrekt im **[!UICONTROL Preview]** wenn nach Preis bestellt.

### Karusselleinstellungen

1. Um zu bestimmen, wie die Produkte im Karussell angezeigt werden, wählen Sie die **[!UICONTROL Carousel Mode]**:

   | Option | Beschreibung |
   | ------ | ----------- |
   | `Default` | Das Karussell zeigt standardmäßig fünf Produkte pro Folie an und reduziert diese Anzahl nach Bedarf responsiv. |
   | `Continuous` | Das Karussell zeigt standardmäßig fünf Produkte pro Folie an (mit der Hälfte eines Produkts auf der rechten und linken Seite), zentriert und scrollt jedoch jeweils ein Produkt in einer Endlosschleife. Produkte links und rechts vom zentrierten Produkt werden abgeblendet dargestellt, sodass das mittlere Produkt hervorgehoben wird. |

   {style="table-layout:auto"}

   Wenn Sie zwischen diesen beiden Modi wechseln, werden die anderen Karusselleinstellungen beibehalten, mit Ausnahme der **[!UICONTROL Infinite Loop]** Einstellung, die immer auf `Yes` im kontinuierlichen Modus und das Feld deaktiviert ist.

   ![Karusselleinstellungen](./assets/pb-products-carousel-settings.png){width="600" zoomable="yes"}

1. Legen Sie bei Bedarf die **[!UICONTROL Autoplay]** -Option `Yes`.

   Wenn die automatische Wiedergabe aktiviert ist, beginnt das Karussell beim Laden der Seite automatisch mit dem Scrollen. Wenn Sie die Standardeinstellung (`No`), muss der Kunde auf die Foliennavigation (Punkte oder Pfeile) klicken, um jede Folie nacheinander anzuzeigen.

   Wenn Sie diese Funktion aktivieren, geben Sie **[!UICONTROL Autoplay Speed]** um die Verzögerung in Millisekunden zwischen den einzelnen Folien anzugeben. Der Standardwert ist `4000` (4 Sekunden).

1. Legen Sie bei Bedarf die **[!UICONTROL Infinite Loop]** -Option `Yes`.

   Wenn die Endlosschleife aktiviert ist, wird die Diashow unbegrenzt wiederholt, während die Seite geöffnet ist. Wenn Sie die Standardeinstellung (`No`), wird die Diashow nur einmal wiedergegeben.

   >[!NOTE]
   >
   >Wenn Sie **[!UICONTROL Infinite Loop]** nach `No` und **[!UICONTROL Autoplay]** auf `Yes`, wird die automatische Wiedergabe am Ende der Anzahl der anzuzeigenden Produkte angehalten.

1. Legen Sie bei Bedarf die **[!UICONTROL Show Arrows]** -Option `Yes`.

   Wenn diese Option aktiviert ist, enthält jede Folie _next_ und _previous_ Navigationspfeile auf der linken und rechten Seite. Wenn Sie die Standardeinstellung (`No`), zeigen die Folien keine Navigationspfeile an.

1. Legen Sie bei Bedarf die **[!UICONTROL Show Dots]** -Option `No`.

   Wenn auf die Standardeinstellung (`Yes`), werden Navigationspunkte unten im Karussellregler angezeigt. Wenn Sie diese Einstellung deaktivieren, zeigt der Karussellregler keine Navigationspunkte an.

### Erweitert

1. Um die Positionierung der Produktliste innerhalb des übergeordneten Containers zu steuern, wählen Sie die **[!UICONTROL Alignment]**:

   | Option | Beschreibung |
   | ------ | ----------- |
   | `Default` | Wendet die Standardeinstellung für die Ausrichtung an, die im Stylesheet des aktuellen Designs angegeben ist. |
   | `Left` | Richtet die Liste am linken Rand des übergeordneten Containers aus, wobei der angegebene Abstand berücksichtigt wird. |
   | `Center` | Richtet die Liste in der Mitte des übergeordneten Containers aus, wobei der angegebene Abstand berücksichtigt wird. |
   | `Right` | Richtet die Liste am rechten Rand des übergeordneten Containers aus, wobei der angegebene Abstand berücksichtigt wird. |

   {style="table-layout:auto"}

1. Legen Sie die **[!UICONTROL Border]** -Stil, der auf alle vier Seiten des Container &quot;Products&quot;angewendet wird:

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

1. Wenn Sie einen anderen Rahmenstil als `None`, füllen Sie die Randanzeigeoptionen aus:

   | Option | Beschreibung |
   | ------ |------------ |
   | [!UICONTROL Border Color] | Geben Sie die Farbe an, indem Sie ein Muster auswählen, auf die Farbauswahl klicken oder einen gültigen Farbnamen oder einen entsprechenden Hexadezimalwert eingeben. |
   | [!UICONTROL Border Width] | Geben Sie die Anzahl Pixel für die Rahmenlinienbreite an. |
   | [!UICONTROL Border Radius] | Geben Sie die Anzahl der Pixel an, um die die Größe des Radius definiert wird, mit dem die einzelnen Ecken des Rands gerundet werden. |

   {style="table-layout:auto"}

1. (Optional) Geben Sie die Namen von **[!UICONTROL CSS classes]** aus dem aktuellen Stylesheet, das auf den Container angewendet werden soll.

   Trennen Sie mehrere Klassennamen durch ein Leerzeichen.

1. Geben Sie Werte in Pixel für die **[!UICONTROL Margins and Padding]** um die äußeren Ränder und den inneren Abstand des Produktbehälters zu bestimmen.

   Geben Sie die entsprechenden Werte in das Diagramm ein.

   | Container-Bereich | Beschreibung |
   | -------------- | ----------- |
   | [!UICONTROL Margins] | Die Menge an leerem Raum, die auf den äußeren Rand aller Seiten des Containers angewendet wird. Optionen: `Top` / `Right` / `Bottom` / `Left` |
   | [!UICONTROL Padding] | Die Menge an leerem Raum, die auf den inneren Rand aller Seiten des Containers angewendet wird. Optionen: `Top` / `Right` / `Bottom` / `Left` |


## Speichern und Vorschau auf der Bühne anzeigen

Klicken Sie oben rechts auf **[!UICONTROL Save]** , um die Einstellungen anzuwenden und zum [!DNL Page Builder] Arbeitsbereich.

Wenn Sie ein Produktkarussell konfiguriert haben, sollte es in etwa wie im folgenden Beispiel aussehen:

![Karussell auf der Bühne](./assets/pb-products-admin-carousel.png){width="600"}

Sie können jetzt eine [Widget](../content-design/widgets.md) um diesen Block an die Stelle zu setzen, an der er im Laden erscheinen soll. Oder Sie können [Inhalt hinzufügen - Block](block.md) , um den Baustein einer vorhandenen Seite, Registerkarte oder Baustein hinzuzufügen.
