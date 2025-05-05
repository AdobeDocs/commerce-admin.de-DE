---
title: Inhalt hinzufügen - Produktempfehlungen
description: Erfahren Sie mehr über den Content-Typ „Produktempfehlungen“, mit dem eine Liste von Empfehlungen zur  [!DNL Page Builder]  hinzugefügt wird.
exl-id: ca90c10d-8d7a-42a2-bb13-2602aa9d6eef
feature: Page Builder, Page Content, Recommendations
source-git-commit: 5da244a548b15863fe31b5df8b509f8e63df27c2
workflow-type: tm+mt
source-wordcount: '931'
ht-degree: 0%

---

# Inhalt hinzufügen - Produktempfehlungen

Verwenden Sie den _Produktempfehlungen_ Content-Typ, um eine vorhandene, aktive [Empfehlungseinheit](https://experienceleague.adobe.com/en/docs/commerce/product-recommendations/admin/create) zum [[!DNL Page Builder] Schritt](workspace.md#stage) für eine CMS-Seite, einen -Block oder einen dynamischen Block hinzuzufügen.

>[!NOTE]
>
>Der Content-Typ [!DNL Page Builder] _Produktempfehlungen_ wird in Adobe Commerce 2.4.4 und höher unterstützt und ist im [Product Recommendations-Metapaket Version 3.0.x oder höher) ](https://commercemarketplace.adobe.com/magento-product-recommendations.html). Informationen zum Hinzufügen [!DNL Page Builder] Unterstützung für Produktempfehlungen [finden Sie in den Installationsinformationen](https://experienceleague.adobe.com/en/docs/commerce/product-recommendations/getting-started/install-configure). **Dieser Inhaltstyp ist für Magento Open Source nicht verfügbar.**

{{$include /help/_includes/page-builder-save-timeout.md}}

## Toolbox für Produktempfehlungen

| Tool | Symbol | Beschreibung |
| --- | --| --- |
| Verschieben | ![move icon](./assets/pb-icon-move.png){width="25"} | Verschiebt den Produktempfehlungs-Container und dessen Inhalt an eine andere Position auf der Bühne. |
| Einstellungen | ![Einstellungssymbol](./assets/pb-icon-settings.png){width="25"} | Öffnet die Seite Produktempfehlung bearbeiten, auf der Sie die Empfehlungseinheit auswählen und die Eigenschaften des Containers ändern können. |
| Ausblenden | ![Symbol ausblenden](./assets/pb-icon-hide.png){width="25"} | Blendet den aktuellen Produktempfehlungs-Container und dessen Inhalt aus. |
| Anzeigen | ![Symbol anzeigen](./assets/pb-icon-show.png){width="25"} | Zeigt den ausgeblendeten Produktempfehlungs-Container und dessen Inhalt an. |
| Duplikat | ![Symbol „Duplizieren“](./assets/pb-icon-duplicate.png){width="25"} | Erstellt eine doppelte Kopie des Produktempfehlungs-Containers und seines Inhalts. |
| entfernen | ![Symbol entfernen](./assets/pb-icon-remove.png){width="25"} | Löscht den Produktempfehlungs-Container und seinen Inhalt aus der Phase. |

{style="table-layout:auto"}

{{$include /help/_includes/page-builder-hidden-element-note.md}}

## Hinzufügen einer vorhandenen Empfehlungseinheit

1. Stellen Sie sicher, [ Sie bereits eine Empfehlungseinheit ](https://experienceleague.adobe.com/en/docs/commerce/product-recommendations/admin/create) den [!DNL Page Builder] Seitentyp erstellt haben.

>[!NOTE]
>
>Sie können Empfehlungseinheiten für den [!DNL Page Builder] Seitentyp nur in der standardmäßigen Store-Ansicht erstellen.

1. Öffnen Sie die Seite, den Block oder den dynamischen Block im Bearbeitungsmodus.

1. Erweitern Sie den Abschnitt _[!UICONTROL Content]_&#x200B;und klicken Sie im Bereich Inhaltsvorschau auf **[!UICONTROL Edit with Page Builder]**&#x200B;oder , um den [!DNL Page Builder] Workspace zu öffnen.

1. Ziehen Sie im [!DNL Page Builder] Bedienfeld unter _[!UICONTROL Layout]_&#x200B;einen **[!UICONTROL Row]**&#x200B;Platzhalter auf die Bühne.

1. Ziehen Sie im [!DNL Page Builder] unter _[!UICONTROL Add Content]_&#x200B;einen **[!UICONTROL Product Recommendation]**&#x200B;Platzhalter in die Zeile.

   ![Hinzufügen des Inhaltstyps für Produktempfehlungen](./assets/pb-add-prex-drag.png){width="600" zoomable="yes"}

1. Führen Sie einen der folgenden Schritte aus:

   - Klicken Sie auf **[!UICONTROL Edit Product Recommendation]**.
   - Bewegen Sie den Mauszeiger über den leeren Container, um die Toolbox anzuzeigen, und klicken Sie auf _Einstellungen_ (![Einstellungssymbol](./assets/pb-icon-settings.png)).

   ![Produktempfehlung bearbeiten](./assets/pb-prex-toolbox.png){width="600" zoomable="yes"}

1. Klicken Sie im Abschnitt _[!UICONTROL Selection]_&#x200B;auf **[!UICONTROL Select]**.

1. Suchen Sie in der Liste der aktiven Produktempfehlungen die Zeile mit der Empfehlungseinheit, die Sie hinzufügen möchten, und klicken Sie auf **[!UICONTROL Select]** in der letzten Spalte.

   ![Ausgewählte Produktempfehlungen](./assets/pb-prex-select.png){width="600" zoomable="yes"}

1. Klicken Sie oben rechts auf **[!UICONTROL Add Selected]**.

   Der Name der ausgewählten Produktempfehlung wird im Abschnitt _[!UICONTROL Selection]_&#x200B;der Seite&#x200B;_[!UICONTROL Edit Product Recommendation]_ angezeigt.

1. Nehmen Sie die erforderlichen Änderungen an den [Erweiterten Einstellungen](#advanced-settings) vor.

   ![Produktempfehlung bearbeiten](./assets/pb-prex-edit.png){width="600" zoomable="yes"}

1. Gehen Sie nach Abschluss des Vorgangs wie folgt vor:

   - Wenn Sie mit einem vollständig maximierten Browser-Fenster arbeiten, klicken Sie auf das Symbol _Vollbild schließen_ (![Vollbildsymbol schließen](./assets/pb-icon-reduce.png)) in der oberen rechten Ecke des Arbeitsbereichs.

   - Klicken Sie auf **[!UICONTROL Save]** , um die Einstellungen anzuwenden und zum Arbeitsbereich [!DNL Page Builder] zurückzukehren.

   Wenn Sie zum Schritt zurückkehren, werden die Produktplatzhalterbilder im Container angezeigt.

## Einstellungen der Empfehlungseinheit bearbeiten

1. Bewegen Sie den Mauszeiger über den Container mit den Empfehlungseinheiten, um die Toolbox anzuzeigen, und klicken Sie _das Symbol_ Einstellungen![ (](./assets/pb-icon-settings.png)).

   ![Recommendations-Toolbox](./assets/pb-placeholder-toolbox.png){width="600" zoomable="yes"}

1. Nehmen Sie die erforderlichen Änderungen an den [Erweiterten Einstellungen](#advanced-settings) vor.

1. Klicken Sie abschließend auf **[!UICONTROL Save]** , um die Einstellungen anzuwenden und zum Arbeitsbereich [!DNL Page Builder] zurückzukehren.

## Duplizieren einer Empfehlungseinheit

1. Bewegen Sie den Mauszeiger über den Container der Empfehlungseinheit, um die Toolbox anzuzeigen, und klicken Sie _das Symbol Duplizieren_ (![Duplikatsymbol](./assets/pb-icon-duplicate.png)) in der Toolbox.

   Das Duplikat wird direkt unter dem Original angezeigt.

1. Um die duplizierte Empfehlungseinheit an eine neue Position zu verschieben, bewegen Sie den Mauszeiger über den Container und klicken Sie auf _Verschieben_-Symbol ![Verschieben](./assets/pb-icon-move.png) in der Toolbox.

1. Wählen Sie die Empfehlungseinheit aus und ziehen Sie sie, bis die rote Richtlinie an der neuen Position angezeigt wird.

   Der obere und untere Rand jedes Containers werden während des Verschiebens der Empfehlungseinheit als gestrichelte Linien angezeigt.

## Entfernen einer Empfehlungseinheit aus der Phase

1. Bewegen Sie den Mauszeiger über den Container für die Empfehlungseinheit und klicken Sie auf das Symbol _Entfernen_ (![Entfernen](./assets/pb-icon-remove.png)) in der Toolbox.

1. Wenn Sie zum Bestätigen aufgefordert werden, klicken Sie auf **[!UICONTROL OK]**.

## Erweiterte Einstellungen

1. Wählen Sie die **[!UICONTROL Alignment]** aus, um die Positionierung der Einheit „Produktempfehlungen“ im übergeordneten Container zu steuern:

   | Option | Beschreibung |
   | ------ | ----------- |
   | `Default` | Wendet die Standardeinstellung für die Ausrichtung an, die im Stylesheet des aktuellen Designs angegeben ist. |
   | `Left` | Richtet die Einheit am linken Rand des übergeordneten Containers aus, wobei ein beliebiger Abstand berücksichtigt wird. |
   | `Center` | Richtet die Einheit in der Mitte des übergeordneten Containers aus, wobei der angegebene Abstand berücksichtigt wird. |
   | `Right` | Richtet die Einheit am rechten Rand des übergeordneten Containers aus, wobei der angegebene Abstand berücksichtigt wird. |

   {style="table-layout:auto"}

1. Legen Sie den **[!UICONTROL Border]** fest, der auf alle vier Seiten der Produktempfehlungseinheit angewendet wird:

   | Option | Beschreibung |
   | ------ | ----------- |
   | `Default` | Wendet die Standardformatvorlage für Rahmen an, die im zugehörigen Stylesheet angegeben ist. |
   | `None` | Stellt keine sichtbaren Zeichen für die Einheitenränder bereit. |
   | `Dotted` | Der Einheitenrahmen wird als gepunktete Linie angezeigt. |
   | `Dashed` | Der Einheitenrahmen wird als gestrichelte Linie angezeigt. |
   | `Solid` | Der Einheitenrahmen wird als durchgezogene Linie angezeigt. |
   | `Double` | Der Einheitenrahmen wird als doppelte Linie angezeigt. |
   | `Groove` | Der Einheitenrahmen wird als gerillte Linie angezeigt. |
   | `Ridge` | Der Einheitenrahmen wird als geriffelte Linie angezeigt. |
   | `Inset` | Der Einheitenrahmen wird als Einfügelinie angezeigt. |
   | `Outset` | Der Einheitenrahmen wird als Anfangslinie angezeigt. |

   {style="table-layout:auto"}

1. Wenn Sie einen anderen Rahmenstil als `None` festlegen, müssen Sie die Anzeigeoptionen für den Rahmen vervollständigen:

   | Option | Beschreibung |
   | ------ |------------ |
   | [!UICONTROL Border Color] | Geben Sie die Farbe an, indem Sie einen Musterabschnitt auswählen, auf die Farbauswahl klicken oder einen gültigen Farbnamen oder einen entsprechenden Hexadezimalwert eingeben. |
   | [!UICONTROL Border Width] | Geben Sie die Anzahl der Pixel für die Rahmenlinienbreite ein. |
   | [!UICONTROL Border Radius] | Geben Sie die Anzahl der Pixel ein, um die Größe des Radius festzulegen, mit dem jede Ecke des Rahmens gerundet werden soll. |

   {style="table-layout:auto"}

1. (Optional) Geben Sie die Namen der **[!UICONTROL CSS classes]** aus dem aktuellen Stylesheet an, die auf die Einheit angewendet werden sollen.

   Trennen Sie mehrere Klassennamen durch ein Leerzeichen.

1. Geben Sie Werte in Pixeln für die **[!UICONTROL Margins and Padding]** ein, um die äußeren Ränder und den inneren Abstand des Geräts zu bestimmen.

   Geben Sie die entsprechenden Werte in das Diagramm ein.

   | Container-Bereich | Beschreibung |
   | ------ | ----------- |
   | [!UICONTROL Margins] | Der Leerraum, der auf die Außenkante aller Seiten des Geräts angewendet wird. Optionen: `Top` / `Right` / `Bottom` / `Left` |
   | [!UICONTROL Padding] | Der Leerraum, der auf die Innenkante aller Seiten des Geräts angewendet wird. Optionen: `Top` / `Right` / `Bottom` / `Left` |

   {style="table-layout:auto"}
