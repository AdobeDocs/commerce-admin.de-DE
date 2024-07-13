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

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. Wählen Sie im Kategoriebaum die Kategorie aus, die Sie ausblenden möchten, und gehen Sie wie folgt vor:

   - Setzen Sie **[!UICONTROL Is Active]** auf `Yes`.
   - Setzen Sie **[!UICONTROL Include in Menu]** auf `No`.

1. Setzen Sie im Abschnitt **[!UICONTROL Display Settings]** **[!UICONTROL Anchor]** auf `No`.

   ![Ausgeblendete Kategorie](./assets/hidden-categories.png){width="600" zoomable="yes"}

   Die ausgeblendete Kategorie ist aktiv, wird jedoch nicht im oberen Menü oder in der Navigation mit Ebenen angezeigt.

1. Führen Sie die folgenden Einstellungen für jede ausgeblendete Unterkategorie aus, um Unterkategorien zu erstellen:

   >[!NOTE]
   >
   >Obwohl die Kategorie ausgeblendet ist, können Sie darunter Unterkategorien erstellen und sie aktivieren.

   - Setzen Sie **[!UICONTROL Enable Category]** auf `Yes`.
   - Setzen Sie im Abschnitt **[!UICONTROL Display Settings]** **[!UICONTROL Anchor]** auf `Yes`.

   Als aktive Kategorien können Sie jetzt Links zu ihnen von anderen Stellen in Ihrem Geschäft aus erstellen, sie werden jedoch nicht im Menü angezeigt.

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save]**.
