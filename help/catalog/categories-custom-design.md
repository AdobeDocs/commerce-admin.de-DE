---
title: Kategorien - Designeinstellungen
description: Erfahren Sie mehr über die Verwendung der [!UICONTROL Design]-Einstellungen zum Definieren des Aussehens einer Kategorie, aller zugehörigen Produktseiten und des Seiten-Layouts.
exl-id: 6dc216ac-1c52-4196-9c93-e5cad19901b5
feature: Catalog Management, Categories, Page Content
TQID: https://experienceleague.adobe.com/cRTRPl-UTfAKXY8rmtVKlnAZooVWpTCjSkVSdNHXp28
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c18ed297-2187-4aec-affb-9d9654eca6fc
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
subfeature_v2:
  - id: e91a50b1-0b31-436e-9033-00e4776e94cb
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 379
ht-degree: 0%

---

# Kategorien - Designeinstellungen

Im _[!UICONTROL Design]_&#x200B;Abschnitt erhalten Sie Kontrolle über das Erscheinungsbild einer Kategorie, alle zugehörigen Produktseiten und das Seitenlayout. Sie können eine Kategorieseite und die zugehörigen Produkte für eine Promotion anpassen oder die Kategorie unterscheiden. Sie können beispielsweise ein unverwechselbares Design für eine Marke oder eine spezielle Produktlinie entwickeln oder ein Update für einen bestimmten Zeitraum anwenden.

![Design-Einstellungen für eine Kategorie](./assets/category-design.png){width="600" zoomable="yes"}

>[!NOTE]
>
>Wenn dasselbe Produkt mehreren Kategorien mit unterschiedlichen Designeinstellungen für jede Kategorie zugewiesen wird, wird empfohlen, in den Konfigurationsoptionen für die Suchmaschinenoptimierung **Kategoriepfad für Produkt** = `Yes` [&#x200B; &#x200B;](../configuration-reference/catalog/catalog.md#search-engine-optimization). Um auf diese Einstellung zuzugreifen, gehen Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**, erweitern Sie **[!UICONTROL Catalog]**&#x200B;und wählen Sie **Katalog**&#x200B;unten im linken Bereich aus und erweitern Sie dann den Abschnitt **Suchmaschinenoptimierung**&#x200B;auf der Seite.

| Feld | Beschreibung |
|--- |--- |
| [!UICONTROL Use Parent Category Settings] | Ermöglicht der aktuellen Kategorie, die Design-Einstellungen von der übergeordneten Kategorie zu übernehmen. Wenn diese Option verwendet wird, sind alle anderen Felder im Abschnitt Design nicht mehr verfügbar. Optionen: `Yes` / ` No` |
| [!UICONTROL Theme] | Wendet ein benutzerdefiniertes Design auf die Kategorie an. |
| [!UICONTROL Layout] | Wendet ein anderes Layout auf die Kategorieseite an. Optionen: <br/>**[!UICONTROL No layout updates]**- Standardmäßig sind Layout-Aktualisierungen für Kategorieseiten nicht verfügbar.<br/>**[!UICONTROL Empty]** : Hiermit können Sie Ihr eigenes Seiten-Layout definieren. (XML muss verstanden werden.) <br/>**[!UICONTROL 1 column]**- Wendet ein einspaltiges Layout auf die Kategorieseite an.<br/>**[!UICONTROL 2 columns with left bar]** - Wendet ein zweispaltiges Layout mit einer linken Seitenleiste auf die Kategorieseite an. <br/>**[!UICONTROL 2 columns with right bar]**- Wendet ein zweispaltiges Layout mit einer rechten Seitenleiste auf die Kategorieseite an.<br/>**[!UICONTROL 3 columns]** - Wendet ein dreispaltiges Layout auf die Kategorieseite an.<br/>**[!UICONTROL Page -- Full Width]**- ([Page Builder](../page-builder/introduction.md)) Wendet das Layout mit voller Breite für CMS-Seiten auf die Kategorieseite an.<br/>**[!UICONTROL Category -- Full Width]** - (Seiten-Builder erforderlich) Wendet das Layout mit voller Breite für Kategorieseiten auf die Kategorieseite an. <br/>**[!UICONTROL Product -- Full Width]**- (Seiten-Builder erforderlich) Wendet das Layout mit voller Breite für Produktseiten auf die Kategorieseite an. |
| [!UICONTROL Custom Layout Update] | Listet die verfügbaren benutzerdefinierten Layout-Aktualisierungsdateien auf dem Server auf. Wählen Sie die benutzerdefinierte Layout-Aktualisierung aus, die Sie auf die Kategorie anwenden möchten. |
| [!UICONTROL Apply Design to Products] | Wenn diese Option aktiviert ist, werden die benutzerdefinierten Einstellungen auf alle Produkte in der Kategorie angewendet. |

{style="table-layout:auto"}

## [!UICONTROL Scheduled Design Update]

{{ce-feature}}

Im Abschnitt _[!UICONTROL Scheduled Design Update]_&#x200B;wird der Datumsbereich festgelegt, in dem ein benutzerdefinierter Entwurf auf Kategorieseiten angewendet wird.

| Feld | Beschreibung |
|--- |--- |
| [!UICONTROL Schedule Update From/To] | Bestimmt den Datumsbereich, in dem ein benutzerdefiniertes Layout auf die Kategorie angewendet wird. |

![Geplante Design-Aktualisierung](./assets/category-scheduled-design-update.png){width="600" zoomable="yes"}
