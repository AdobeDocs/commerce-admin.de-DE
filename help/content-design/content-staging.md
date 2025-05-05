---
title: Inhalts-Staging
description: Mit der Inhalts-Staging-Funktion kann Ihr Business-Team eine breite Palette von Inhaltsaktualisierungen für Ihren Store einfach erstellen, in der Vorschau anzeigen und direkt vom Administrator planen.
exl-id: 929cd020-cbc7-40bf-a22c-02df35212ecf
feature: Page Content, Staging
badgePaas: label="Nur PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Gilt nur für Adobe Commerce in Cloud-Projekten (von Adobe verwaltete PaaS-Infrastruktur) und lokale Projekte."
source-git-commit: 07d7ca7e7f6af42fe8e06dc3c49c2df5f50d1425
workflow-type: tm+mt
source-wordcount: '946'
ht-degree: 0%

---

# Inhalts-Staging

{{ee-feature}}

Mit der Inhalts-Staging-Funktion kann Ihr Business-Team eine breite Palette von Inhaltsaktualisierungen für Ihren Store einfach erstellen, in der Vorschau anzeigen und direkt von der _aus_. Anstatt beispielsweise in Form einer statischen Seite zu denken, stellen Sie eine Seite als eine Sammlung verschiedener Elemente dar, die je nach Zeitplan _-_ _-_ können. Sie können die Inhalts-Staging-Umgebung verwenden, um eine Seite zu erstellen, die sich automatisch über das Jahr nach einem Zeitplan ändert.

Der Begriff _Kampagne_ bezieht sich auf den Datensatz einer geplanten Änderung oder eine Sammlung von Änderungen, die über das Staging-Dashboard verwaltet werden. Die Änderungen können in einem Kalender oder einer Timeline angezeigt werden. Die Begriffe _Geplante Änderung_ und _Geplante Aktualisierung_ sind austauschbar und beziehen sich auf eine einzelne Änderung.

Wenn Sie eine Inhaltsänderung für einen bestimmten Zeitraum planen, wird der Inhalt nach Ablauf der geplanten Änderung auf die vorherige Version zurückgesetzt. Sie können mehrere Versionen desselben grundlegenden Inhalts erstellen, der für zukünftige Aktualisierungen verwendet werden soll. Sie können auch einen Schritt zurück durch die Zeitleiste gehen, um frühere Versionen des Inhalts anzuzeigen. Um eine Entwurfsversion zu speichern, weisen Sie einfach ein Datum auf der Timeline zu, das so weit in der Zukunft liegt, dass es nie in die Produktion übernommen wird.

## Staging-Objekte und -Kampagnen von Inhalten

Felder, die sich auf das Start- und Enddatum beziehen, wurden aus Adobe Commerce entfernt und können nicht direkt auf der Seite „Warenkorb-Preisregel“, „Katalogpreisregel“, „Produkt“, „Kategorie“ und &quot;CMS&quot; geändert werden. Für diese Aktivierungen muss ein geplantes Update erstellt werden.

Alle geplanten Aktualisierungen werden nacheinander angewendet, d. h., jede Entität kann nur jeweils eine geplante Aktualisierung haben. Jede geplante Aktualisierung wird auf alle Store-Ansichten innerhalb ihres Zeitrahmens angewendet. Daher kann eine Entität nicht gleichzeitig verschiedene geplante Aktualisierungen für verschiedene Store-Ansichten haben. Alle Entitätsattributwerte in allen Store-Ansichten, die nicht von der aktuellen geplanten Aktualisierung betroffen sind, werden aus den Standardwerten übernommen, nicht aus der vorherigen geplanten Aktualisierung.

Wenn ein neues geplantes Update für eines der folgenden Objekte erstellt wird, wird eine entsprechende Kampagne als Platzhalter erstellt, und das _[!UICONTROL Scheduled Changes]_&#x200B;wird am oberen Rand der Seite angezeigt. Die Platzhalterkampagne hat ein Startdatum, aber kein Enddatum. Sie können Aktualisierungen des Inhalts als Teil einer Kampagne planen und dann eine Vorschau anzeigen und die Änderungen nach Datum, Uhrzeit oder Store-Ansicht freigeben. Nachdem Sie eine neue Kampagne für ein Objekt erstellt haben, können Sie sie anderen Objekten als geplante Aktualisierung zuweisen.

- [PRODUCT](../catalog/product-scheduled-changes.md)
- [Kategorien](../catalog/category-scheduled-changes.md)
- [Katalogpreisregeln](../merchandising-promotions/price-rule-catalog-scheduled-changes.md)
- [Warenkorb-Preisregeln](../merchandising-promotions/price-rule-cart-scheduled-changes.md)
- [CMS-Seiten](pages-workspace.md#scheduled-changes)
- [CMS-Blöcke](blocks.md)

## Staging-Workflow für Inhalte

1. **Erstellen des Grundlinieninhalts**

   Die Grundlinie ist der Inhalt eines Assets ohne Kampagne und umfasst alles, was sich unter dem Abschnitt _[!UICONTROL Scheduled Changes]_&#x200B;oben auf der Seite befindet. Der Baseline-Inhalt wird immer verwendet, es sei denn, es gibt eine aktive Kampagne mit Änderungen, die für diesen Ort in der Timeline geplant sind.

1. **Erstellen der ersten Kampagne**

   Erstellen Sie Ihre erste Kampagne mit dem Start- und Enddatum nach Bedarf. Damit die Kampagne unbegrenzt ist, lassen Sie das Enddatum leer. Wenn die erste Kampagne endet, wird der ursprüngliche Baseline-Inhalt wiederhergestellt.

   Das Start- und Enddatum einer Kampagne müssen mithilfe der Admin-Zeitzone **_Standard_** definiert werden, die aus der lokalen Zeitzone jeder Website konvertiert wird. Angenommen, Sie haben mehrere Websites in verschiedenen Zeitzonen, möchten aber eine Kampagne basierend auf einer US-Zeitzone starten. In diesem Fall müssen Sie für jede lokale Zeitzone eine separate Aktualisierung planen und **[!UICONTROL Start Date]** und **[!UICONTROL End Date]** in festlegen, die von jeder lokalen Website-Zeitzone in die standardmäßige Admin-Zeitzone konvertiert werden.

1. **Zweite Kampagne hinzufügen**

   Erstellen Sie die zweite Kampagne mit dem Start- und Enddatum nach Bedarf. Die zweite Kampagne kann einem völlig anderen Zeitraum zugeordnet werden. Beim Erstellen mehrerer Kampagnen für dasselbe Asset können sich die Kampagnen nicht überschneiden. Sie können so viele Kampagnen wie nötig erstellen.

   Einer bestehenden Kampagne, die noch nicht gestartet wurde, können mehrere Assets zugewiesen werden. Beispielsweise können zwei verschiedene Produktpreise im Umfang derselben Kampagne mit einem zukünftigen Startdatum aktualisiert werden.

   >[!NOTE]
   >
   >Wenn eine Kampagne mit mehr als einer Entität verknüpft ist, kann die Kampagne nur über das [Staging-Dashboard“ bearbeitet ](content-staging-dashboard.md).

1. **Baseline-Inhalt wiederherstellen**

   Wenn alle Kampagnen ein Enddatum haben, wird der Baseline-Inhalt jedes Mal wiederhergestellt, wenn alle aktiven Kampagnen enden.

   >[!NOTE]
   >
   >Wenn eine aktive Kampagne anfänglich ohne Enddatum erstellt wird, kann die Kampagne nicht später bearbeitet werden, um ein Enddatum einzuschließen. In diesem Fall müssen Sie eine doppelte Kampagne erstellen und das erforderliche Enddatum eingeben.

>[!NOTE]
>
>Während eine Staging-Aktualisierung für eine Entität aktiv ist, wird beim Bearbeiten der Entität die aktuelle aktive Staging-Aktualisierung bearbeitet. Dies wirkt sich nicht auf den Grundlinieninhalt aus, der wiederhergestellt wird, wenn die Staging-Aktualisierung beendet wird.

## [!UICONTROL Content Staging] Dashboard

Das [!UICONTROL Content Staging] [Dashboard](content-staging-dashboard.md) bietet Einblick in alle geplanten Änderungen und Aktualisierungen der Site. Jeder Tag, jeder Datumsbereich oder jeder Zeitraum einer Kampagne kann als Vorschau angezeigt und für andere freigegeben werden.

![Staging-Dashboard](./assets/content-staging-dashboard-grid.png){width="600" zoomable="yes"}

## Demo zur Inhalts-Staging

In diesem Video erfahren Sie mehr über Inhalts-Staging:

>[!VIDEO](https://video.tv.adobe.com/v/343784?quality=12&learn=on)

## Fehlerbehebung bei Ressourcen

Hilfe bei der Fehlerbehebung bei Problemen mit der Inhalts-Staging-Umgebung finden Sie in den folgenden Artikeln der [!DNL Commerce]-Support-Wissensdatenbank:

- [Fehler 404 auf allen Seiten aufgrund eines Problems mit der Inhalts-Staging-Umgebung](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/site-down-or-unresponsive/error-404-on-all-pages-due-to-content-staging-issue.html)
- [Geplante Staging-Aktualisierungen von Inhalten werden nicht mit veraltetem Fastly-Cache angezeigt](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/miscellaneous/scheduled-content-staging-updates-not-displayed-with-stale-fastly-cache.html)
- [Kann ich Aktualisierungen der Inhalts-Staging-Umgebung für Preise in einem freigegebenen Katalog planen?](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/faq/can-i-schedule-content-staging-updates-for-prices-in-a-shared-catalog.html)
