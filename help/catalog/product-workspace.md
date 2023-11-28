---
title: Produktarbeitsbereich
description: Erfahren Sie mehr über die Einstellungen und Steuerelemente, die im Produktarbeitsbereich verfügbar sind.
exl-id: 8258b117-56d2-4d5f-9413-80d51fd5eae6
feature: Catalog Management, Products, Admin Workspace
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '463'
ht-degree: 0%

---

# Produktarbeitsbereich

Der Produktarbeitsbereich ist im Wesentlichen für alle Produktarten gleich, obwohl sich die Auswahl der Felder je nach verwendetem Attributsatz ändert. Die Produktattribute befinden sich oben im Formular, gefolgt von erweiterbaren Abschnitten der Produktinformationen. Wenn ein neues Produkt zum ersten Mal gespeichert wird, wird die _[!UICONTROL Store View]_wird oben links im Formular angezeigt.

![Produktarbeitsbereich](./assets/product-workspace-ee.png){width="700" zoomable="yes"}

## [!UICONTROL Enable Product] Einstellung

Der Online-Status des Produkts wird durch den Schalter oben im Formular angezeigt. Um den Online-Status zu ändern, legen Sie die **[!UICONTROL Enable Product]** Switch zu `Yes` oder `No`.

| Kontrolle | Beschreibung |
|-------- | ----------- |
| ![Ja umschalten](../assets/toggle-yes.png) | Gibt an, dass das Produkt online ist. |
| ![Umschalten](../assets/toggle-no.png) | Gibt an, dass das Produkt offline ist. |

{style="table-layout:auto"}

## Attributsatz

Der Name der [Attributset](attribute-sets.md) in der oberen linken Ecke angezeigt wird, und bestimmt, welche Felder im Produktdatensatz angezeigt werden. Um einen anderen Attributsatz auszuwählen, klicken Sie auf den Abwärtspfeil neben dem Standardnamen des Attributsatzes.

![Attributsatz](./assets/product-attribute-set.png){width="600" zoomable="yes"}

## Erweitern/Reduzieren

Um einen Abschnitt zu erweitern oder zu reduzieren, klicken Sie auf die Schaltfläche ![Erweiterungsauswahl](../assets/icon-display-expand.png) oder reduzieren ![Auswahl reduzieren](../assets/icon-display-collapse.png) Symbol.

## [!UICONTROL Save] Menü

Die _[!UICONTROL Save]_enthält mehrere Optionen, mit denen Sie ein Produkt speichern und fortsetzen, speichern und erstellen, speichern und duplizieren oder speichern und schließen können.

![Menü &quot;Speichern&quot;](./assets/product-save-menu.png){width="600" zoomable="yes"}

| Befehl | Beschreibung |
|--- |--- |
| [!UICONTROL Save] | Speichern Sie das aktuelle Produkt und arbeiten Sie weiter. |
| [!UICONTROL Save & New] | Speichern und schließen Sie das aktuelle Produkt und beginnen Sie ein neues Produkt basierend auf demselben Produkttyp und derselben Vorlage. |
| [!UICONTROL Save & Duplicate] | Speichern und schließen Sie das aktuelle Produkt und öffnen Sie eine neue Kopie. |
| [!UICONTROL Save & Close] | Speichern Sie das aktuelle Produkt und kehren Sie zum _[!UICONTROL Products]_Arbeitsbereich. |

{style="table-layout:auto"}

## Standardfeldwerte

Um beim Erstellen von Produkten Zeit zu sparen, verweist der Standardwert mehrerer Produktfelder auf Werte aus einem anderen Feld. Sie können entweder den Standardwert akzeptieren oder einen anderen eingeben. Die folgenden Felder haben automatisch Standardwerte generiert:

| Feld | Standard |
|----- |------- |
| [!UICONTROL SKU] | Basiert auf dem Produktnamen. |
| [!UICONTROL Meta Title] | Basiert auf dem Produktnamen. |
| [!UICONTROL Meta Keywords] | Basiert auf dem Produktnamen. |
| [!UICONTROL Meta Description] | Basiert auf Produktname und Beschreibung. |

{style="table-layout:auto"}

Die Platzhalter, die den Wert eines anderen Felds darstellen, sind in zweigeschweifte Klammern eingeschlossen. Jeder Attribut-Code, der im Produkt enthalten ist [Attributset](attribute-sets.md) kann als Platzhalter verwendet werden.

![Automatische Erstellung von Produktfeldern](../configuration-reference/catalog/assets/catalog-product-fields-auto-generation.png){width="600" zoomable="yes"}

Eine detaillierte Liste dieser Einstellungen finden Sie unter [Automatische Erstellung von Produktfeldern](../configuration-reference/catalog/catalog.md#product-fields-auto-generation) im _Konfigurationsreferenz_.

### Bearbeiten des Platzhalterwerts

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Catalog]** und wählen **[!UICONTROL Catalog]** darunter.

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL Product Fields Auto-Generation]** und nehmen Sie die erforderlichen Änderungen an den Platzhalterwerten vor.

   Wenn es beispielsweise einen bestimmten Suchbegriff gibt, den Sie für jedes Produkt oder eine Wortgruppe einbeziehen möchten, die Sie in jede Meta-Beschreibung aufnehmen möchten, geben Sie den Wert direkt in das entsprechende Feld ein.

   >[!NOTE]
   >
   >Wenn Sie die vorhandenen Platzhalterwerte beibehalten möchten, behalten Sie die doppelten geschweiften Klammern bei, die jedes Markup-Tag umschließen.

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save Config]**.

### Allgemeine Platzhalter

- `{{color}}`
- `{{country_of_manufacture}}`
- `{{description}}`
- `{{gender}}`
- `{{material}}`
- `{{name}}`
- `{{short_description}}`
- `{{size}}`
- `{{sku}}`
