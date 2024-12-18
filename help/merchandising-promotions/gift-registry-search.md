---
title: Geschenkregistrierungssuche hinzufügen
description: Erfahren Sie, wie Sie ein Suchfeld für die Geschenkregistrierung platzieren, um Besucherinnen und Besucher beim Kauf von Produkten aus Kundenregistraturen zu unterstützen.
exl-id: 8c5558d6-3641-4769-987e-8b217603d9fc
feature: Gift, Storefront, Search
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '436'
ht-degree: 0%

---

# Geschenkregistrierungssuche hinzufügen

{{ee-feature}}

Das [Widget](../content-design/widgets.md)-Tool kann verwendet werden, um ein Geschenkregistrierungs-Suchfeld fast überall in Ihrem Geschäft zu platzieren. Sie können die Suchoptionen angeben, die Kundinnen und Kunden zur Verfügung stehen sollen, z. B. Name, E-Mail-Adresse und Geschenkregistrierungs-ID. Wenn der Kunde auf die Schaltfläche „Suchen“ klickt, werden die Ergebnisse auf der Suchseite der Geschenkregistrierung angezeigt. Wenn die Suche keine Ergebnisse zurückgibt, kann der Kunde es erneut mit anderen Parametern versuchen.

![Beispiel-Storefront - Geschenkregistrierungssuche](./assets/storefront-gift-registry-search.png){width="700" zoomable="yes"}

## Konfigurieren der Geschenkregistrierungssuche

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**.

1. Klicken Sie oben rechts auf **[!UICONTROL Add Widget]**.

1. Wählen Sie die Registerkarte **[!UICONTROL Settings]** aus und führen Sie folgende Schritte aus:

   - Legen Sie **[!UICONTROL Type]** auf `Gift Registry Search` fest.

   - Legen Sie **[!UICONTROL Design Theme]** auf das Design fest, das vom Store verwendet wird.

   - Klicken Sie auf **[!UICONTROL Continue]**.

   ![Geschenkregistrierung - Sucheinstellungen](./assets/widget-gift-registry-search-settings.png){width="700" zoomable="yes"}

1. Gehen Sie im Abschnitt _[!UICONTROL Storefront Properties]_wie folgt vor:

   - Geben Sie eine **[!UICONTROL Widget Title]** als interne Referenz ein.

   - Legen Sie **[!UICONTROL Assign to Store Views]** auf die Store-Ansichten fest, in denen die Geschenkregistrierungssuche verfügbar sein soll.

   - Legen Sie **[!UICONTROL Sort Order]** fest, um die Reihenfolge zu bestimmen, in der der Suchblock „Geschenkregistrierung“ angezeigt wird, wenn andere Blöcke demselben Speicherort auf der Seite zugewiesen sind.

   ![Geschenkregistrierung - Storefront-Eigenschaften](./assets/widget-gift-registry-search-storefront-properties.png){width="700" zoomable="yes"}

1. Klicken Sie im Abschnitt **[!UICONTROL Layout Updates]** auf **[!UICONTROL Add Layout Update]**.

1. Gehen Sie wie folgt vor, um zu bestimmen, wo die Geschenkregistrierungssuche im Store angezeigt wird:

   - Legen Sie **[!UICONTROL Display On]** auf die Seiten in Ihrem Store fest, auf denen der Geschenkregistrierungs-Suchblock angezeigt werden soll.

   - Wählen Sie ggf. die **[!UICONTROL Categories]** aus, in der sie angezeigt werden soll.

   - Legen Sie **[!UICONTROL Container]** auf die Position auf der Seite fest, um den Suchblock für die Geschenkregistrierung zu platzieren.

   ![Geschenkregistrierung - Layout-Aktualisierungen](./assets/widget-gift-registry-search-layout-updates.png){width="500" zoomable="yes"}

1. Wählen Sie im linken Bedienfeld **[!UICONTROL Widget Options]** aus.

1. Um zu bestimmen, wie Besucher Ihrer Site nach Geschenkregistern suchen können, wählen Sie beliebig viele der folgenden Optionen aus:

   - [!UICONTROL All Forms]
   - [!UICONTROL Registrant Name Search]
   - [!UICONTROL Registrant Email Search]
   - [!UICONTROL Gift Registry ID Search]

   ![Geschenkregistrierung - Widget-Optionen](./assets/widget-gift-registry-search-widget-options.png){width="700" zoomable="yes"}

1. Klicken Sie abschließend auf **[!UICONTROL Save]**.

1. Wenn Sie aufgefordert werden, den Seiten-Cache zu aktualisieren, klicken Sie auf den Link in der Nachricht oben im Arbeitsbereich und folgen Sie den Anweisungen.

## Feldbeschreibungen

### [!UICONTROL Settings]

| Feld | Beschreibung |
|--- |--- |
| [!UICONTROL Type] | Gibt `Gift Registry Search` als Typ des Widgets an. |
| [!UICONTROL Design Theme] | Das Design, das vom Store verwendet wird, in dem die Geschenkregistrierungssuche angezeigt werden soll. |

{style="table-layout:auto"}

### [!UICONTROL Storefront Properties]

| Feld | Beschreibung |
|--- |--- |
| [!UICONTROL Widget Title] | Ein Name für die interne Referenz. |
| [!UICONTROL Assign to Store Views] | Gibt die Store-Ansichten an, in denen die Geschenkregistrierungssuche verfügbar sein soll. |
| [!UICONTROL Sort Order] | Gibt die Reihenfolge an, in der der Suchblock für die Geschenkregistrierung angezeigt wird, wenn andere Blöcke zugewiesen sind, die an derselben Stelle angezeigt werden. |

{style="table-layout:auto"}

### [!UICONTROL Layout Updates]

| Feld | Beschreibung |
|--- |--- |
| [!UICONTROL Display On] | Geben Sie die spezifischen Seiten oder Seitentypen an, auf denen der Geschenkregistrierungs-Suchblock angezeigt wird. |
| [!UICONTROL Categories] | Gibt gegebenenfalls die Kategorieseiten an, auf denen die Geschenkregistrierungssuche angezeigt wird. |
| [!UICONTROL Container] | Gibt den Seiten-Layout-Block an, in dem die Geschenkregistrierungssuche platziert ist. Die Optionen variieren je nach Vorlage und Design. |

{style="table-layout:auto"}

### [!UICONTROL Widget Options]

| Feld | Beschreibung |
|--- |--- |
| [!UICONTROL Quick Search Form Types] | Bestimmt die Arten von Suchen, die mit der Geschenkregistrierungssuche durchgeführt werden können. Optionen: `All Forms` / `Registrant Name Search` /` Registrant Email Search` / `Gift Registry ID Search` |

{style="table-layout:auto"}
