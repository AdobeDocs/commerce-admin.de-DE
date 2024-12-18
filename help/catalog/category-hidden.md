---
title: Ausgeblendete Kategorien
description: Erfahren Sie, wie Sie ausgeblendete Kategorien für interne Zwecke oder zum Verknüpfen mit einer Kategorie verwenden, die nicht im Navigationsmenü enthalten ist.
exl-id: 43aa74b3-b4cd-488d-aa58-fa2c468fe3a2
feature: Catalog Management, Categories
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 0%

---

# Ausgeblendete Kategorien

Es gibt viele Möglichkeiten, ausgeblendete Kategorien zu verwenden. Möglicherweise möchten Sie zusätzliche Kategorieebenen für Ihre eigenen internen Zwecke erstellen, Ihren Kunden jedoch nur die übergeordneten Kategorien anzeigen. Oder Sie möchten eine Verknüpfung zu einer Kategorie erstellen, die nicht im Navigationsmenü enthalten ist.

## Erstellen ausgeblendeter Kategorien

1. Navigieren Sie in der _Admin_-Seitenleiste zu **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. Wählen Sie in der Kategoriestruktur die Kategorie aus, die Sie ausblenden möchten, und führen Sie dann folgende Schritte aus:

   - Legen Sie **[!UICONTROL Is Active]** auf `Yes` fest.
   - Legen Sie **[!UICONTROL Include in Menu]** auf `No` fest.

1. Legen Sie im **[!UICONTROL Display Settings]** Abschnitt **[!UICONTROL Anchor]** auf `No` fest.

   ![Ausgeblendete Kategorie](./assets/hidden-categories.png){width="600" zoomable="yes"}

   Die ausgeblendete Kategorie ist aktiv, wird jedoch nicht im oberen Menü oder in der mehrschichtigen Navigation angezeigt.

1. Führen Sie die folgenden Einstellungen für jede ausgeblendete Unterkategorie aus, um Unterkategorien zu erstellen:

   >[!NOTE]
   >
   >Obwohl die Kategorie ausgeblendet ist, können Sie darunter Unterkategorien erstellen und diese aktivieren.

   - Legen Sie **[!UICONTROL Enable Category]** auf `Yes` fest.
   - Legen Sie im **[!UICONTROL Display Settings]** Abschnitt **[!UICONTROL Anchor]** auf `Yes` fest.

   Als aktive Kategorien können Sie jetzt von anderen Stellen in Ihrem Store aus eine Verknüpfung zu ihnen herstellen, sie werden jedoch nicht im Menü angezeigt.

1. Klicken Sie abschließend auf **[!UICONTROL Save]**.
