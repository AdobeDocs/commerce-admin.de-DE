---
title: Inventarquellen für ein Lager priorisieren
description: Erfahren Sie, wie Sie die Quellen vorrangig von oben nach unten anordnen können, die bei der Bestimmung von Versand- und Lagerabzügen verwendet werden.
exl-id: 16db3ee3-ce99-40dd-b1a3-fcb145b1298f
feature: Inventory, Configuration
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '210'
ht-degree: 0%

---

# Priorisieren von Quellen für ein Lager

Nach dem Hinzufügen [sources](sources-manage.md) der [stock](stocks-manage.md), ordnen Sie diese Quellen prioritär von oben nach unten an, um Bestellungen zu erfüllen. Der Quellauswahlalgorithmus (SSA) bietet eine Algorithmuspriorität, die diese Reihenfolge bei der Bestimmung von Versand- und Bestandsabzügen verwendet.

Die Quellpriorität für Lager hat keinen Einfluss auf zugewiesene Quellen bei der Bearbeitung von Produktbeständen.

In diesem Beispiel wurden der britischen Börse für ein Geschäft und zwei Lagerhäuser in London und für ein Lager in Berlin Quellen zugewiesen, die nicht bestellt wurden.

![Quellreihenfolge vor Priorisierung](assets/inventory-priority-before.png){width="350" zoomable="yes"}

Der Händler zieht es vor, die Sendungen aus dem größeren Lagerhaus in Berlin, dann dem Lagerhaus in London, dem Überlaufort in London und schließlich der Storefront in London priorisieren zu lassen. Um die Reihenfolge zu ändern, werden Einträge in die gewünschte Reihenfolge gezogen und abgelegt.

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Inventory]_>**[!UICONTROL Stocks]**.

1. Öffnen Sie das Lager im _Bearbeiten_ -Modus.

1. Erweitern Sie die _[!UICONTROL Sources]_bei Bedarf.

1. Verwendung ![Symbol &quot;Sortieren&quot;](assets/icon-sort.png) , um die Quellen per Drag-and-Drop von oben (erste) nach unten (letzte) in eine Priorität zu ziehen.

   Diese Bestellung ist bei Versandbestellungen wichtig. SSA empfiehlt Verbringungen auf der Grundlage der Reihenfolge der Quellen

1. Klicks **[!UICONTROL Save & Continue]** , um die Änderungen zu speichern.

![Quellreihenfolge nach Priorisierung](assets/inventory-stock-priority-after.png){width="350" zoomable="yes"}
