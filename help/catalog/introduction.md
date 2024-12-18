---
title: Einführung in die Katalogverwaltung
description: Erfahren Sie, wie der Katalog und der Produktumfang in der Katalogverwaltung funktionieren.
exl-id: 3c58fc1c-d7a3-4f51-8a78-6bf2fd0dbeee
source-git-commit: f36925217230e558043078fdc274f5e69c096c1e
workflow-type: tm+mt
source-wordcount: '775'
ht-degree: 0%

---

# Einführung in die Katalogverwaltung

Adobe Commerce und Magento Open Source verwenden den Begriff _Katalog_, um auf die Produktdatenbank als Ganzes zu verweisen.

Einer der wichtigsten Bereiche bei der Erstellung und Verwaltung Ihres Stores ist die Produkterstellung und -kategorien. Der Administrator stellt mehrere Tools bereit, die Sie für die Ersteinrichtung Ihres Stores sowie für die Wartung Ihres Stores und die Optimierung Ihres Geschäfts verwenden können.

>[!TIP]
>
>Inventory management für Adobe Commerce und Magento Open Source bietet Ihnen die Tools zur Verwaltung Ihres Produktbestands. Händler mit einem einzigen Shop für mehrere Lager, Geschäfte, Abholorte, Drop-Versender und mehr können diese Funktionen verwenden, um Mengen für den Verkauf zu verwalten und Sendungen zu bearbeiten, um Bestellungen abzuschließen. Weitere Informationen zu diesen Funktionen und deren Verwendung zur Verwaltung von Lagern an mehreren Orten finden Sie im [Inventory management-Benutzerhandbuch](../inventory-management/introduction.md).

## Katalogbereich

Der Zugriff auf Katalogdaten wird durch mehrere Faktoren bestimmt, darunter die [Bereich](../getting-started/websites-stores-views.md#scope-settings)-Einstellung, die Katalogkonfiguration und die [Stammkategorie](category-root.md) die dem Store zugewiesen ist. Der Katalog enthält Produkte, die aktiviert und zum Verkauf verfügbar sind, sowie Produkte, die derzeit nicht zum Verkauf angeboten werden.

Im Vertrieb bezieht sich der Begriff _Katalog_ normalerweise auf eine kuratierte Auswahl von Produkten, die zum Verkauf angeboten werden. Beispielsweise könnte ein Geschäft einen „Frühlingskatalog“ und einen „Herbstkatalog“ haben.

Wie das Inhaltsverzeichnis eines gedruckten Katalogs organisiert das Hauptmenü Ihres Geschäfts - oder _Top-Navigation_ - Produkte nach Kategorie, um es den Kunden zu erleichtern, zu finden, was sie möchten. Das Hauptmenü basiert auf einer _Stammkategorie_ die ein Container für das Menü ist, das dem Store zugewiesen ist. Da die spezifischen Menüoptionen auf der Store-Ansichtsebene definiert werden, kann jede Ansicht ein anderes Hauptmenü basierend auf derselben Stammkategorie haben. Innerhalb jedes Menüs können Sie eine kuratierte Auswahl von Produkten anbieten, die für den Store geeignet ist.

![Katalog-Hierarchie-Diagramm](./assets/catalog-hierarchy-scope.svg){width="550"}

## Produktpalette

Bei Installationen mit mehreren Websites, Geschäften und Ansichten bestimmt die Einstellung [Umfang](../getting-started/websites-stores-views.md#scope-settings), wo Produkte zum Verkauf verfügbar sind, sowie die Produktinformationen, die für jede Shop-Ansicht verfügbar sind. Zunächst werden alle von Ihnen erstellten Produkte in der standardmäßigen Website-, Store- und Store-Ansicht veröffentlicht.

![Multi-Site-Store-Diagramm](./assets/scope-multisite.svg){width="550"}

Wenn Sie nur über einen einzigen Store mit der Standardansicht verfügen, können Sie Ihren Store im [Einzelspeichermodus) ausführen](../getting-started/websites-stores-views.md#single-store-mode) um die Bereichseinstellungen auszublenden. Wenn Ihr Store jedoch über mehrere Ansichten verfügt, wird unter dem Namen jedes Felds ein Indikator für den Umfang angezeigt.

- Um die Produktinformationen für eine bestimmte Ansicht zu bearbeiten, wählen Sie mit dem Steuerelement _Store-_&quot; in der linken oberen Ecke die Ansicht aus. Zusätzliche Steuerelemente werden für alle Felder verfügbar, die auf Store-Ansichtsebene bearbeitet werden können.

- Informationen zum Definieren des Umfangs eines Produkts in einer Multi-Site-Installation finden Sie [ Abschnitt „Produkt in ](settings-basic-websites.md)&quot;.

Der Prozess der Bearbeitung eines Produkts für eine Store-Ansicht entspricht dem Hinzufügen einer Ebene mit Produktinformationen, die für die Ansicht spezifisch sind.

Sie können Produkte nur für die Site bearbeiten oder zuweisen, für die Sie Berechtigungen haben, nicht für alle Sites, denen das Produkt zugewiesen ist.

Obwohl im folgenden Beispiel _Store_ Ansicht „Spanisch“ ausgewählt ist, werden die Produktinformationen weiterhin in der Originalsprache der standardmäßigen Store-Ansicht angezeigt. Um die Produktinformationen zu übersetzen, müssen Sie zur Store _Ansicht „Spanisch_ wechseln und die Textfelder übersetzen - wie Produkttitel, Beschreibung und die Metadaten. Weitere Informationen finden Sie unter [Produkte lokalisieren](../stores-purchase/store-localize.md#localize-products).

## Produkt für eine andere Ansicht bearbeiten

>[!NOTE]
>
>Der _Alle Store-_&quot; ist für Admin-Benutzer deaktiviert, die auf einen bestimmten Bereich beschränkt sind, wenn das Produkt auch außerhalb des zulässigen Bereichs veröffentlicht wird. Der erste zur Bearbeitung verfügbare Bereich ist standardmäßig ausgewählt, da eingeschränkte Benutzer keine _globalen_ Aktionen oder Aktionen ausführen können, die Bereiche betreffen, in denen sie keinen Zugriff haben.

1. Legen Sie in der oberen linken Ecke **[!UICONTROL Store View]** auf die spezifische Ansicht fest, die bearbeitet werden soll.

1. Um die Änderung des Umfangs zu bestätigen, klicken Sie auf **[!UICONTROL OK]**.

1. Aktualisieren Sie das Feld mit dem neuen Wert für die Store-Ansicht.

   Unter jedem Feld, das für die Store-Ansicht bearbeitet werden kann, wird ein Kontrollkästchen angezeigt. Um den Standardwert zu überschreiben, deaktivieren Sie das Kontrollkästchen **Standardwert verwenden**.

   ![Übersetzen des Produktnamens für die spanische Shop-Ansicht](./assets/product-translate-field-french.png){width="600" zoomable="yes"}

1. Klicken Sie abschließend auf **[!UICONTROL Save]**.

1. Setzen Sie die **[!UICONTROL Store View]** in der oberen linken Ecke wieder auf den Standardwert zurück.

1. Gehen Sie wie folgt vor, um die Änderung in Ihrem Store zu überprüfen:

   - Klicken Sie oben rechts auf den Menüpfeil _Admin_ und wählen Sie **[!UICONTROL Customer View]** aus.

     ![Kundenansicht](./assets/product-admin-menu-customer-view.png){width="600" zoomable="yes"}

   - Legen Sie in der oberen rechten Ecke des Stores den **[!UICONTROL Language Chooser]** auf die Store-Ansicht des bearbeiteten Produkts fest und suchen Sie das Produkt, das Sie für die Ansicht bearbeitet haben.

     ![Sprachauswahl](./assets/storefront-language-chooser.png){width="700" zoomable="yes"}
