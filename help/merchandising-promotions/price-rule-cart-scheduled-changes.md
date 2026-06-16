---
title: Geplante Änderungen für Warenkorbpreisregeln
description: Erfahren Sie, wie Sie die Regeln für den Warenkorbpreis im Rahmen einer Kampagne planmäßig anwenden und mit anderen Inhaltsänderungen gruppieren.
exl-id: 4c9caa04-1e11-440d-b3db-7cc5fc83a08f
feature: Merchandising, Price Rules, Shopping Cart
TQID: https://experienceleague.adobe.com/S4sSXY-SSMabdW-rkaqr-cMexe0q1-k6AbTNvb7pR14
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: b5520579-b31f-4df7-9281-f0d9f91e2edc
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 489
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
