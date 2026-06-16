---
title: Kundensegmente in Preisregeln
description: Erfahren Sie, wie Sie Kundensegmente mit einer Warenkorb-Preisregel verknüpfen, damit Sie zielgerichtete Promotions für Ihren Store definieren können.
exl-id: eaa04e7a-c0f9-4f09-8e65-75965ccbdc69
feature: Customers, Configuration, Price Rules
TQID: https://experienceleague.adobe.com/MSMNikJwG2lQuLlQxnK82zjCOeF-u8JEjmabKFJgpZU
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 232
ht-degree: 0%

---

# Kundensegmente in Preisregeln

{{ee-feature}}

Ein Kundensegment kann für zielgerichtete Promotions verwendet werden, indem es mit einer [Warenkorb-Preisregel) verknüpft &#x200B;](../merchandising-promotions/price-rules-cart.md).

![Warenkorb-Preisregel - Zielkundensegment](assets/price-rule-cart-condition-segments.png){width="700" zoomable="yes"}

_&#x200B;**So verknüpfen Sie ein Segment mit einer Warenkorb-Preisregel:**&#x200B;_

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Marketing]** > _Promotions_ > **[!UICONTROL Cart Price Rules]**.

1. Öffnen Sie eine neue oder vorhandene Regel:

   * Um eine neue Regel zu verwenden, klicken Sie oben rechts auf **[!UICONTROL Add New Rule]** .
   * Um eine vorhandene Regel zu verwenden, klicken Sie auf die Regel in der Liste, um sie im Bearbeitungsmodus zu öffnen.

1. Scrollen Sie nach unten und erweitern Sie den Abschnitt **[!UICONTROL Conditions]** .

1. Fügen Sie die Bedingung hinzu.

   * Klicken Sie auf _Symbol_ Hinzufügen![&#x200B; (](../assets/icon-add-green-circle.png)), um die Liste der Bedingungen anzuzeigen. Wählen Sie dann **[!UICONTROL Customer Segment]**.

   ![Warenkorb-Preisregel - Kundensegmentbedingung hinzufügen](assets/condition-customer-segment.png){width="600" zoomable="yes"}

   Standardmäßig ist die Bedingung so eingestellt, dass sie eine entsprechende Bedingung findet. Klicken Sie bei Bedarf auf den Link **[!UICONTROL matches]** und ändern Sie den Operator in einen der folgenden:

   * `does not match`
   * `is one of`
   * `is not one of`

   ![Bedingungsoperator](assets/price-rule-condition-customer-segment-operator.png){width="600" zoomable="yes"}

1. Um ein bestimmtes Segment anzusprechen, klicken Sie auf den Link Mehr **…** , um zusätzliche Optionen anzuzeigen. Klicken Sie dann auf das Symbol _Auswahl_ (![Listensymbol](../assets/icon-list-chooser.png)), um die Liste der Kundensegmente anzuzeigen.

1. Aktivieren Sie in der Liste das Kontrollkästchen jedes Segments, das Sie mit der Bedingung ansprechen möchten.

   ![Warenkorb-Preisregel - Bedingungsauswahlliste](assets/condition-segment-chooser-list.png){width="600" zoomable="yes"}

1. Klicken Sie auf **[!UICONTROL Select]** , um die ausgewählten Kundensegmente in der Bedingung zu platzieren.

1. Vervollständigen Sie den Rest der Preisregel nach Bedarf.

1. Klicken Sie abschließend auf **[!UICONTROL Save]**.
