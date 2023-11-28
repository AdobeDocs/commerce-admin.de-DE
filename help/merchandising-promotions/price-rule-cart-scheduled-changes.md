---
title: Geplante Änderungen für Warenkorbpreisregeln
description: Erfahren Sie, wie Sie im Rahmen einer Kampagne Regeln für den Warenkorbpreis anwenden und diese mit anderen Inhaltsänderungen gruppieren können.
exl-id: 4c9caa04-1e11-440d-b3db-7cc5fc83a08f
feature: Merchandising, Price Rules, Shopping Cart
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '394'
ht-degree: 0%

---

# Geplante Änderungen für Warenkorbpreisregeln

{{ee-feature}}

Preisregeln für Warenkorb können planmäßig im Rahmen einer Kampagne angewendet und mit anderen Inhaltsänderungen gruppiert werden. Sie können eine Kampagne auf der Grundlage geplanter Änderungen an einer Preisregel erstellen oder die Änderungen auf eine bestehende Kampagne anwenden.

![Preisregeln für Warenkorb - geplante Änderungen](./assets/content-staging-price-rules-cart-scheduled-changes.png){width="700" zoomable="yes"}

>[!NOTE]
>
>Alle geplanten Aktualisierungen werden nacheinander angewendet. Das bedeutet, dass jeder Entität nur eine geplante Aktualisierung zu einem bestimmten Zeitpunkt zugewiesen werden kann. Jede geplante Aktualisierung wird auf alle Store-Ansichten innerhalb des Zeitrahmens angewendet. Daher kann eine Entität nicht mehrere geplante Aktualisierungen für verschiedene Store-Ansichten gleichzeitig aufweisen. Alle Entitätsattributwerte in allen Store-Ansichten, die von der aktuellen geplanten Aktualisierung nicht betroffen sind, werden von den Standardwerten übernommen und nicht von der vorherigen geplanten Aktualisierung.

Wenn in derselben Kampagne mehrere Preisregeln ausgeführt werden, wird die Variable _[!UICONTROL Priority]_bestimmt, welche Regel Vorrang hat. Weitere Informationen finden Sie unter [Inhaltstaging](../content-design/content-staging.md).

Beachten Sie die folgenden Einschränkungen:

- Wenn eine Kampagne, die eine Preisregel enthält, zunächst ohne Enddatum erstellt wird, kann die Kampagne später nicht mehr so bearbeitet werden, dass sie ein Enddatum enthält. Es wird empfohlen, entweder beim Erstellen der Kampagne ein Enddatum hinzuzufügen oder eine duplizierte Version der vorhandenen Kampagne zu erstellen und das Enddatum nach Bedarf dem Duplikat hinzuzufügen.
- Wenn Sie eine geplante Aktualisierung verwenden, um eine Regel zum Warenkorbpreis mit einem Enddatum zu aktivieren, stellen Sie sicher, dass Sie die Regel so einstellen, dass sie ursprünglich deaktiviert war. Regeln, die bereits aktiv sind, respektieren nicht das Enddatum.
- Coupons sind nicht an die Preisregeln für den Warenkorb gebunden. Eine geplante Aktualisierung bietet keinen Zugriff auf die _[!UICONTROL Coupon]_,_[!UICONTROL Coupon Code]_, _[!UICONTROL Uses per Coupon]_, und_[!UICONTROL Uses per Customer]_ -Felder auf _[!UICONTROL Rule Information]_Registerkarte. Außerdem werden alle Einstellungen aus dem_[!UICONTROL Manage Coupon Codes]_ nicht verfügbar sind.

>[!IMPORTANT]
>
>Kampagne **[!UICONTROL Start Date]** und **[!UICONTROL End Date]** muss mithilfe der **_default_** Admin-Zeitzone, die aus der lokalen Zeitzone jeder Website konvertiert wird. Betrachten wir ein Beispiel, bei dem Sie mehrere Websites in verschiedenen Zeitzonen haben, aber die Kampagne auf der Grundlage einer US-Zeitzone starten möchten. In diesem Fall müssen Sie für jede lokale Zeitzone eine separate Aktualisierung planen und **[!UICONTROL Start Date]** und **[!UICONTROL End Date]** wird aus jeder lokalen Website-Zeitzone in die standardmäßige Admin-Zeitzone konvertiert.
