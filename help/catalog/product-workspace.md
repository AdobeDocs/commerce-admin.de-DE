---
title: Produktarbeitsbereich
description: Erfahren Sie mehr über die Einstellungen und Steuerelemente, die im Produktarbeitsbereich verfügbar sind.
exl-id: 8258b117-56d2-4d5f-9413-80d51fd5eae6
feature: Catalog Management, Products, Admin Workspace
TQID: https://experienceleague.adobe.com/O9e0Z-bHxbokLZd4RbT1puWWAGWnF7SDqvGcc4Bteco
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c18ed297-2187-4aec-affb-9d9654eca6fc
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: ccaac3a13a346ce192a724efb3384ef2d612c980
workflow-type: tm+mt
source-wordcount: 467
ht-degree: 0%

---

# Produktarbeitsbereich

Der Arbeitsbereich Produkt ist für alle Produkttypen grundsätzlich identisch, obwohl sich die Auswahl der Felder je nach verwendetem Attributsatz ändert. Die Produktattribute befinden sich am Anfang des Formulars, gefolgt von erweiterbaren Abschnitten mit Produktinformationen. Wenn ein neues Produkt zum ersten Mal gespeichert wird, wird die _[!UICONTROL Store View]_-Auswahl oben links im Formular angezeigt.

![Produktarbeitsbereich](./assets/product-workspace-ee.png){width="700" zoomable="yes"}

## [!UICONTROL Enable Product]

Der Online-Status des Produkts wird durch den Schalter am oberen Rand des Formulars angezeigt. Um den Online-Status zu ändern, stellen Sie den **[!UICONTROL Enable Product]** auf `Yes` oder `No`.

| Kontrolle | Beschreibung |
|-------- | ----------- |
| ![Ja ein/aus](../assets/toggle-yes.png) | Gibt an, dass das Produkt online ist. |
| ![Umschalten auf](../assets/toggle-no.png) | Gibt an, dass das Produkt offline ist. |

{style="table-layout:auto"}

## Attributsatz

Der Name des [Attributsatzes](attribute-sets.md) wird in der oberen linken Ecke angezeigt und bestimmt die Felder, die im Produktdatensatz angezeigt werden. Um einen anderen Attributsatz auszuwählen, klicken Sie auf den Abwärtspfeil neben dem Namen des standardmäßigen Attributsatzes.

![Attribut festgelegt](./assets/product-attribute-set.png){width="600" zoomable="yes"}

## Erweitern/Reduzieren

Um einen Abschnitt zu erweitern oder zu reduzieren, klicken Sie entweder auf das Symbol ![Erweiterungsauswahl](../assets/icon-display-expand.png) oder auf das Symbol ![Auswahl reduzieren](../assets/icon-display-collapse.png).

## Menü [!UICONTROL Save]

Das Menü _[!UICONTROL Save]_&#x200B;enthält mehrere Optionen, mit denen Sie speichern und fortfahren, ein Produkt speichern und erstellen, das Produkt speichern und duplizieren oder speichern und schließen können.

![Menü „Speichern](./assets/product-save-menu.png){width="600" zoomable="yes"}

| Befehl | Beschreibung |
|--- |--- |
| [!UICONTROL Save] | Speichern Sie das aktuelle Produkt und arbeiten Sie weiter. |
| [!UICONTROL Save & New] | Speichern und schließen Sie das aktuelle Produkt, und beginnen Sie ein neues Produkt basierend auf demselben Produkttyp und derselben Vorlage. |
| [!UICONTROL Save & Duplicate] | Speichern und schließen Sie das aktuelle Produkt, und öffnen Sie eine neue Duplikatkopie. |
| [!UICONTROL Save & Close] | Speichern Sie das aktuelle Produkt und kehren Sie zum Arbeitsbereich _[!UICONTROL Products]_&#x200B;zurück. |

{style="table-layout:auto"}

## Standardfeldwerte

Um beim Erstellen von Produkten Zeit zu sparen, verweist der Standardwert mehrerer Produktfelder auf Werte aus einem anderen Feld. Sie können entweder den Standardwert annehmen oder einen anderen eingeben. Die folgenden Felder haben automatisch Standardwerte generiert:

| Feld | Standard |
|----- |------- |
| [!UICONTROL SKU] | Basierend auf Produktname. |
| [!UICONTROL Meta Title] | Basierend auf Produktname. |
| [!UICONTROL Meta Keywords] | Basierend auf Produktname. |
| [!UICONTROL Meta Description] | Basierend auf Produktname und Beschreibung. |

{style="table-layout:auto"}

Die Platzhalter, die den Wert eines anderen Felds darstellen, werden in geschweifte Klammern eingeschlossen. Jeder Attributcode, der im Produkt ([) enthalten &#x200B;](attribute-sets.md), kann als Platzhalter verwendet werden.

![Automatische Generierung von Produktfeldern](../configuration-reference/catalog/assets/catalog-product-fields-auto-generation.png){width="600" zoomable="yes"}

Eine detaillierte Liste dieser Einstellungen finden Sie unter [Automatische Generierung von Produktfeldern](../configuration-reference/catalog/catalog.md#product-fields-auto-generation) in der _Konfigurationsreferenz_.

### Bearbeiten des Platzhalterwerts

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Catalog]** und wählen Sie darunter **[!UICONTROL Catalog]**.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Product Fields Auto-Generation]** und nehmen Sie die erforderlichen Änderungen an den Platzhalterwerten vor.

   Wenn es beispielsweise ein bestimmtes Keyword gibt, das Sie für jedes Produkt oder eine Phrase in jede Metabeschreibung aufnehmen möchten, geben Sie den Wert direkt in das entsprechende Feld ein.

   >[!NOTE]
   >
   >Wenn Sie die vorhandenen Platzhalterwerte beibehalten möchten, behalten Sie die doppelten geschweiften Klammern bei, die jedes Markup-Tag einschließen.

1. Klicken Sie abschließend auf **[!UICONTROL Save Config]**.

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

