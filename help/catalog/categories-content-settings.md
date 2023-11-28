---
title: Kategorien - Inhaltseinstellungen
description: Erfahren Sie mehr über die Verwendung der [!UICONTROL Content] -Einstellungen, um zusätzliche Inhalte zu definieren, die auf der Kategorieseite angezeigt werden.
exl-id: 988083e1-0993-4e08-b5e6-8b0855e56467
feature: Catalog Management, Categories, Page Content
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '449'
ht-degree: 0%

---

# Kategorien - Inhaltseinstellungen

Die _[!UICONTROL Content]_-Einstellungen bestimmen, ob zusätzliche Inhalte auf der Kategorieseite angezeigt werden. Zusätzlich zur Liste der Kategorieprodukte kann die Seite ein Bild, eine Beschreibung und einen CMS-Block enthalten. Sie können die [[!DNL Page Builder]](../page-builder/introduction.md) Content-Tools zur Definition der Kategoriebeschreibung.

## Fügen Sie die Kategoriebeschreibung in [!DNL Page Builder]

1. Öffnen Sie die Kategorie im Bearbeitungsmodus.

1. Hinunter scrollen und erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL Content]** Abschnitt.

   ![Kategorieinhalt](./assets/category-content.png){width="600" zoomable="yes"}

1. Oben rechts im **[!UICONTROL Description]** Bereich, klicken Sie **[!UICONTROL Edit with Page Builder]**.

1. Verwenden Sie die [[!DNL Page Builder]](../page-builder/introduction.md) Content-Tools in [vorhandenen Text bearbeiten](../page-builder/text.md) und fügen Sie bei Bedarf weitere Inhalte hinzu.

## [!DNL Page Builder] Vorschau

Wenn Sie die _Inhalt_ für eine vorhandene Kategorie, in der Inhalte mit [!DNL Page Builder], zeigt es eine Vorschau der **[!UICONTROL Description]** Inhalt, wie er auf der Kategorieseite angezeigt würde. Durch Klicken auf den Inhaltsbereich wird das [!DNL Page Builder] Arbeitsbereich, in dem Sie erforderliche Aktualisierungen vornehmen können.

![Beschreibung Vorschau](../page-builder/assets/pb-product-category-content-preview.png){width="500" zoomable="yes"}

Diese Inhaltsvorschau ist standardmäßig für die Produkt- und Kategorieformulare aktiviert. Wenn die Leistung durch das Laden der Vorschau beeinträchtigt wird, können Sie die Vorschau im [Content Management-Konfiguration](../configuration-reference/general/content-management.md#advanced-content-tools) -Einstellungen.

## Kategoriebeschreibung im Editor hinzufügen

Geben Sie nur einfache ASCII-Zeichen in das Textfeld ein. Wenn Sie Text aus einem Textverarbeitungsprogramm einfügen, speichern Sie ihn zuerst als einfache .TXT-Datei, um unsichtbare Steuerzeichen zu entfernen.

Weitere Informationen finden Sie unter [WYSIWYG-Editor](../content-design/editor.md).

1. Öffnen Sie die Kategorie im Bearbeitungsmodus.

1. Hinunter scrollen und erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL Content]** Abschnitt.

   ![Kategorieinhalt](./assets/category-content-ce.png){width="500" zoomable="yes"}

1. Kategorie eingeben **[!UICONTROL Description]** und verwenden Sie [Editor-Symbolleiste](../content-design/editor.md) , um das Format nach Bedarf anzupassen.

   Sie können die untere rechte Ecke ziehen, um die Höhe des Textfelds zu ändern.

## Hinzufügen eines CMS-Blocks zur Kategorieseite

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. Wählen Sie im Kategoriebaum die Kategorie aus, die Sie bearbeiten möchten.

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL Content]** Abschnitt.

1. Für **[!UICONTROL Add the CMS block]**, wählen Sie einen Baustein aus, den Sie hinzufügen möchten.

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL Display Settings]** Abschnitt.

1. Legen Sie die **[!UICONTROL Display Mode]** auf einen der folgenden Werte zu:

   - `Static block only`
   - `Static block and products`

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save]** und überprüfen Sie die Blockanzeige auf der Storefront (Cache-Aktualisierung erforderlich).

## Inhaltseinstellungen - Referenz

| Einstellung | [Anwendungsbereich](../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Category Image] | Store-Ansicht | Gibt ein Bild für den oberen Rand der Kategorieseite an. Methoden: <br/><br/>**[!UICONTROL Upload]**- Lädt eine Bilddatei von Ihrem lokalen Computer in die Galerie hoch und verwendet sie als Kategoriebild.<br/><br/>**[!UICONTROL Select from Gallery]** - Fordert Sie auf, ein vorhandenes Bild aus der Galerie auszuwählen. <br/><br/>![Kamerasymbol des Seitenaufbaus](../assets/icon-camera.png) - Ziehen Sie entweder eine Bilddatei auf die Kachel Kamera oder navigieren Sie zum Bild und wählen Sie es aus Ihrem lokalen Dateisystem aus. |
| [!UICONTROL Description] | Store-Ansicht | Gibt eine Beschreibung an, die auf der Kategorieseite angezeigt wird. <br/><br/>**[!UICONTROL Edit with Page Builder]**- Öffnet die [[!DNL Page Builder] Arbeitsbereich](../page-builder/workspace.md), wo Sie die Beschreibung bearbeiten können.<br/><br/>**[!UICONTROL Show / Hide Editor]** - Schaltet die Anzeige zwischen dem WYSIWYG-Editor und dem HTML-Modus um. |
| [!UICONTROL Add CMS Block] | Store-Ansicht | Fügt eine vorhandene [CMS-Block](../content-design/blocks.md) zur Kategorieseite hinzu. |

{style="table-layout:auto"}
