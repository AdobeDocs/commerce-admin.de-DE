---
title: Kategorien - Inhaltseinstellungen
description: Erfahren Sie mehr über die Verwendung der Einstellungen für [!UICONTROL Content] , um zusätzliche Inhalte zu definieren, die auf der Kategorieseite angezeigt werden.
exl-id: 988083e1-0993-4e08-b5e6-8b0855e56467
feature: Catalog Management, Categories, Page Content
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '449'
ht-degree: 0%

---

# Kategorien - Inhaltseinstellungen

Die Einstellungen _[!UICONTROL Content]_bestimmen, ob zusätzliche Inhalte auf der Kategorieseite angezeigt werden. Zusätzlich zur Liste der Kategorieprodukte kann die Seite ein Bild, eine Beschreibung und einen CMS-Block enthalten. Sie können die [[!DNL Page Builder]](../page-builder/introduction.md)-Inhaltstools verwenden, um die Kategoriebeschreibung zu definieren.

## Kategoriebeschreibung in [!DNL Page Builder] hinzufügen

1. Öffnen Sie die Kategorie im Bearbeitungsmodus.

1. Scrollen Sie nach unten und erweitern Sie den Abschnitt **[!UICONTROL Content]** um den ![Erweiterungsselektor](../assets/icon-display-expand.png).

   ![Kategorieinhalt](./assets/category-content.png){width="600" zoomable="yes"}

1. Klicken Sie oben rechts im Bereich **[!UICONTROL Description]** auf **[!UICONTROL Edit with Page Builder]**.

1. Verwenden Sie die &quot;[[!DNL Page Builder]](../page-builder/introduction.md)&quot;-Inhaltstools, um [ vorhandenen Text zu bearbeiten](../page-builder/text.md) und weitere Inhalte hinzuzufügen (falls erforderlich).

## [!DNL Page Builder] Vorschau

Wenn Sie den Abschnitt _Inhalt_ für eine vorhandene Kategorie erweitern, in der Inhalte mit [!DNL Page Builder] erstellt werden, wird eine Vorschau des Inhalts mit **[!UICONTROL Description]** so angezeigt, wie er auf der Kategorieseite angezeigt würde. Durch Klicken auf den Inhaltsbereich wird der Arbeitsbereich [!DNL Page Builder] geöffnet, in dem Sie erforderliche Aktualisierungen vornehmen können.

![Vorschau der Beschreibung](../page-builder/assets/pb-product-category-content-preview.png){width="500" zoomable="yes"}

Diese Inhaltsvorschau ist standardmäßig für die Produkt- und Kategorieformulare aktiviert. Wenn die Leistung durch das Laden der Vorschau beeinträchtigt wird, können Sie die Vorschau in den Einstellungen für die [Konfiguration des Content Managements](../configuration-reference/general/content-management.md#advanced-content-tools) deaktivieren.

## Kategoriebeschreibung im Editor hinzufügen

Geben Sie nur einfache ASCII-Zeichen in das Textfeld ein. Wenn Sie Text aus einem Textverarbeitungsprogramm einfügen, speichern Sie ihn zuerst als einfache .TXT-Datei, um unsichtbare Steuerzeichen zu entfernen.

Weitere Informationen finden Sie unter [WYSIWYG-Editor](../content-design/editor.md).

1. Öffnen Sie die Kategorie im Bearbeitungsmodus.

1. Scrollen Sie nach unten und erweitern Sie den Abschnitt **[!UICONTROL Content]** um den ![Erweiterungsselektor](../assets/icon-display-expand.png).

   ![Kategorieinhalt](./assets/category-content-ce.png){width="500" zoomable="yes"}

1. Geben Sie die Kategorie **[!UICONTROL Description]** ein und verwenden Sie die [Editor-Symbolleiste](../content-design/editor.md), um die Formatierung nach Bedarf vorzunehmen.

   Sie können die untere rechte Ecke ziehen, um die Höhe des Textfelds zu ändern.

## Hinzufügen eines CMS-Blocks zur Kategorieseite

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. Wählen Sie im Kategoriebaum die Kategorie aus, die Sie bearbeiten möchten.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) im Abschnitt **[!UICONTROL Content]** .

1. Wählen Sie für **[!UICONTROL Add the CMS block]** einen Block aus, den Sie hinzufügen möchten.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) im Abschnitt **[!UICONTROL Display Settings]** .

1. Setzen Sie den **[!UICONTROL Display Mode]** auf einen der folgenden Werte:

   - `Static block only`
   - `Static block and products`

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save]** und überprüfen Sie die Blockanzeige auf der Storefront (Cache-Aktualisierung erforderlich).

## Inhaltseinstellungen - Referenz

| Einstellung | [Umfang](../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Category Image] | Store-Ansicht | Gibt ein Bild für den oberen Rand der Kategorieseite an. Methoden: <br/><br/>**[!UICONTROL Upload]**- Lädt eine Bilddatei von Ihrem lokalen Computer in die Galerie hoch und verwendet sie als Kategoriebild.<br/><br/>**[!UICONTROL Select from Gallery]** - Erfordert Sie zur Auswahl eines vorhandenen Bildes aus der Galerie. <br/><br/>![Seiten-Builder-Kamerasymbol](../assets/icon-camera.png) - Ziehen Sie eine Bilddatei auf die Kachel &quot;Kamera&quot;oder navigieren Sie zum Bild und wählen Sie es aus Ihrem lokalen Dateisystem aus. |
| [!UICONTROL Description] | Store-Ansicht | Gibt eine Beschreibung an, die auf der Kategorieseite angezeigt wird. <br/><br/>**[!UICONTROL Edit with Page Builder]**- Öffnet den [[!DNL Page Builder] Arbeitsbereich](../page-builder/workspace.md), in dem Sie die Beschreibung bearbeiten können.<br/><br/>**[!UICONTROL Show / Hide Editor]** - Schaltet die Anzeige zwischen dem WYSIWYG-Editor und dem HTML-Modus um. |
| [!UICONTROL Add CMS Block] | Store-Ansicht | Fügt der Kategorieseite einen vorhandenen [CMS-Block](../content-design/blocks.md) hinzu. |

{style="table-layout:auto"}
