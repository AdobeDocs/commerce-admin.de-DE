---
title: Sortierreihenfolge für Checkout-Summen
description: Erfahren Sie mehr über die angezeigte Checkout-Gesamtsumme und wie Sie die Sortierreihenfolge der Checkout-Summen in der Bestellübersicht konfigurieren.
exl-id: 2b1345e3-6ad3-472a-af3e-3f7b24577b13
feature: Checkout, Configuration
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '257'
ht-degree: 0%

---

# Sortierreihenfolge für Checkout-Summen

Während der Überprüfung der Bestellung erscheint der Gesamtbetrag unten in der Bestellung, mit allen Anpassungen für Rabatte, Versandkosten, Gutschriften aus dem Geschäft und Steuern. Die Reihenfolge jedes Elements bestimmt die Reihenfolge der Berechnungen und wird in der Konfiguration durch eine Zahl festgelegt, die jedem Element zugewiesen wird. Beispielsweise ist die Zwischensumme das erste Element im Abschnitt und erhält den Wert 10. Die Gesamtsumme wird als letzter angezeigt und erhält den Wert 100. Allen anderen Elementen im Abschnitt &quot;Summen&quot;wird ein Wert zwischen diesen Werten zugewiesen.

![Bestellzusammenfassung zeigt die Checkout-Gesamtsumme an](./assets/storefront-checkout-totals.png){width="700" zoomable="yes"}

**_So konfigurieren Sie die Sortierreihenfolge der Checkout-Summen:_**

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich den Abschnitt **[!UICONTROL Sales]** und wählen Sie unter &quot;**[!UICONTROL Sales]**&quot;.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) im Abschnitt **[!UICONTROL Checkout Totals Sort Order]** .

   ![Checkout-Gesamtzahlen, nummeriert, um die Sortierreihenfolge zu bestimmen](../configuration-reference/sales/assets/sales-checkout-totals-sort-order.png){width="600" zoomable="yes"}

   Eine ausführliche Beschreibung der einzelnen Konfigurationseinstellungen finden Sie unter [Sortierreihenfolge insgesamt auschecken](../configuration-reference/sales/sales.md#checkout-totals-sort-order) im _Konfigurationshandbuch_.

1. Wenn die Einstellung für eine bestimmte Store-Ansicht gilt, wählen Sie [die Store-Ansicht](../configuration-reference/scope-change.md#set-the-scope), in der die Konfiguration gilt.

   Klicken Sie nach Aufforderung auf **[!UICONTROL OK]** , um fortzufahren.

1. Um die Reihenfolge im Abschnitt _Gesamt_ zu bestimmen, ändern Sie die jedem Element zugewiesene Zahl.

   Je niedriger der Wert ist, desto früher wird er in die Liste eingefügt. In der Standardkonfiguration ist die Zwischensumme (`10`) die erste und die Gesamtsumme (`100`) die letzte.

   Deaktivieren Sie bei Bedarf das Kontrollkästchen **[!UICONTROL Use system value]** , um diese Änderungen durchzuführen.

1. Klicken Sie auf **[!UICONTROL Save Config]**.
