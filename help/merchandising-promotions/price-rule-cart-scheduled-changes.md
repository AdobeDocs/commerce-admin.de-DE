---
title: Geplante Änderungen für Warenkorbpreisregeln
description: Erfahren Sie, wie Sie die Regeln für den Warenkorbpreis im Rahmen einer Kampagne planmäßig anwenden und mit anderen Inhaltsänderungen gruppieren.
exl-id: 4c9caa04-1e11-440d-b3db-7cc5fc83a08f
feature: Merchandising, Price Rules, Shopping Cart
source-git-commit: 0ceb61e6f1629a3bef16c550362c1db25b4aefa5
workflow-type: tm+mt
source-wordcount: '489'
ht-degree: 0%

---

# Geplante Änderungen für Warenkorbpreisregeln

{{ee-feature}}

Die Regeln für den Warenkorbpreis können im Rahmen einer Kampagne planmäßig angewendet und mit anderen Inhaltsänderungen gruppiert werden. Sie können eine Kampagne auf der Grundlage geplanter Änderungen an einer Preisregel erstellen oder die Änderungen auf eine vorhandene Kampagne anwenden.

>[!NOTE]
>
>Die Felder [!UICONTROL From] und [!UICONTROL To] wurden in ![Adobe Commerce](../assets/adobe-logo.svg) Adobe Commerce entfernt und können nicht direkt über die Warenkorb-Preisregel geändert werden. Für diese Aktivierungen muss ein geplantes Update erstellt werden.

![Warenkorbpreisregeln - Geplante Änderungen](./assets/content-staging-price-rules-cart-scheduled-changes.png){width="700" zoomable="yes"}

>[!NOTE]
>
>Alle geplanten Aktualisierungen werden nacheinander angewendet. Das bedeutet, dass jede Entität zu einem bestimmten Zeitpunkt nur eine geplante Aktualisierung haben kann. Jede geplante Aktualisierung wird auf alle Store-Ansichten innerhalb ihres Zeitrahmens angewendet. Daher kann eine Entität nicht gleichzeitig verschiedene geplante Aktualisierungen für verschiedene Store-Ansichten haben. Alle Entitätsattributwerte in allen Store-Ansichten, die nicht von der aktuellen geplanten Aktualisierung betroffen sind, werden aus den Standardwerten übernommen, nicht aus der vorherigen geplanten Aktualisierung.

Wenn in derselben Kampagne mehrere Preisregeln ausgeführt werden, bestimmt die _[!UICONTROL Priority]_&#x200B;der Preisregel, welche Regel Vorrang hat. Weitere Informationen finden Sie unter [Inhaltsbereitstellung](../content-design/content-staging.md).

>[!NOTE]
>
>Wenn eine aktive Kampagne anfänglich ohne Enddatum erstellt wird, kann die Kampagne nicht später bearbeitet werden, um ein Enddatum einzuschließen. In diesem Fall müssen Sie eine doppelte Kampagne erstellen und das erforderliche Enddatum eingeben.

>[!NOTE]
>
>Wenn eine Kampagne mit mehr als einer Warenkorb-Preisregel verknüpft ist, kann die Kampagne nur über das [Inhalts-Staging-Dashboard“ bearbeitet &#x200B;](../content-design/content-staging-dashboard.md).

Beachten Sie die folgenden Einschränkungen:

- Wenn eine Kampagne mit einer Preisregel anfänglich ohne Enddatum erstellt wird, kann die Kampagne später nicht mehr so bearbeitet werden, dass sie ein Enddatum enthält. Es wird empfohlen, entweder beim Erstellen der Kampagne ein Enddatum hinzuzufügen oder eine doppelte Version der vorhandenen Kampagne zu erstellen und das Enddatum dem Duplikat nach Bedarf hinzuzufügen.
- Wenn Sie eine geplante Aktualisierung verwenden, um eine Warenkorb-Preisregel mit einem Enddatum zu aktivieren, stellen Sie sicher, dass Sie die Regel zunächst als deaktiviert festlegen. Bereits aktive Regeln berücksichtigen nicht das Enddatum.
- Coupons sind nicht mit Warenkorb-Preisregeln verbunden. Eine geplante Aktualisierung bietet keinen Zugriff auf die Felder _[!UICONTROL Coupon]_,_[!UICONTROL Coupon Code]_, _[!UICONTROL Uses per Coupon]_&#x200B;und&#x200B;_[!UICONTROL Uses per Customer]_ auf der Registerkarte _[!UICONTROL Rule Information]_. Außerdem sind nicht alle Einstellungen auf der Registerkarte&#x200B;_[!UICONTROL Manage Coupon Codes]_ verfügbar.

>[!IMPORTANT]
>
>**[!UICONTROL Start Date]** und **[!UICONTROL End Date]** für Kampagnen müssen mithilfe der **_Standard_**-Admin-Zeitzone definiert werden, die aus der lokalen Zeitzone jeder Website konvertiert wird. Angenommen, Sie haben mehrere Websites in verschiedenen Zeitzonen, möchten Ihre Kampagne jedoch basierend auf einer US-Zeitzone starten. In diesem Fall müssen Sie für jede lokale Zeitzone eine separate Aktualisierung planen und **[!UICONTROL Start Date]** und **[!UICONTROL End Date]** von jeder lokalen Website-Zeitzone in die standardmäßige Admin-Zeitzone konvertieren festlegen.
