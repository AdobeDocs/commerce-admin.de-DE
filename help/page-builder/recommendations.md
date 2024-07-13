---
title: Inhalt hinzufügen - Produkt-Recommendations
description: Erfahren Sie mehr über den Inhaltstyp "Product Recommendations", der zum Hinzufügen einer Empfehlungsliste zur  [!DNL Page Builder] Bühne verwendet wird.
exl-id: ca90c10d-8d7a-42a2-bb13-2602aa9d6eef
feature: Page Builder, Page Content, Recommendations
source-git-commit: 2f86421311b218d39c1abebaf117b8af0be5ea5d
workflow-type: tm+mt
source-wordcount: '931'
ht-degree: 0%

---

# Inhalt hinzufügen - Produkt-Recommendations

Verwenden Sie den Inhaltstyp _Produkt-Recommendations_ , um der [[!DNL Page Builder] Bühne](workspace.md#stage) eine vorhandene, aktive [Empfehlungseinheit](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/product-recommendations/admin/create) für eine CMS-Seite, einen Block oder einen dynamischen Block hinzuzufügen.

>[!NOTE]
>
>Der Inhaltstyp [!DNL Page Builder] _Produkt-Recommendations_ wird in Adobe Commerce 2.4.4 und höher unterstützt und ist in den [Produkt-Recommendations-Metapaketen der Versionen 3.0.x oder höher](https://commercemarketplace.adobe.com/magento-product-recommendations.html) verfügbar. Informationen zum Hinzufügen von [!DNL Page Builder] Support für Product Recommendations finden Sie in den Installationsinformationen](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/product-recommendations/getting-started/install-configure). [ **Dieser Inhaltstyp steht nicht zur Magento Open Source zur Verfügung.**

{{$include /help/_includes/page-builder-save-timeout.md}}

## Produkt-Recommendations-Toolbox

| Tool | Symbol | Beschreibung |
| --- | --| --- |
| Verschieben | ![Symbol &quot;Verschieben&quot;](./assets/pb-icon-move.png){width="25"} | Verschiebt den Produktempfehlungs-Container und seinen Inhalt an eine andere Position auf der Bühne. |
| Einstellungen | ![Einstellungssymbol](./assets/pb-icon-settings.png){width="25"} | Öffnet die Seite Produktempfehlung bearbeiten , auf der Sie die Empfehlungseinheit auswählen und die Eigenschaften des Containers ändern können. |
| Ausblenden | ![Symbol zum Ausblenden](./assets/pb-icon-hide.png){width="25"} | Blendet den aktuellen Produktempfehlungs-Container und seinen Inhalt aus. |
| Anzeigen | ![Symbol &quot;Anzeigen&quot;](./assets/pb-icon-show.png){width="25"} | Zeigt den ausgeblendeten Produkt-Empfehlungs-Container und seinen Inhalt an. |
| Duplizieren | ![Symbol &quot;Duplizieren&quot;](./assets/pb-icon-duplicate.png){width="25"} | Kopiert den Produktempfehlungs-Container und seinen Inhalt in zweifacher Hinsicht. |
| Entfernen | ![Symbol &quot;Entfernen&quot;](./assets/pb-icon-remove.png){width="25"} | Löscht den Produktempfehlungs-Container und seinen Inhalt aus der Phase. |

{style="table-layout:auto"}

{{$include /help/_includes/page-builder-hidden-element-note.md}}

## Hinzufügen einer vorhandenen Empfehlungseinheit

1. Stellen Sie sicher, dass Sie bereits [eine Empfehlungseinheit](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/product-recommendations/admin/create) für den Seitentyp [!DNL Page Builder] erstellt haben.

>[!NOTE]
>
>Sie können nur in der standardmäßigen Store-Ansicht Empfehlungseinheiten für den Seitentyp [!DNL Page Builder] erstellen.

1. Öffnen Sie die Seite, den Block oder den dynamischen Block im Bearbeitungsmodus.

1. Erweitern Sie den Abschnitt _[!UICONTROL Content]_und klicken Sie auf **[!UICONTROL Edit with Page Builder]**oder innerhalb des Inhaltsvorschaubereichs, um den Arbeitsbereich [!DNL Page Builder] zu öffnen.

1. Ziehen Sie im Bedienfeld [!DNL Page Builder] unter _[!UICONTROL Layout]_einen **[!UICONTROL Row]**Platzhalter auf die Bühne.

1. Ziehen Sie im Bedienfeld [!DNL Page Builder] unter _[!UICONTROL Add Content]_einen **[!UICONTROL Product Recommendation]**Platzhalter in die Zeile.

   ![Hinzufügen des Inhaltstyps &quot;Produktempfehlung&quot;](./assets/pb-add-prex-drag.png){width="600" zoomable="yes"}

1. Führen Sie einen der folgenden Schritte aus:

   - Klicken Sie auf **[!UICONTROL Edit Product Recommendation]**.
   - Bewegen Sie den Mauszeiger über den leeren Container, um die Toolbox anzuzeigen, und klicken Sie auf das Symbol _Einstellungen_ (![Einstellungssymbol](./assets/pb-icon-settings.png)).

   ![Produktempfehlungen bearbeiten](./assets/pb-prex-toolbox.png){width="600" zoomable="yes"}

1. Klicken Sie im Abschnitt _[!UICONTROL Selection]_auf **[!UICONTROL Select]**.

1. Suchen Sie in der Liste der aktiven Produktempfehlungen die Zeile mit der Empfehlungseinheit, die Sie hinzufügen möchten, und klicken Sie in der letzten Spalte auf **[!UICONTROL Select]** .

   ![Ausgewählte Produktempfehlungen](./assets/pb-prex-select.png){width="600" zoomable="yes"}

1. Klicken Sie in der oberen rechten Ecke auf **[!UICONTROL Add Selected]**.

   Der Name der ausgewählten Produktempfehlung wird im Abschnitt _[!UICONTROL Selection]_der Seite_[!UICONTROL Edit Product Recommendation]_ angezeigt.

1. Nehmen Sie alle erforderlichen Änderungen an den [erweiterten Einstellungen](#advanced-settings) vor.

   ![Produktempfehlungen bearbeiten](./assets/pb-prex-edit.png){width="600" zoomable="yes"}

1. Führen Sie nach Abschluss folgende Schritte aus:

   - Wenn Sie mit einem vollständig maximierten Browserfenster arbeiten, klicken Sie auf das Symbol _Vollbild schließen_ (![Vollbildsymbol schließen](./assets/pb-icon-reduce.png)) in der oberen rechten Ecke des Arbeitsbereichs.

   - Klicken Sie auf **[!UICONTROL Save]** , um die Einstellungen anzuwenden und zum Arbeitsbereich [!DNL Page Builder] zurückzukehren.

   Wenn Sie zur Bühne zurückkehren, werden Produktplatzhalter-Bilder im Container angezeigt.

## Einstellungen der Empfehlungseinheiten bearbeiten

1. Bewegen Sie den Mauszeiger über den Container der Empfehlungseinheit, um die Toolbox anzuzeigen, und klicken Sie auf das Symbol _Einstellungen_ (![Einstellungssymbol](./assets/pb-icon-settings.png)).

   ![Empfehlungs-Toolbox](./assets/pb-placeholder-toolbox.png){width="600" zoomable="yes"}

1. Nehmen Sie alle erforderlichen Änderungen an den [erweiterten Einstellungen](#advanced-settings) vor.

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save]** , um die Einstellungen anzuwenden und zum Arbeitsbereich [!DNL Page Builder] zurückzukehren.

## Duplizieren einer Empfehlungseinheit

1. Bewegen Sie den Mauszeiger über den Container der Empfehlungseinheit, um die Toolbox anzuzeigen, und klicken Sie in der Toolbox auf das Symbol _Duplizieren_ (![Duplizieren-Symbol](./assets/pb-icon-duplicate.png)).

   Das Duplikat wird direkt unter dem Original angezeigt.

1. Um die duplizierte Empfehlungseinheit an eine neue Position zu verschieben, halten Sie den Mauszeiger über den Container und klicken Sie in der Toolbox auf das Symbol _Verschieben_ (![Verschieben-Symbol](./assets/pb-icon-move.png)).

1. Wählen Sie die Empfehlungseinheit aus und ziehen Sie sie, bis die rote Führungslinie an der neuen Position angezeigt wird.

   Die oberen und unteren Ränder der einzelnen Behälter werden als gestrichelte Linien angezeigt, während die Empfehlungseinheit verschoben wird.

## Entfernen einer Empfehlungseinheit aus der Bühne

1. Bewegen Sie den Mauszeiger über den Empfehlungseinheiten-Container und klicken Sie in der Toolbox auf das Symbol _Entfernen_ ( ![Symbol &quot;Entfernen&quot;](./assets/pb-icon-remove.png)).

1. Klicken Sie bei Aufforderung zur Bestätigung auf **[!UICONTROL OK]**.

## Erweiterte Einstellungen

1. Um die Positionierung der Product Recommendations-Einheit innerhalb des übergeordneten Containers zu steuern, wählen Sie den Wert **[!UICONTROL Alignment]**:

   | Option | Beschreibung |
   | ------ | ----------- |
   | `Default` | Wendet die Standardeinstellung für die Ausrichtung an, die im Stylesheet des aktuellen Designs angegeben ist. |
   | `Left` | Richtet die Einheit am linken Rand des übergeordneten Containers aus, wobei der angegebene Abstand berücksichtigt wird. |
   | `Center` | Richtet die Einheit in der Mitte des übergeordneten Containers aus, wobei der angegebene Abstand berücksichtigt wird. |
   | `Right` | Richtet die Einheit am rechten Rand des übergeordneten Containers aus, wobei der angegebene Abstand berücksichtigt wird. |

   {style="table-layout:auto"}

1. Legen Sie den **[!UICONTROL Border]** -Stil fest, der auf alle vier Seiten der Product Recommendations-Einheit angewendet wird:

   | Option | Beschreibung |
   | ------ | ----------- |
   | `Default` | Wendet den standardmäßigen Randstil an, der vom zugehörigen Stylesheet angegeben wird. |
   | `None` | keine sichtbare Anzeige der Einheitengrenzen. |
   | `Dotted` | Der Einheitenrahmen wird als gepunktete Linie angezeigt. |
   | `Dashed` | Der Einheitenrahmen wird als gestrichelte Linie angezeigt. |
   | `Solid` | Der Einheitenrahmen wird als durchgehende Linie angezeigt. |
   | `Double` | Der Einheitenrand wird als doppelte Linie angezeigt. |
   | `Groove` | Der Einheitsrand wird als Einradellinie angezeigt. |
   | `Ridge` | Der Rahmen der Einheit erscheint als gekürzte Linie. |
   | `Inset` | Der Einheitsrand wird als Einzugslinie angezeigt. |
   | `Outset` | Der Einheitsrand wird als Einstiegslinie angezeigt. |

   {style="table-layout:auto"}

1. Wenn Sie einen anderen Rahmenstil als `None` festlegen, füllen Sie die Anzeigeoptionen für die Rahmenanzeige aus:

   | Option | Beschreibung |
   | ------ |------------ |
   | [!UICONTROL Border Color] | Geben Sie die Farbe an, indem Sie ein Muster auswählen, auf die Farbauswahl klicken oder einen gültigen Farbnamen oder einen entsprechenden Hexadezimalwert eingeben. |
   | [!UICONTROL Border Width] | Geben Sie die Anzahl Pixel für die Rahmenlinienbreite an. |
   | [!UICONTROL Border Radius] | Geben Sie die Anzahl der Pixel an, um die die Größe des Radius definiert wird, mit dem die einzelnen Ecken des Rands gerundet werden. |

   {style="table-layout:auto"}

1. (Optional) Geben Sie die Namen von **[!UICONTROL CSS classes]** aus dem aktuellen Stylesheet an, das auf die Einheit angewendet werden soll.

   Trennen Sie mehrere Klassennamen durch ein Leerzeichen.

1. Geben Sie Werte in Pixel für den Wert **[!UICONTROL Margins and Padding]** ein, um die äußeren Ränder und den inneren Abstand der Einheit zu bestimmen.

   Geben Sie die entsprechenden Werte in das Diagramm ein.

   | Container-Bereich | Beschreibung |
   | ------ | ----------- |
   | [!UICONTROL Margins] | Die Menge des Leerraums, der auf den äußeren Rand aller Seiten der Einheit angewendet wird. Optionen: `Top` / `Right` / `Bottom` / `Left` |
   | [!UICONTROL Padding] | Die Menge des Leerraums, der auf den inneren Rand aller Seiten der Einheit angewendet wird. Optionen: `Top` / `Right` / `Bottom` / `Left` |

   {style="table-layout:auto"}
