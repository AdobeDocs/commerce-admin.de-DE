---
title: Geplante Änderungen für Warenkorbpreisregeln
description: Erfahren Sie, wie Sie im Rahmen einer Kampagne Regeln für den Warenkorbpreis anwenden und diese mit anderen Inhaltsänderungen gruppieren können.
exl-id: 4c9caa04-1e11-440d-b3db-7cc5fc83a08f
feature: Merchandising, Price Rules, Shopping Cart
source-git-commit: 74cc26e74c3efabc914c27b6d8327a85a77fd6e6
workflow-type: tm+mt
source-wordcount: '447'
ht-degree: 0%

---

# Geplante Änderungen für Warenkorbpreisregeln

{{ee-feature}}

Preisregeln für Warenkorb können planmäßig im Rahmen einer Kampagne angewendet und mit anderen Inhaltsänderungen gruppiert werden. Sie können eine Kampagne auf der Grundlage geplanter Änderungen an einer Preisregel erstellen oder die Änderungen auf eine bestehende Kampagne anwenden.

>[!NOTE]
>
>Die Felder [!UICONTROL From] und [!UICONTROL To] wurden in der Adobe Commerce ![Adobe Commerce](../assets/adobe-logo.svg) entfernt und können nicht direkt in der Preisregel des Warenkorbs geändert werden. Sie müssen eine geplante Aktualisierung für diese Aktivierungen erstellen.

![Preisregeln für Warenkorb - geplante Änderungen](./assets/content-staging-price-rules-cart-scheduled-changes.png){width="700" zoomable="yes"}

>[!NOTE]
>
>Alle geplanten Aktualisierungen werden nacheinander angewendet. Das bedeutet, dass jeder Entität nur eine geplante Aktualisierung zu einem bestimmten Zeitpunkt zugewiesen werden kann. Jede geplante Aktualisierung wird auf alle Store-Ansichten innerhalb des Zeitrahmens angewendet. Daher kann eine Entität nicht mehrere geplante Aktualisierungen für verschiedene Store-Ansichten gleichzeitig aufweisen. Alle Entitätsattributwerte in allen Store-Ansichten, die von der aktuellen geplanten Aktualisierung nicht betroffen sind, werden von den Standardwerten übernommen und nicht von der vorherigen geplanten Aktualisierung.

Wenn in derselben Kampagne mehrere Preisregeln ausgeführt werden, bestimmt die Einstellung _[!UICONTROL Priority]_der Preisregel, welche Regel Vorrang hat. Weitere Informationen finden Sie unter [Inhaltstaging](../content-design/content-staging.md).

>[!NOTE]
>
>Wenn eine Kampagne mit mehreren Preisregeln für den Warenkorb verknüpft ist, kann die Kampagne nur über das Dashboard [Inhaltstaging-Dashboard](../content-design/content-staging-dashboard.md) bearbeitet werden.

Beachten Sie die folgenden Einschränkungen:

- Wenn eine Kampagne, die eine Preisregel enthält, zunächst ohne Enddatum erstellt wird, kann die Kampagne später nicht mehr so bearbeitet werden, dass sie ein Enddatum enthält. Es wird empfohlen, entweder beim Erstellen der Kampagne ein Enddatum hinzuzufügen oder eine duplizierte Version der vorhandenen Kampagne zu erstellen und das Enddatum nach Bedarf dem Duplikat hinzuzufügen.
- Wenn Sie eine geplante Aktualisierung verwenden, um eine Regel zum Warenkorbpreis mit einem Enddatum zu aktivieren, stellen Sie sicher, dass Sie die Regel so einstellen, dass sie ursprünglich deaktiviert war. Regeln, die bereits aktiv sind, respektieren nicht das Enddatum.
- Coupons sind nicht an die Preisregeln für den Warenkorb gebunden. Eine geplante Aktualisierung bietet keinen Zugriff auf die Felder _[!UICONTROL Coupon]_,_[!UICONTROL Coupon Code]_, _[!UICONTROL Uses per Coupon]_und_[!UICONTROL Uses per Customer]_ auf der Registerkarte _[!UICONTROL Rule Information]_. Außerdem sind nicht alle Einstellungen auf der Registerkarte_[!UICONTROL Manage Coupon Codes]_ verfügbar.

>[!IMPORTANT]
>
>Campaign **[!UICONTROL Start Date]** und **[!UICONTROL End Date]** müssen mithilfe der **_default_** Admin-Zeitzone definiert werden, die aus der lokalen Zeitzone jeder Website konvertiert wird. Betrachten wir ein Beispiel, bei dem Sie mehrere Websites in verschiedenen Zeitzonen haben, aber die Kampagne auf der Grundlage einer US-Zeitzone starten möchten. In diesem Fall müssen Sie für jede lokale Zeitzone eine separate Aktualisierung planen und **[!UICONTROL Start Date]** und **[!UICONTROL End Date]**, die aus jeder lokalen Website-Zeitzone konvertiert wurden, auf die standardmäßige Zeitzone &quot;Admin&quot;setzen.
