---
title: Einführung in die Katalogverwaltung
description: Erfahren Sie, wie Katalog und Produktbereich im Katalogmanagement funktionieren.
exl-id: 3c58fc1c-d7a3-4f51-8a78-6bf2fd0dbeee
source-git-commit: f36925217230e558043078fdc274f5e69c096c1e
workflow-type: tm+mt
source-wordcount: '775'
ht-degree: 0%

---

# Einführung in die Katalogverwaltung

Adobe Commerce und Magento Open Source verwenden den Begriff _catalog_, um auf die Produktdatenbank als Ganzes zu verweisen.

Einer der wichtigsten Bereiche beim Erstellen und Verwalten Ihres Geschäfts ist die Erstellung von Produkten und Kategorien. Der Administrator bietet verschiedene Tools, die Sie für die Ersteinrichtung Ihres Stores sowie für die Wartung Ihres Stores und die Optimierung Ihres Unternehmens verwenden.

>[!TIP]
>
>Inventory management für Adobe Commerce und Magento Open Source bietet Ihnen die Tools zur Verwaltung Ihres Produktbestands. Händler mit einem einzigen Geschäft zu mehreren Lagern, Geschäften, Abholstandorten, Ablagelagern und mehr können diese Funktionen nutzen, um die Mengen für den Verkauf zu halten und Sendungen für komplette Bestellungen abzuwickeln. Weitere Informationen zu diesen Funktionen und wie Sie sie zur Verwaltung von Lagern an mehreren Standorten verwenden können, finden Sie im [Inventory management-Benutzerhandbuch](../inventory-management/introduction.md).

## Katalogbereich

Der Zugriff auf Katalogdaten wird durch verschiedene Faktoren bestimmt, darunter die Einstellung [Perimeter](../getting-started/websites-stores-views.md#scope-settings), die Katalogkonfiguration und die dem Store zugewiesene [Stammkategorie](category-root.md). Der Katalog enthält Produkte, die aktiviert und zum Verkauf angeboten werden, sowie Produkte, die derzeit nicht zum Verkauf angeboten werden.

Beim Verkauf bezieht sich der Begriff _Katalog_ normalerweise auf eine kuratierte Auswahl von Produkten, die zum Verkauf angeboten werden. Ein Store könnte beispielsweise über einen &quot;Frühjahrskatalog&quot;und einen &quot;Herbstkatalog&quot;verfügen.

Wie das Inhaltsverzeichnis eines gedruckten Katalogs organisiert auch das Hauptmenü Ihres Stores - oder _oberste Navigation_ - Produkte nach Kategorie, um es den Kunden zu erleichtern, das zu finden, was sie wollen. Das Hauptmenü basiert auf einer _Stammkategorie_, die ein Container für das Menü ist, das dem Store zugewiesen ist. Da die spezifischen Menüoptionen auf der Ebene der Store-Ansicht definiert sind, kann jede Ansicht ein anderes Hauptmenü basierend auf derselben Stammkategorie haben. In jedem Menü können Sie eine kuratierte Auswahl an Produkten anbieten, die für den Laden geeignet sind.

![Kataloghierarchiediagramm](./assets/catalog-hierarchy-scope.svg){width="550"}

## Produktbereich

Bei Installationen mit mehreren Websites, Stores und Ansichten bestimmt die Einstellung [scope](../getting-started/websites-stores-views.md#scope-settings) , wo Produkte zum Verkauf angeboten werden, und welche Produktinformationen für jede Store-Ansicht verfügbar sind. Zunächst werden alle von Ihnen erstellten Produkte in der standardmäßigen Website-, Store- und Store-Ansicht veröffentlicht.

![Multi-Site-Store-Diagramm](./assets/scope-multisite.svg){width="550"}

Wenn Sie nur einen einzigen Store mit der Standardansicht haben, können Sie Ihren Store im [Einzelspeichermodus](../getting-started/websites-stores-views.md#single-store-mode) ausführen, um die Bereichseinstellungen auszublenden. Wenn Ihr Store jedoch mehrere Ansichten hat, wird unter dem Namen jedes Felds eine Scope-Anzeige angezeigt.

- Um Produktinformationen für eine bestimmte Ansicht zu bearbeiten, verwenden Sie das Steuerelement _Store-Ansicht_ in der oberen linken Ecke, um die Ansicht auszuwählen. Zusätzliche Steuerelemente stehen für alle Felder zur Verfügung, die auf der Ebene der Store-Ansicht bearbeitet werden können.

- Informationen zum Definieren des Umfangs eines Produkts in einer Multisite-Installation finden Sie im Abschnitt [Produkt in Websites](settings-basic-websites.md) der Produktinformationen.

Der Prozess der Bearbeitung eines Produkts für eine Store-Ansicht ähnelt dem Hinzufügen einer Schicht von Produktinformationen, die für die Ansicht spezifisch sind.

Sie können nur Produkte für die Site bearbeiten oder zuweisen, für die Sie Berechtigungen haben, nicht für alle Sites, auf denen das Produkt zugewiesen ist.

Obwohl die Store-Ansicht _Spanisch_ im folgenden Beispiel ausgewählt ist, werden die Produktinformationen weiterhin in der Originalsprache der standardmäßigen Store-Ansicht angezeigt. Um die Produktinformationen zu übersetzen, müssen Sie zur Store-Ansicht &quot;_Spanisch_&quot;wechseln und die Textfelder übersetzen, z. B. Produktname, Beschreibung und Metadaten. Weitere Informationen finden Sie unter [Produkte lokalisieren](../stores-purchase/store-localize.md#localize-products).

## Produkt für eine andere Ansicht bearbeiten

>[!NOTE]
>
>Der Bereich _Alle Store-Ansichten_ ist für Admin-Benutzer deaktiviert, die auf einen bestimmten Bereich beschränkt sind, wenn das Produkt auch außerhalb des zulässigen Bereichs veröffentlicht wird. Der erste Bereich, der zur Bearbeitung verfügbar ist, ist standardmäßig ausgewählt, da eingeschränkte Benutzer keine _globalen_ Aktionen oder Aktionen ausführen können, die sich auf Bereiche auswirken, auf die sie keinen Zugriff haben.

1. Setzen Sie oben links **[!UICONTROL Store View]** auf die jeweilige Ansicht, die bearbeitet werden soll.

1. Um die Perimeteränderung zu bestätigen, klicken Sie auf **[!UICONTROL OK]**.

1. Aktualisieren Sie das Feld mit dem neuen Wert für die Store-Ansicht.

   Unter jedem Feld, das für die Store-Ansicht bearbeitet werden kann, wird ein Kontrollkästchen angezeigt. Um den Standardwert zu überschreiben, deaktivieren Sie das Kontrollkästchen **Standardwert verwenden** .

   ![Übersetzung des Produktnamens für die spanische Store-Ansicht](./assets/product-translate-field-french.png){width="600" zoomable="yes"}

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save]**.

1. Setzen Sie in der oberen linken Ecke die Auswahl **[!UICONTROL Store View]** wieder auf den Standard.

1. Gehen Sie wie folgt vor, um die Änderung in Ihrem Store zu überprüfen:

   - Klicken Sie in der oberen rechten Ecke auf den Menüpfeil _Admin_ und wählen Sie **[!UICONTROL Customer View]**.

     ![Kundenansicht](./assets/product-admin-menu-customer-view.png){width="600" zoomable="yes"}

   - Legen Sie in der rechten oberen Ecke des Stores den Wert &quot;**[!UICONTROL Language Chooser]**&quot;auf die Store-Ansicht des bearbeiteten Produkts fest und suchen Sie nach dem Produkt, das Sie für die Ansicht bearbeitet haben.

     ![Sprachauswahl](./assets/storefront-language-chooser.png){width="700" zoomable="yes"}
