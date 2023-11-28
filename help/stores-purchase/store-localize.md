---
title: Lokalisierung speichern
description: Erfahren Sie, wie Sie eine Store- oder Store-Ansicht lokalisieren.
exl-id: 64e1b431-f599-444c-9d39-207bb95f0400
topic: Commerce, Localization
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '735'
ht-degree: 0%

---

# Lokalisierung speichern

Der Großteil des Texts, der auf Seiten in Ihrem Store hartcodiert zu sein scheint, kann sofort in eine andere Sprache geändert werden, indem das Gebietsschema der Ansicht geändert wird. Das Ändern des Gebietsschemas übersetzt den Text nicht wörtlich, sondern verweist einfach auf eine andere Übersetzungstabelle, die den im gesamten Speicher verwendeten Schnittstellentext bereitstellt. Zu dem Text, der geändert werden kann, gehören Navigationstitel, Beschriftungen, Schaltflächen und Links wie _Mein Warenkorb_ und _Mein Konto_. Sie können auch die [Inline-Übersetzung](../configuration-reference/advanced/developer.md) -Tool, um Text in der Benutzeroberfläche zu berühren.

Sprachpakete finden Sie unter [Übersetzungen und Lokalisierung][1]{:target=&quot;_blank&quot;} auf Commerce Marketplace. Neue Erweiterungen werden fortlaufend zu Marketplace hinzugefügt. Überprüfen Sie daher häufig.

## Schritt 1: Installieren eines Sprachpakets

Befolgen Sie die Standardanweisungen zum Installieren der Sprachpack-Erweiterung. Detaillierte Informationen zum Installieren einer Erweiterung finden Sie unter [Allgemeine CLI-Installation][2] im _Erweiterungshandbuch_.

## Schritt 2: Erstellen einer Store-Ansicht für die Sprache

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL All Stores]**.

1. Klicken **[!UICONTROL Create Store View]**.

1. Legen Sie die Optionen für die neue Store-Ansicht fest:

   - **[!UICONTROL Store]** — Wählen Sie den Store aus, der der Ansicht übergeordnet ist.

   - **[!UICONTROL Name]** — Geben Sie einen Namen für die Store-Ansicht ein. Beispiel: Portugiesisch.

     In der Kopfzeile des Stores wird der Name in der _Sprachauswahl_.

   - **[!UICONTROL Code]** — Geben Sie einen Code in Kleinbuchstaben ein, um die Ansicht zu identifizieren. Beispiel: `portuguese`.

   - **[!UICONTROL Status]** — Um die Ansicht zu aktivieren, setzen Sie auf `Enabled`.

   - **[!UICONTROL Sort Order]** — (Optional) Geben Sie eine Zahl ein, um die Sequenz zu bestimmen, in der diese Ansicht mit anderen Ansichten aufgeführt wird.

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save Store View]**.

## Schritt 3: Gebietsschema der Store-Ansicht ändern

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Legen Sie in der oberen linken Ecke **[!UICONTROL Store View]** in die spezifische Ansicht, in der die Konfiguration angewendet werden soll.

1. Wenn Sie aufgefordert werden, den Perimeterwechsel zu bestätigen, klicken Sie auf **[!UICONTROL OK]**.

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL Locale Options]** Abschnitt.

1. Löschen Sie die **[!UICONTROL Use Website]** Kontrollkästchen und festlegen **[!UICONTROL Locale]** in die Sprache, die Sie der Ansicht zuweisen möchten.

   Wenn mehrere Varianten der Sprache verfügbar sind, wählen Sie unbedingt eine für die jeweilige Region oder den Dialekt.

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save Config]**.

   Nachdem Sie die Sprache des Gebietsschemas geändert haben, den verbleibenden von Ihnen erstellten Inhalt, einschließlich Produktnamen und Beschreibungen, Kategorien, [CMS](../content-design/page-translate.md) Seiten und Blöcke müssen für jede Store-Ansicht separat übersetzt werden.

## Lokalisieren von Produkten

Wenn Ihr Store mehrere Ansichten in verschiedenen Sprachen hat, sind in jeder Store-Ansicht dieselben Produkte verfügbar. Sie können unabhängig von der Sprache dieselben grundlegenden Produktinformationen wie SKU, Preis und Lagerbestand verwenden. Übersetzen Sie dann nur den Produktnamen, die Beschreibungsfelder und Metadaten nach Bedarf für jede Sprache.

### Schritt 1: Produktfelder übersetzen

1. Im _Admin_ Seitenleiste, navigieren Sie zu  **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Suchen Sie im Raster das zu übersetzende Produkt und öffnen Sie es im Bearbeitungsmodus.

1. Legen Sie in der oberen linken Ecke **[!UICONTROL Store View]** zur Ansicht für die Übersetzung hinzu und klicken Sie auf **[!UICONTROL OK]** bei Aufforderung zur Bestätigung.

1. Gehen Sie für jedes zu bearbeitende Feld wie folgt vor:

   - Deaktivieren Sie die **[!UICONTROL Use Default Value]** rechts neben dem Feld.

   - Fügen Sie den übersetzten Text in das Feld ein oder geben Sie ihn ein.

   Übersetzen Sie alle Textfelder, einschließlich [image](../catalog/catalog-images-video.md) Beschriftungen und Alternativtext, [Suchmaschinenoptimierung](../catalog/product-search-engine-optimization.md) Felder und alle [Benutzerdefinierte Optionen](../catalog/settings-advanced-custom-options.md) Informationen.

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save]**.

### Schritt 2: Übersetzen von Feldbezeichnungen

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Product]**.

1. Suchen Sie in der Liste das zu übersetzende Attribut und öffnen Sie es im Bearbeitungsmodus.

1. Wählen Sie im linken Bereich die Option **[!UICONTROL Manage Labels]**.

1. Im _[!UICONTROL Manage Titles]_eingeben, geben Sie für jede Store-Ansicht einen übersetzten Titel ein.

   ![Übersetzte Beschriftungen eingeben](./assets/product-attribute-labels-translate.png){width="600" zoomable="yes"}

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save Attribute]**.

### Schritt 3: Alle Kategorien übersetzen

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Catalog]** > **Kategorien**.

1. Legen Sie in der linken oberen Ecke **[!UICONTROL Store View]** zur Ansicht für die Übersetzung hinzu und klicken Sie auf **[!UICONTROL OK]** bei Aufforderung zur Bestätigung.

1. Suchen Sie im Baum die zu übersetzende Kategorie und öffnen Sie sie im Bearbeitungsmodus.

1. Für _Basisinformationen_, übersetzen **[!UICONTROL Category Name]**.

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die _[!UICONTROL Content]_Abschnitt und Übersetzung **[!UICONTROL Description]**.

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL Search Engine Optimization Settings]** und übersetzen Sie die folgenden Felder:

   - **[!UICONTROL Meta Title]**
   - **[!UICONTROL Meta Keywords]**
   - **[!UICONTROL Meta Description]**

1. Unter dem _[!UICONTROL Search Engine Optimization Settings]_führen Sie die folgenden Schritte aus, um die **[!UICONTROL URL Key]**:

   - Löschen Sie die **[!UICONTROL Use Default Value]** rechts neben dem Feld.

   - Geben Sie den übersetzten Text ein.

   - Stellen Sie sicher, dass die Variable **[!UICONTROL Create Permanent Redirect for old URL]** aktiviert ist.

   ![URL-Schlüssel übersetzen](./assets/category-translate-url-key.png)

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save Category]**.

1. Wiederholen Sie den Vorgang für alle Kategorien, die im Store verwendet werden.

### Schritt 4: Optionen für Produktattribute und Attribute übersetzen

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Product]**.

1. Wählen Sie das zu übersetzende Attribut aus.

1. Auswählen **[!UICONTROL Manage Labels]** auf der linken Seite und legen Sie die **[!UICONTROL Managed Titles]** Optionen zum Definieren der Attributtitelübersetzungen.

1. Auswählen **[!UICONTROL Properties]** auf der linken Seite und geben Sie die übersetzten Attributoptionen in die **[!UICONTROL Manage Options]** Abschnitt.

   ![Optionen verwalten](./assets/manage-option-tab.png){width="600" zoomable="yes"}

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save Attribute]**.


[1]: https://marketplace.magento.com/extensions/content-customizations/translations-localization.html
[2]: https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/extensions.html
