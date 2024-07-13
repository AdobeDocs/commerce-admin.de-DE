---
title: Hinzufügen der Suche nach Geschenkregistern
description: Erfahren Sie, wie Sie ein Suchfeld für Geschenkregistrierung platzieren, um Besucher beim Kauf von Produkten aus Kundenregistern zu unterstützen.
exl-id: 8c5558d6-3641-4769-987e-8b217603d9fc
feature: Gift, Storefront, Search
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '436'
ht-degree: 0%

---

# Hinzufügen der Suche nach Geschenkregistern

{{ee-feature}}

Mit dem Tool [Widget](../content-design/widgets.md) können Sie eine Suche in der Geschenkregistrierung an beliebiger Stelle in Ihrem Geschäft platzieren. Sie können die Suchoptionen festlegen, die Kunden zur Verfügung stehen sollen, z. B. Name, E-Mail-Adresse und Geschenkregisterkennung. Wenn der Kunde auf die Suchschaltfläche klickt, werden die Ergebnisse auf der Seite &quot;Suche in der Gift Registry&quot;angezeigt. Wenn bei der Suche keine Ergebnisse zurückgegeben werden, kann der Kunde es mit anderen Parametern erneut versuchen.

![Beispiel-Storefront - Suche nach Geschenkregistrierung](./assets/storefront-gift-registry-search.png){width="700" zoomable="yes"}

## Suche nach Geschenkgutregistern konfigurieren

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**.

1. Klicken Sie in der oberen rechten Ecke auf **[!UICONTROL Add Widget]**.

1. Wählen Sie die Registerkarte **[!UICONTROL Settings]** aus und führen Sie die folgenden Schritte aus:

   - Setzen Sie **[!UICONTROL Type]** auf `Gift Registry Search`.

   - Setzen Sie **[!UICONTROL Design Theme]** auf das Design, das vom Store verwendet wird.

   - Klicken Sie auf **[!UICONTROL Continue]**.

   ![Gift registry - search settings](./assets/widget-gift-registry-search-settings.png){width="700" zoomable="yes"}

1. Gehen Sie im Abschnitt _[!UICONTROL Storefront Properties]_wie folgt vor:

   - Geben Sie einen &quot;**[!UICONTROL Widget Title]**&quot;-Wert für die interne Referenz ein.

   - Setzen Sie **[!UICONTROL Assign to Store Views]** auf die Store-Ansichten, in denen die Geschenkregistersuche verfügbar sein soll.

   - Legen Sie **[!UICONTROL Sort Order]** fest, um die Reihenfolge zu bestimmen, in der der Suchblock &quot;Gift Registry&quot;angezeigt wird, wenn dem gleichen Ort auf der Seite andere Blöcke zugewiesen sind.

   ![Geschenkregistrierung - Storefront-Eigenschaften](./assets/widget-gift-registry-search-storefront-properties.png){width="700" zoomable="yes"}

1. Klicken Sie im Abschnitt **[!UICONTROL Layout Updates]** auf **[!UICONTROL Add Layout Update]**.

1. Gehen Sie wie folgt vor, um zu ermitteln, wo die Suche in der Gift Registry im Store angezeigt wird:

   - Setzen Sie **[!UICONTROL Display On]** auf die Seiten in Ihrem Geschäft, auf denen der Suchblock der Geschenkregistrierung angezeigt werden soll.

   - Wählen Sie ggf. die **[!UICONTROL Categories]** aus, wo sie angezeigt werden soll.

   - Setzen Sie &quot;**[!UICONTROL Container]**&quot;auf die Position auf der Seite, um den Suchblock &quot;Gift Registry&quot;zu platzieren.

   ![Gift registry - layout updates](./assets/widget-gift-registry-search-layout-updates.png){width="500" zoomable="yes"}

1. Wählen Sie im linken Bereich **[!UICONTROL Widget Options]** aus.

1. Um festzustellen, wie Besucher Ihrer Site nach Geschenkregistern suchen können, wählen Sie so viele der folgenden Punkte aus:

   - [!UICONTROL All Forms]
   - [!UICONTROL Registrant Name Search]
   - [!UICONTROL Registrant Email Search]
   - [!UICONTROL Gift Registry ID Search]

   ![Gift-Registrierung - Widget-Optionen](./assets/widget-gift-registry-search-widget-options.png){width="700" zoomable="yes"}

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save]**.

1. Wenn Sie aufgefordert werden, den Seiten-Cache zu aktualisieren, klicken Sie auf den Link in der Meldung oben im Arbeitsbereich und befolgen Sie die Anweisungen.

## Feldbeschreibungen

### [!UICONTROL Settings]

| Feld | Beschreibung |
|--- |--- |
| [!UICONTROL Type] | Identifiziert `Gift Registry Search` als Typ des Widgets. |
| [!UICONTROL Design Theme] | Das Design, das vom Store verwendet wird, in dem die Suche in der Gift Registry angezeigt werden soll. |

{style="table-layout:auto"}

### [!UICONTROL Storefront Properties]

| Feld | Beschreibung |
|--- |--- |
| [!UICONTROL Widget Title] | Ein Name für eine interne Referenz. |
| [!UICONTROL Assign to Store Views] | Identifiziert die Store-Ansichten, in denen die Suche in der Gift Registry verfügbar sein soll. |
| [!UICONTROL Sort Order] | Gibt die Reihenfolge an, in der der Suchblock der Geschenkregistrierung angezeigt wird, wenn andere Blöcke am selben Ort zugewiesen sind. |

{style="table-layout:auto"}

### [!UICONTROL Layout Updates]

| Feld | Beschreibung |
|--- |--- |
| [!UICONTROL Display On] | Geben Sie die spezifischen Seiten oder Seitentypen an, auf denen der Suchblock für die Geschenkregistrierung angezeigt wird. |
| [!UICONTROL Categories] | Gibt ggf. die Kategorieseiten an, auf denen die Suche in der Gift Registry angezeigt wird. |
| [!UICONTROL Container] | Gibt den Seitenlayoutblock an, in dem die Gift Registry-Suche platziert wird. Die Optionen variieren je nach Vorlage und Thema. |

{style="table-layout:auto"}

### [!UICONTROL Widget Options]

| Feld | Beschreibung |
|--- |--- |
| [!UICONTROL Quick Search Form Types] | Bestimmt die Arten von Suchvorgängen, die mit der Suche in der Git Registry durchgeführt werden können. Optionen: `All Forms` / `Registrant Name Search` /` Registrant Email Search` / `Gift Registry ID Search` |

{style="table-layout:auto"}
