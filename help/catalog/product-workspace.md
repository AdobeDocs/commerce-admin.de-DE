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

Der Produktarbeitsbereich ist im Wesentlichen für alle Produktarten gleich, obwohl sich die Auswahl der Felder je nach verwendetem Attributsatz ändert. Die Produktattribute befinden sich oben im Formular, gefolgt von erweiterbaren Abschnitten der Produktinformationen. Wenn ein neues Produkt zum ersten Mal gespeichert wird, wird die &quot;_[!UICONTROL Store View]_&quot;-Auswahl oben links im Formular angezeigt.

![Produktarbeitsbereich](./assets/product-workspace-ee.png){width="700" zoomable="yes"}

## Einstellung [!UICONTROL Enable Product]

Der Online-Status des Produkts wird durch den Schalter oben im Formular angezeigt. Um den Online-Status zu ändern, setzen Sie den **[!UICONTROL Enable Product]** -Schalter auf `Yes` oder `No`.

| Kontrolle | Beschreibung |
|-------- | ----------- |
| ![Ja umschalten](../assets/toggle-yes.png) | Gibt an, dass das Produkt online ist. |
| ![Umschalten Nr.](../assets/toggle-no.png) | Gibt an, dass das Produkt offline ist. |

{style="table-layout:auto"}

## Attributsatz

Der Name des [Attributsatzes](attribute-sets.md) wird oben links angezeigt und bestimmt die Felder, die im Produktdatensatz angezeigt werden. Um einen anderen Attributsatz auszuwählen, klicken Sie auf den Abwärtspfeil neben dem Standardnamen des Attributsatzes.

![Attributsatz](./assets/product-attribute-set.png){width="600" zoomable="yes"}

## Erweitern/Reduzieren

Um einen Abschnitt zu erweitern oder zu reduzieren, klicken Sie auf das Symbol ![Erweiterungsauswahl](../assets/icon-display-expand.png) erweitern oder auf das Symbol ![Reduzieren-Selektor](../assets/icon-display-collapse.png).

## Menü [!UICONTROL Save]

Das Menü _[!UICONTROL Save]_enthält mehrere Optionen, mit denen Sie ein Produkt speichern und fortsetzen, speichern und erstellen, speichern und duplizieren oder speichern und schließen können.

![Menü &quot;Speichern&quot;](./assets/product-save-menu.png){width="600" zoomable="yes"}

| Befehl | Beschreibung |
|--- |--- |
| [!UICONTROL Save] | Speichern Sie das aktuelle Produkt und arbeiten Sie weiter. |
| [!UICONTROL Save & New] | Speichern und schließen Sie das aktuelle Produkt und beginnen Sie ein neues Produkt basierend auf demselben Produkttyp und derselben Vorlage. |
| [!UICONTROL Save & Duplicate] | Speichern und schließen Sie das aktuelle Produkt und öffnen Sie eine neue Kopie. |
| [!UICONTROL Save & Close] | Speichern Sie das aktuelle Produkt und kehren Sie zum Arbeitsbereich _[!UICONTROL Products]_zurück. |

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

Die Platzhalter, die den Wert eines anderen Felds darstellen, sind in zweigeschweifte Klammern eingeschlossen. Jeder Attributcode, der im Produkt [Attributsatz](attribute-sets.md) enthalten ist, kann als Platzhalter verwendet werden.

![Automatische Erstellung von Produktfeldern](../configuration-reference/catalog/assets/catalog-product-fields-auto-generation.png){width="600" zoomable="yes"}

Eine detaillierte Liste dieser Einstellungen finden Sie unter [Automatische Erstellung von Produktfeldern](../configuration-reference/catalog/catalog.md#product-fields-auto-generation) in der _Konfigurationsreferenz_.

### Bearbeiten des Platzhalterwerts

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bedienfeld den Wert **[!UICONTROL Catalog]** und wählen Sie unter &quot;**[!UICONTROL Catalog]**&quot;.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Product Fields Auto-Generation]** und nehmen Sie die erforderlichen Änderungen an den Platzhalterwerten vor.

   Wenn es beispielsweise einen bestimmten Suchbegriff gibt, den Sie für jedes Produkt oder eine Wortgruppe einbeziehen möchten, die Sie in jede Meta-Beschreibung aufnehmen möchten, geben Sie den Wert direkt in das entsprechende Feld ein.

   >[!NOTE]
   >
   >Wenn Sie die vorhandenen Platzhalterwerte beibehalten möchten, behalten Sie die doppelten geschweiften Klammern bei, die jedes Markup-Tag umschließen.

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save Config]**.

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
