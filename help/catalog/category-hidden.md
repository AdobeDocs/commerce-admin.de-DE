---
title: Ausgeblendete Kategorien
description: Erfahren Sie, wie Sie ausgeblendete Kategorien für interne Zwecke oder zum Verknüpfen mit einer Kategorie verwenden, die nicht im Navigationsmenü enthalten ist.
exl-id: 43aa74b3-b4cd-488d-aa58-fa2c468fe3a2
feature: Catalog Management, Categories
TQID: https://experienceleague.adobe.com/vXJFiYxeTBcRQxdc4XGrPEPKuBAcqr-mnuUlh1WIskM
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: c18ed297-2187-4aec-affb-9d9654eca6fc
subfeature_v2: id: e91a50b1-0b31-436e-9033-00e4776e94cb
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 186
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
