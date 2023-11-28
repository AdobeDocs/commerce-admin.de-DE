---
title: Ausgeblendete Kategorien
description: Erfahren Sie, wie Sie ausgeblendete Kategorien für interne Zwecke verwenden oder mit einer Kategorie verknüpfen, die nicht im Navigationsmenü enthalten ist.
exl-id: 43aa74b3-b4cd-488d-aa58-fa2c468fe3a2
feature: Catalog Management, Categories
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 0%

---

# Ausgeblendete Kategorien

Es gibt viele Möglichkeiten, ausgeblendete Kategorien zu verwenden. Möglicherweise möchten Sie für Ihre eigenen internen Zwecke zusätzliche Kategorieebenen erstellen, für Ihre Kunden jedoch nur die Kategorien auf höherer Ebene anzeigen. Sie können auch eine Verknüpfung zu einer Kategorie erstellen, die nicht im Navigationsmenü enthalten ist.

## Verborgene Kategorien erstellen

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. Wählen Sie im Kategoriebaum die Kategorie aus, die Sie ausblenden möchten, und gehen Sie wie folgt vor:

   - Satz **[!UICONTROL Is Active]** nach `Yes`.
   - Satz **[!UICONTROL Include in Menu]** nach `No`.

1. Im **[!UICONTROL Display Settings]** Abschnitt, festlegen **[!UICONTROL Anchor]** nach `No`.

   ![Ausgeblendete Kategorie](./assets/hidden-categories.png){width="600" zoomable="yes"}

   Die ausgeblendete Kategorie ist aktiv, wird jedoch nicht im oberen Menü oder in der Navigation mit Ebenen angezeigt.

1. Führen Sie die folgenden Einstellungen für jede ausgeblendete Unterkategorie aus, um Unterkategorien zu erstellen:

   >[!NOTE]
   >
   >Obwohl die Kategorie ausgeblendet ist, können Sie darunter Unterkategorien erstellen und sie aktivieren.

   - Satz **[!UICONTROL Enable Category]** nach `Yes`.
   - Im **[!UICONTROL Display Settings]** Abschnitt, festlegen **[!UICONTROL Anchor]** nach `Yes`.

   Als aktive Kategorien können Sie jetzt Links zu ihnen von anderen Stellen in Ihrem Geschäft aus erstellen, sie werden jedoch nicht im Menü angezeigt.

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save]**.
