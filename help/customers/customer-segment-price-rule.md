---
title: Kundensegmente in Preisregeln
description: Erfahren Sie, wie Sie Kundensegmente mit einer Preisregel für den Warenkorb verknüpfen, damit Sie gezielte Promotions für Ihren Store definieren können.
exl-id: eaa04e7a-c0f9-4f09-8e65-75965ccbdc69
feature: Customers, Configuration, Price Rules
source-git-commit: 7de285d4cd1e25ec890f1efff9ea7bdf2f0a9144
workflow-type: tm+mt
source-wordcount: '231'
ht-degree: 0%

---

# Kundensegmente in Preisregeln

{{ee-feature}}

Ein Kundensegment kann für zielgerichtete Promotions verwendet werden, indem es mit einer [Warenkorbpreisregel](../merchandising-promotions/price-rules-cart.md) verknüpft wird.

![Warenkorbpreisregel - zielgerichtetes Kundensegment](assets/price-rule-cart-condition-segments.png){width="700" zoomable="yes"}

_**So verknüpfen Sie ein Segment mit einer Warenkorbpreisregel:**_

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Marketing]** > _Promotions_ > **[!UICONTROL Cart Price Rules]**.

1. Öffnen Sie eine neue oder vorhandene Regel:

   * Um eine neue Regel zu verwenden, klicken Sie oben rechts auf **[!UICONTROL Add New Rule]** .
   * Um eine vorhandene Regel zu verwenden, klicken Sie in der Liste auf die Regel, um sie im Bearbeitungsmodus zu öffnen.

1. Scrollen Sie nach unten und erweitern Sie den Abschnitt **[!UICONTROL Conditions]** .

1. Fügen Sie die Bedingung hinzu.

   * Klicken Sie auf das Symbol _Hinzufügen_ (![Listensymbol](../assets/icon-add-green-circle.png)), das die Liste der Bedingungen anzeigt. Wählen Sie dann **[!UICONTROL Customer Segment]** aus.

   ![Preisregel für Warenkorb - Bedingung für Kundensegment hinzufügen](assets/condition-customer-segment.png){width="600" zoomable="yes"}

   Standardmäßig ist die Bedingung so eingestellt, dass eine passende Bedingung gefunden wird. Klicken Sie bei Bedarf auf den Link **[!UICONTROL matches]** und ändern Sie den Operator in einen der folgenden Werte:

   * `does not match`
   * `is one of`
   * `is not one of`

   ![Bedingungsoperator](assets/price-rule-condition-customer-segment-operator.png){width="600" zoomable="yes"}

1. Um ein bestimmtes Segment als Ziel festzulegen, klicken Sie auf den Link Mehr **...** , um weitere Optionen anzuzeigen. Klicken Sie dann auf das Symbol _Auswahl_ (![Listensymbol](../assets/icon-list-chooser.png)), um die Liste der Kundensegmente anzuzeigen.

1. Aktivieren Sie in der Liste das Kontrollkästchen jedes Segments, das Sie mit der Bedingung als Ziel auswählen möchten.

   ![Preisregel für Warenkorb - Liste der Bedingungsauswahl](assets/condition-segment-chooser-list.png){width="600" zoomable="yes"}

1. Klicken Sie auf **[!UICONTROL Select]** , um die ausgewählten Kundensegmente in die Bedingung einzufügen.

1. Nehmen Sie den Rest der Preisregel nach Bedarf vor.

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save]**.
