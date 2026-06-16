---
title: Sortierreihenfolge für Checkout-Summen
description: Erfahren Sie mehr über die angezeigte Kaufsumme und wie Sie die Sortierreihenfolge der Kaufsummen in der Bestellübersicht konfigurieren.
exl-id: 2b1345e3-6ad3-472a-af3e-3f7b24577b13
feature: Checkout, Configuration
TQID: https://experienceleague.adobe.com/cXt3dbS5Jd8baKFk8K8HP1Cypk1oMS85iCq-WZ8cIgg
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
source-wordcount: 257
ht-degree: 0%

---

# Sortierreihenfolge für Checkout-Summen

Bei der Bestellüberprüfung wird der Gesamtbetrag am unteren Rand der Bestellung angezeigt, einschließlich aller Berichtigungen für Rabatte, Versandkosten, Warenkorbgutschriften und Steuern. Die Reihenfolge der einzelnen Elemente bestimmt die Reihenfolge der Berechnungen und wird in der Konfiguration durch eine Zahl festgelegt, die jedem Element zugewiesen ist. Beispielsweise ist die Zwischensumme der erste Artikel im Abschnitt und erhält den Wert 10. Der Gesamtwert wird als letzter angezeigt und erhält den Wert 100. Allen anderen Elementen im Abschnitt „Gesamtwerte“ wird ein Wert zwischen diesen Werten zugewiesen.

![Bestellzusammenfassung zeigt die Checkout-Summe an](./assets/storefront-checkout-totals.png){width="700" zoomable="yes"}

**_So konfigurieren Sie die Sortierreihenfolge der Checkout-Gesamtwerte:_**

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich den Abschnitt **[!UICONTROL Sales]** und wählen Sie darunter **[!UICONTROL Sales]**.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Checkout Totals Sort Order]** .

   ![Die Gesamtzahl der Checkout-Optionen ist nummeriert, um die Sortierreihenfolge zu bestimmen](../configuration-reference/sales/assets/sales-checkout-totals-sort-order.png){width="600" zoomable="yes"}

   Eine ausführliche Beschreibung jeder dieser Konfigurationseinstellungen finden Sie unter [Sortierreihenfolge für Checkout-Summen](../configuration-reference/sales/sales.md#checkout-totals-sort-order) im _Konfigurationshandbuch_.

1. Wenn die Einstellung für eine bestimmte Store-Ansicht ist, wählen [die Store-Ansicht aus](../configuration-reference/scope-change.md#set-the-scope) für die die Konfiguration gilt.

   Wenn Sie dazu aufgefordert werden, klicken Sie auf **[!UICONTROL OK]** , um fortzufahren.

1. Um die Reihenfolge im Abschnitt _Summen_ zu bestimmen, ändern Sie die jedem Artikel zugewiesene Zahl.

   Je niedriger der Wert, desto früher ist seine Platzierung in der Liste. In der Standardkonfiguration ist die Zwischensumme (`10`) die erste und die Gesamtsumme (`100`) die letzte.

   Deaktivieren Sie bei Bedarf das Kontrollkästchen **[!UICONTROL Use system value]** , um diese Änderungen abzuschließen.

1. Klicken Sie auf **[!UICONTROL Save Config]**.
