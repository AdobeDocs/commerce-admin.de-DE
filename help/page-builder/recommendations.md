---
title: Inhalt hinzufügen - Produkt-Recommendations
description: Erfahren Sie mehr über den Inhaltstyp des Produkt-Recommendations, mit dem Empfehlungen zur [!DNL Page Builder] Bühne.
exl-id: ca90c10d-8d7a-42a2-bb13-2602aa9d6eef
feature: Page Builder, Page Content, Recommendations
source-git-commit: 2f86421311b218d39c1abebaf117b8af0be5ea5d
workflow-type: tm+mt
source-wordcount: '931'
ht-degree: 0%

---

# Inhalt hinzufügen - Produkt-Recommendations

Verwenden Sie die _Produkt-Recommendations_ Inhaltstyp zum Hinzufügen eines vorhandenen, aktiven [Empfehlungseinheit](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/product-recommendations/admin/create) der [[!DNL Page Builder] Schritt](workspace.md#stage) für eine CMS-Seite, einen Block oder einen dynamischen Block.

>[!NOTE]
>
>Die [!DNL Page Builder] _Produkt-Recommendations_ Inhaltstyp wird in Adobe Commerce 2.4.4 und höher unterstützt und ist im Abschnitt [Produkt-Recommendations-Metapaket Version 3.0.x oder neuer](https://commercemarketplace.adobe.com/magento-product-recommendations.html). Hinzufügen von [!DNL Page Builder] Support für Product Recommendations, [Installationsinformationen anzeigen](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/product-recommendations/getting-started/install-configure). **Dieser Inhaltstyp steht nicht zur Magento Open Source zur Verfügung.**

{{$include /help/_includes/page-builder-save-timeout.md}}

## Produkt-Recommendations-Toolbox

| Tool | Symbol | Beschreibung |
| --- | --| --- |
| Verschieben | ![Symbol Verschieben](./assets/pb-icon-move.png){width="25"} | Verschiebt den Produktempfehlungs-Container und seinen Inhalt an eine andere Position auf der Bühne. |
| Einstellungen | ![Symbol Einstellungen](./assets/pb-icon-settings.png){width="25"} | Öffnet die Seite Produktempfehlung bearbeiten , auf der Sie die Empfehlungseinheit auswählen und die Eigenschaften des Containers ändern können. |
| Ausblenden | ![Symbol &quot;Ausblenden&quot;](./assets/pb-icon-hide.png){width="25"} | Blendet den aktuellen Produktempfehlungs-Container und seinen Inhalt aus. |
| Anzeigen | ![Symbol &quot;Anzeigen&quot;](./assets/pb-icon-show.png){width="25"} | Zeigt den ausgeblendeten Produkt-Empfehlungs-Container und seinen Inhalt an. |
| Duplizieren | ![Symbol &quot;Duplizieren&quot;](./assets/pb-icon-duplicate.png){width="25"} | Kopiert den Produktempfehlungs-Container und seinen Inhalt in zweifacher Hinsicht. |
| Entfernen | ![Symbol &quot;Entfernen&quot;](./assets/pb-icon-remove.png){width="25"} | Löscht den Produktempfehlungs-Container und seinen Inhalt aus der Phase. |

{style="table-layout:auto"}

{{$include /help/_includes/page-builder-hidden-element-note.md}}

## Hinzufügen einer vorhandenen Empfehlungseinheit

1. Stellen Sie sicher, dass Sie bereits [eine Empfehlungseinheit erstellt hat](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/product-recommendations/admin/create) für die [!DNL Page Builder] Seitentyp.

>[!NOTE]
>
>Sie können für die [!DNL Page Builder] Seitentyp nur in der standardmäßigen Store-Ansicht.

1. Öffnen Sie die Seite, den Block oder den dynamischen Block im Bearbeitungsmodus.

1. Erweitern Sie die _[!UICONTROL Content]_und klicken Sie auf **[!UICONTROL Edit with Page Builder]**oder innerhalb des Inhaltsvorschaubereichs, um die [!DNL Page Builder] Arbeitsbereich.

1. Im [!DNL Page Builder] Bereich unter _[!UICONTROL Layout]_, ziehen Sie eine **[!UICONTROL Row]**Platzhalter zur Bühne.

1. Im [!DNL Page Builder] Bereich unter _[!UICONTROL Add Content]_, ziehen Sie eine **[!UICONTROL Product Recommendation]**Platzhalter zur Zeile.

   ![Hinzufügen des Inhaltstyps für Produktempfehlungen](./assets/pb-add-prex-drag.png){width="600" zoomable="yes"}

1. Führen Sie einen der folgenden Schritte aus:

   - Klicks **[!UICONTROL Edit Product Recommendation]**.
   - Bewegen Sie den Mauszeiger über den leeren Container, um die Toolbox anzuzeigen, und klicken Sie auf _Einstellungen_ (![Symbol Einstellungen](./assets/pb-icon-settings.png)).

   ![Produktempfehlungen bearbeiten](./assets/pb-prex-toolbox.png){width="600" zoomable="yes"}

1. Im _[!UICONTROL Selection]_Abschnitt, klicken Sie auf **[!UICONTROL Select]**.

1. Suchen Sie in der Liste der Empfehlungen für aktive Produkte die Zeile mit der hinzuzufügenden Empfehlungseinheit und klicken Sie auf **[!UICONTROL Select]** in der letzten Spalte.

   ![Ausgewählte Produktempfehlung](./assets/pb-prex-select.png){width="600" zoomable="yes"}

1. Klicken Sie oben rechts auf **[!UICONTROL Add Selected]**.

   Der Name der ausgewählten Produktempfehlung wird im _[!UICONTROL Selection]_Abschnitt_[!UICONTROL Edit Product Recommendation]_ Seite.

1. Nehmen Sie die erforderlichen Änderungen an der [Erweiterte Einstellungen](#advanced-settings).

   ![Produktempfehlungen bearbeiten](./assets/pb-prex-edit.png){width="600" zoomable="yes"}

1. Führen Sie nach Abschluss folgende Schritte aus:

   - Wenn Sie mit einem vollständig maximierten Browser-Fenster arbeiten, klicken Sie auf das _Vollbild schließen_ (![Symbol &quot;Vollbild schließen&quot;](./assets/pb-icon-reduce.png)) in der oberen rechten Ecke des Arbeitsbereichs.

   - Klicks **[!UICONTROL Save]** , um die Einstellungen anzuwenden und zum [!DNL Page Builder] Arbeitsbereich.

   Wenn Sie zur Bühne zurückkehren, werden Produktplatzhalter-Bilder im Container angezeigt.

## Einstellungen der Empfehlungseinheiten bearbeiten

1. Bewegen Sie den Mauszeiger über den Container der Empfehlungseinheit, um die Toolbox anzuzeigen, und klicken Sie auf die Schaltfläche _Einstellungen_ (![Symbol Einstellungen](./assets/pb-icon-settings.png)).

   ![Empfehlungs-Toolbox](./assets/pb-placeholder-toolbox.png){width="600" zoomable="yes"}

1. Nehmen Sie die erforderlichen Änderungen an der [Erweiterte Einstellungen](#advanced-settings).

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save]** , um die Einstellungen anzuwenden und zum [!DNL Page Builder] Arbeitsbereich.

## Duplizieren einer Empfehlungseinheit

1. Bewegen Sie den Mauszeiger über den Container der Empfehlungseinheit, um die Toolbox anzuzeigen, und klicken Sie auf die Schaltfläche _Duplizieren_ (![Symbol &quot;Duplizieren&quot;](./assets/pb-icon-duplicate.png)) in der Toolbox.

   Das Duplikat wird direkt unter dem Original angezeigt.

1. Um die duplizierte Empfehlungseinheit an eine neue Position zu verschieben, bewegen Sie den Mauszeiger über den Container und klicken Sie auf die _Verschieben_ (![Symbol Verschieben](./assets/pb-icon-move.png)) in der Toolbox.

1. Wählen Sie die Empfehlungseinheit aus und ziehen Sie sie, bis die rote Führungslinie an der neuen Position angezeigt wird.

   Die oberen und unteren Ränder der einzelnen Behälter werden als gestrichelte Linien angezeigt, während die Empfehlungseinheit verschoben wird.

## Entfernen einer Empfehlungseinheit aus der Bühne

1. Bewegen Sie den Mauszeiger über den Container der Empfehlungseinheit und klicken Sie auf die _Entfernen_ ( ![Symbol &quot;Entfernen&quot;](./assets/pb-icon-remove.png)) in der Toolbox.

1. Klicken Sie bei Aufforderung zur Bestätigung auf **[!UICONTROL OK]**.

## Erweiterte Einstellungen

1. Um die Positionierung der Product Recommendations-Einheit innerhalb des übergeordneten Containers zu steuern, wählen Sie die **[!UICONTROL Alignment]**:

   | Option | Beschreibung |
   | ------ | ----------- |
   | `Default` | Wendet die Standardeinstellung für die Ausrichtung an, die im Stylesheet des aktuellen Designs angegeben ist. |
   | `Left` | Richtet die Einheit am linken Rand des übergeordneten Containers aus, wobei der angegebene Abstand berücksichtigt wird. |
   | `Center` | Richtet die Einheit in der Mitte des übergeordneten Containers aus, wobei der angegebene Abstand berücksichtigt wird. |
   | `Right` | Richtet die Einheit am rechten Rand des übergeordneten Containers aus, wobei der angegebene Abstand berücksichtigt wird. |

   {style="table-layout:auto"}

1. Legen Sie die **[!UICONTROL Border]** -Stil, der auf alle vier Seiten der Product Recommendations-Einheit angewendet wird:

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

1. Wenn Sie einen anderen Rahmenstil als `None`, füllen Sie die Randanzeigeoptionen aus:

   | Option | Beschreibung |
   | ------ |------------ |
   | [!UICONTROL Border Color] | Geben Sie die Farbe an, indem Sie ein Muster auswählen, auf die Farbauswahl klicken oder einen gültigen Farbnamen oder einen entsprechenden Hexadezimalwert eingeben. |
   | [!UICONTROL Border Width] | Geben Sie die Anzahl Pixel für die Rahmenlinienbreite an. |
   | [!UICONTROL Border Radius] | Geben Sie die Anzahl der Pixel an, um die die Größe des Radius definiert wird, mit dem die einzelnen Ecken des Rands gerundet werden. |

   {style="table-layout:auto"}

1. (Optional) Geben Sie die Namen von **[!UICONTROL CSS classes]** aus dem aktuellen Stylesheet, das auf die Einheit angewendet werden soll.

   Trennen Sie mehrere Klassennamen durch ein Leerzeichen.

1. Geben Sie Werte in Pixel für die **[!UICONTROL Margins and Padding]** zur Bestimmung der äußeren Ränder und des inneren Abstands der Einheit.

   Geben Sie die entsprechenden Werte in das Diagramm ein.

   | Container-Bereich | Beschreibung |
   | ------ | ----------- |
   | [!UICONTROL Margins] | Die Menge des Leerraums, der auf den äußeren Rand aller Seiten der Einheit angewendet wird. Optionen: `Top` / `Right` / `Bottom` / `Left` |
   | [!UICONTROL Padding] | Die Menge des Leerraums, der auf den inneren Rand aller Seiten der Einheit angewendet wird. Optionen: `Top` / `Right` / `Bottom` / `Left` |

   {style="table-layout:auto"}
